
<!---
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
-->
# Apache Hive  3.0.0 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [HIVE-16281](https://issues.apache.org/jira/browse/HIVE-16281) | *Major* | **Upgrade master branch to JDK8**

With this change, we are switching to build master branch with JDK8


---

* [HIVE-12274](https://issues.apache.org/jira/browse/HIVE-12274) | *Major* | **Increase width of columns used for general configuration in the metastore.**

Increased width of metastore text columns for general configuration storage.


---

* [HIVE-15434](https://issues.apache.org/jira/browse/HIVE-15434) | *Major* | **Add UDF to allow interrogation of uniontype values**

Added UDF to allow interrogation of uniontype values.


---

* [HIVE-16049](https://issues.apache.org/jira/browse/HIVE-16049) | *Major* | **upgrade to jetty 9**

Embedded web services now rely on Jetty 9; downstream users who rely on Hive's classpath for their Jetty jars will need to update their use for the change.


---

* [HIVE-16520](https://issues.apache.org/jira/browse/HIVE-16520) | *Major* | **Cache hive metadata in metastore**

To use CachedStore, please set hive.metastore.rawstore.impl to "org.apache.hadoop.hive.metastore.cache.CachedStore" in hive-site.xml.


---

* [HIVE-16269](https://issues.apache.org/jira/browse/HIVE-16269) | *Major* | **enable incremental function dump to be loaded via repl load**

Committed to master.


---

* [HIVE-14412](https://issues.apache.org/jira/browse/HIVE-14412) | *Major* | **Add timestamp with time zone**

HIVE-14412 adds 'timestamp with time zone' data type to Hive. The full qualified input format of this type is 'yyyy-MM-dd HH:mm:ss[.SSS...] ZoneId/ZoneOffset', where the time and zone parts are optional. If time part is absent, a default '00:00:00.0' will be used. If zone part is absent, the system time zone will be used. Examples of valid ZoneId and ZoneOffset are: America/Los\_Angeles and GMT+08:00. All timestamp with time zone will be converted and stored as UTC retaining the instant. E.g. '2017-04-14 18:00:00 Asia/Shanghai' will be converted and stored as '2017-04-14 10:00:00.0 Z'.
'timestamptz' is accepted as a type alias for 'timestamp with time zone'.
Conversion between date/timestamp and timestamp with time zone is done using the system time zone.
'time' becomes a reserved key word after HIVE-14412, thus can break user queries where 'time' is used as identifiers. If users want to continue use 'time' as identifiers, they have to escape it with '\`' (backtick).


---

* [HIVE-1010](https://issues.apache.org/jira/browse/HIVE-1010) | *Major* | **Implement INFORMATION\_SCHEMA in Hive**

New method added to StorageHandler to pass credentials around.

Adds db type to hive schematool. The db type is "hive". When you run the schematool w/ hive it installs the "sys" db and the "information\_schema" db. both contain tables and views that expose meta information about tables, columns etc.


---

* [HIVE-16686](https://issues.apache.org/jira/browse/HIVE-16686) | *Major* | **repl invocations of distcp needs additional handling**

This introduces parsing of additional parameters that are not directly used by hive, but are passed on to distcp when hive invokes it. We now introduce the ability to use the hive command to do "set" commands to pass along cli arguments to distcp.

Any parameter set as "set distcp.options.blah=''" will result in an extra "-blah" argument going into distcp, as well as any parameter set as "set distcp.options.foo='bar'" will result in an extra "-foo bar" argument going to distcp.

Currently, we always pass along "-update" and "-skipcrccheck" to distcp - that is retained as defaults if no distcp.options.\* params are found. If they are found, then these options are not added by default, letting the user instead provide an excplicit list.

Note that all of these properties affect how distcp runs when it is launched by hive, but are not directly hive settings. Instead, hive will allow setting them through the use of the "set" command.


---

* [HIVE-16799](https://issues.apache.org/jira/browse/HIVE-16799) | *Major* | **Control the max number of task for a stage in a spark job**

Document the new configuration.


---

* [HIVE-17429](https://issues.apache.org/jira/browse/HIVE-17429) | *Major* | **Hive JDBC doesn't return rows when querying Impala**

Check for resultSet returned by TExecuteRequest in Hive JDBC.  This preserves compatibility when fetching data from Impala.


---

* [HIVE-17483](https://issues.apache.org/jira/browse/HIVE-17483) | *Major* | **HS2 kill command to kill queries using query id**

In HiveConnection - 
static List\<JdbcConnectionParams\> getAllUrls(String zookeeperBasedHS2Url)
You can call
JdbcConnectionParams.toString() to get the actual URL

In HiveStatement -
You can get query id of a running query using -
String getQueryId()

You can kill hive queries using 
"KILL QUERY \<queryid1\> \<queryid2\>"


---

* [HIVE-17679](https://issues.apache.org/jira/browse/HIVE-17679) | *Major* | **http-generic-click-jacking for WebHcat server**

Security fix: Adds protection from clickjacking using X-Frame-Options header. 
This will prevent use of WebHCat UI in frames. A new configuration 'templeton.frame.options.filter' is added to allow configuring such option.


---

* [HIVE-15016](https://issues.apache.org/jira/browse/HIVE-15016) | *Major* | **Run tests with Hadoop 3.0.0-beta1**

With this change, Hive is pointing to Hadoop 3.0.0-beta1 and HBase 2.0.0-alpha3.


---

* [HIVE-17710](https://issues.apache.org/jira/browse/HIVE-17710) | *Major* | **LockManager should only lock Managed tables**

The LockManager which is installed automatically when enabling Acid (hive.txn.manager=org.apache.hadoop.hive.ql.lockmgr.DbTxnManager) does not lock any External Tables since Hive has no control over what is modifying the data in such tables.


---

* [HIVE-18419](https://issues.apache.org/jira/browse/HIVE-18419) | *Major* | **CliDriver loads different hive-site.xml into HiveConf and MetastoreConf**

n/a


---

* [HIVE-18606](https://issues.apache.org/jira/browse/HIVE-18606) | *Major* | **CTAS on empty table throws NPE from org.apache.hadoop.hive.ql.exec.MoveTask**

N/A


---

* [HIVE-18552](https://issues.apache.org/jira/browse/HIVE-18552) | *Major* | **Split hive.strict.checks.large.query into two configs**

This change splits {{hive.strict.checks.large.query}} into two new configs: {{hive.strict.checks.no.partition.filter}} and {{hive.strict.checks.orderby.no.limit}}

Previously, {{hive.strict.checks.large.query}} controlled whether or not (1) order bys were allowed without limits, and (2) scans on partitioned tables were allowed without filters.

After this change, {{hive.strict.checks.no.partition.filter}} controls the partitioned table check and {{hive.strict.checks.orderby.no.limit}} controls the order by check.


---

* [HIVE-18693](https://issues.apache.org/jira/browse/HIVE-18693) | *Major* | **Snapshot Isolation does not work for Micromanaged table when a insert transaction is aborted**

n/a


---

* [HIVE-18963](https://issues.apache.org/jira/browse/HIVE-18963) | *Major* | **JDBC: Provide an option to simplify beeline usage by supporting default and named URL for beeline**

https://cwiki.apache.org/confluence/display/Hive/HiveServer2+Clients#HiveServer2Clients-Usingbeeline-site.xmltoautomaticallyconnecttoHiveServer2


---

* [HIVE-19100](https://issues.apache.org/jira/browse/HIVE-19100) | *Major* | **investigate TestStreaming failures**

n/a


---

* [HIVE-19014](https://issues.apache.org/jira/browse/HIVE-19014) | *Major* | **utilize YARN-8028 (queue ACL check) in Hive Tez session pool**

This feature will only work with YARN 3.2+; there's no compile time dependency thanks to the REST API usage, so Hive may release this before YARN 3.2 is even available.


---

* [HIVE-18739](https://issues.apache.org/jira/browse/HIVE-18739) | *Major* | **Add support for Import/Export from Acid table**

n/a


---

* [HIVE-19137](https://issues.apache.org/jira/browse/HIVE-19137) | *Major* | **orcfiledump doesn't print hive.acid.version value**

n/a


---

* [HIVE-19315](https://issues.apache.org/jira/browse/HIVE-19315) | *Major* | **Test failure org.apache.hadoop.hive.ql.lockmgr.TestDbTxnManager2#testWriteSetTracking3**

n/a


---

* [HIVE-17457](https://issues.apache.org/jira/browse/HIVE-17457) | *Major* | **IOW Acid Insert Overwrite when the transaction fails**

n/a


---

* [HIVE-18131](https://issues.apache.org/jira/browse/HIVE-18131) | *Major* | **Truncate table for Acid tables**

n/a


---

* [HIVE-18380](https://issues.apache.org/jira/browse/HIVE-18380) | *Minor* | **ALTER TABLE CONCATENATE is not supported on Micro-managed table**

n/a


---

* [HIVE-12451](https://issues.apache.org/jira/browse/HIVE-12451) | *Major* | **Orc fast file merging/concatenation should be disabled for ACID tables**

Concatenate is now supported on Acid tables



