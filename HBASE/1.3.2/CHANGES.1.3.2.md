
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
# Apache HBase Changelog

## Release 1.3.2 - Unreleased (as of 2017-05-12)



### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HBASE-17916](https://issues.apache.org/jira/browse/HBASE-17916) | Error message not clear when the permission of staging dir is not as expected |  Minor | Operability | Xiang Li | Xiang Li |
| [HBASE-17944](https://issues.apache.org/jira/browse/HBASE-17944) | Removed unused JDK version parsing from ClassSize. |  Minor | build | Colm O hEigeartaigh | Colm O hEigeartaigh |
| [HBASE-17514](https://issues.apache.org/jira/browse/HBASE-17514) | Warn when Thrift Server 1 is configured for proxy users but not the HTTP transport |  Minor | Thrift, Usability | Sean Busbey | lv zehui |
| [HBASE-17877](https://issues.apache.org/jira/browse/HBASE-17877) | Improve HBase's byte[] comparator |  Major | util | Lars Hofhansl | Vikas Vishwakarma |
| [HBASE-17817](https://issues.apache.org/jira/browse/HBASE-17817) | Make Regionservers log which tables it removed coprocessors from when aborting |  Major | Coprocessors, regionserver | Steen Manniche | Steen Manniche |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HBASE-17902](https://issues.apache.org/jira/browse/HBASE-17902) | Backport HBASE-16367 "Race between master and region server initialization may lead to premature server abort" to 1.3 |  Major | . | Ted Yu | Ted Yu |
| [HBASE-17937](https://issues.apache.org/jira/browse/HBASE-17937) | Memstore size becomes negative in case of expensive postPut/Delete Coprocessor call |  Major | regionserver | Abhishek Singh Chouhan | Abhishek Singh Chouhan |
| [HBASE-17862](https://issues.apache.org/jira/browse/HBASE-17862) | Condition that always returns true |  Trivial | Client | JC | JC |
| [HBASE-17985](https://issues.apache.org/jira/browse/HBASE-17985) | Inline package manage updates with package installation in Yetus Dockerfile |  Blocker | . | Josh Elser | Josh Elser |
| [HBASE-17534](https://issues.apache.org/jira/browse/HBASE-17534) | SecureBulkLoadClient squashes DoNotRetryIOExceptions from the server |  Major | Client | Josh Elser | Josh Elser |
| [HBASE-8758](https://issues.apache.org/jira/browse/HBASE-8758) | Error in RegionCoprocessorHost class preScanner method documentation. |  Minor | Coprocessors, documentation | Roman Nikitchenko |  |
| [HBASE-18026](https://issues.apache.org/jira/browse/HBASE-18026) | ProtobufUtil seems to do extra array copying |  Minor | . | Vincent Poon | Vincent Poon |
| [HBASE-18000](https://issues.apache.org/jira/browse/HBASE-18000) | Make sure we always return the scanner id with ScanResponse |  Major | regionserver | Lars Hofhansl | Duo Zhang |
| [HBASE-17887](https://issues.apache.org/jira/browse/HBASE-17887) | Row-level consistency is broken for read |  Blocker | regionserver | Umesh Agashe | Chia-Ping Tsai |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HBASE-17925](https://issues.apache.org/jira/browse/HBASE-17925) | mvn assembly:single fails against hadoop3-alpha2 |  Major | hadoop3 | Jonathan Hsieh | Jonathan Hsieh |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HBASE-17968](https://issues.apache.org/jira/browse/HBASE-17968) | Update copyright year in NOTICE file |  Trivial | build | Nick Dimiduk | Josh Elser |

