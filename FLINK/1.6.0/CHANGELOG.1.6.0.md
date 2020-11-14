
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
# Apache Flink Changelog

## Release 1.6.0 - Unreleased (as of 2020-11-14)



### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-9935](https://issues.apache.org/jira/browse/FLINK-9935) | Batch Table API: grouping by window and attribute causes java.lang.ClassCastException: |  Critical | Table SQL / API | Roman Wozniak | Fabian Hueske |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-8620](https://issues.apache.org/jira/browse/FLINK-8620) | Enable shipping custom artifacts to BlobStore and accessing them through DistributedCache |  Major | . | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9316](https://issues.apache.org/jira/browse/FLINK-9316) | Expose operator unique ID to the user defined functions in DataStream . |  Major | . | Piotr Nowojski | Piotr Nowojski |
| [FLINK-8838](https://issues.apache.org/jira/browse/FLINK-8838) | Add Support for UNNEST a MultiSet type field |  Major | Table SQL / API | lincoln lee | lincoln lee |
| [FLINK-7836](https://issues.apache.org/jira/browse/FLINK-7836) | specifying node label for flink job to run on yarn |  Major | Command Line Client | zhaibaba | vinoyang |
| [FLINK-5878](https://issues.apache.org/jira/browse/FLINK-5878) | Add stream-stream non-window inner/outer join |  Major | Table SQL / API | Shaoxuan Wang | Hequn Cheng |
| [FLINK-9566](https://issues.apache.org/jira/browse/FLINK-9566) | Support listing all jobs in CliFrontend#list |  Major | Command Line Client | Chesnay Schepler | Rong Rong |
| [FLINK-9564](https://issues.apache.org/jira/browse/FLINK-9564) | Expose end-to-end module directory to test scripts |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8744](https://issues.apache.org/jira/browse/FLINK-8744) | Add annotations for documenting common/advanced options |  Trivial | Documentation, Runtime / Configuration | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9599](https://issues.apache.org/jira/browse/FLINK-9599) | Implement generic mechanism to receive files via rest |  Major | Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9557](https://issues.apache.org/jira/browse/FLINK-9557) | Parse 'integer' type as BigDecimal |  Major | . | Dominik Wosiński | Timo Walther |
| [FLINK-9280](https://issues.apache.org/jira/browse/FLINK-9280) | Extend JobSubmitHandler to accept jar files |  Critical | Runtime / Coordination, Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9153](https://issues.apache.org/jira/browse/FLINK-9153) | TaskManagerRunner should support rpc port range |  Major | Runtime / Coordination | vinoyang | vinoyang |
| [FLINK-9187](https://issues.apache.org/jira/browse/FLINK-9187) | add prometheus pushgateway reporter |  Minor | Runtime / Metrics | lamber-ken | lamber-ken |
| [FLINK-9823](https://issues.apache.org/jira/browse/FLINK-9823) | Add Kubernetes deployment files for standalone job cluster |  Major | Deployment / Kubernetes | Till Rohrmann | Till Rohrmann |
| [FLINK-9822](https://issues.apache.org/jira/browse/FLINK-9822) | Add Dockerfile for StandaloneJobClusterEntryPoint image |  Major | flink-docker | Till Rohrmann | Till Rohrmann |
| [FLINK-9819](https://issues.apache.org/jira/browse/FLINK-9819) | Create start up scripts for the StandaloneJobClusterEntryPoint |  Major | Deployment / Scripts | Till Rohrmann | Till Rohrmann |
| [FLINK-8558](https://issues.apache.org/jira/browse/FLINK-8558) | Add unified format interfaces and format discovery |  Major | Formats (JSON, Avro, Parquet, ORC, SequenceFile) | Timo Walther | Timo Walther |
| [FLINK-8866](https://issues.apache.org/jira/browse/FLINK-8866) | Create unified interfaces to configure and instatiate TableSinks |  Major | Table SQL / API | Timo Walther | Shuyi Chen |
| [FLINK-9312](https://issues.apache.org/jira/browse/FLINK-9312) | Perform mutual authentication during SSL handshakes |  Major | Runtime / Coordination | Stephan Ewen | Stephan Ewen |
| [FLINK-9852](https://issues.apache.org/jira/browse/FLINK-9852) | Expose descriptor-based sink creation and introduce update mode |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9846](https://issues.apache.org/jira/browse/FLINK-9846) | Add a Kafka table sink factory |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9499](https://issues.apache.org/jira/browse/FLINK-9499) | Allow REST API for running a job to provide job configuration as body of POST request |  Minor | Runtime / REST | Esteban Serrano | Esteban Serrano |
| [FLINK-8101](https://issues.apache.org/jira/browse/FLINK-8101) | Elasticsearch 6.x support |  Major | Connectors / ElasticSearch | Hai Zhou |  |
| [FLINK-10069](https://issues.apache.org/jira/browse/FLINK-10069) | Add docs for updates SSL model |  Major | Documentation | Stephan Ewen | Stephan Ewen |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-9041](https://issues.apache.org/jira/browse/FLINK-9041) | Refactor StreamTaskTest to not use scala and akka |  Trivial | Tests | Chesnay Schepler | Andrey Zagrebin |
| [FLINK-9136](https://issues.apache.org/jira/browse/FLINK-9136) | Remove StreamingProgramTestBase |  Minor | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9362](https://issues.apache.org/jira/browse/FLINK-9362) | Document that Flink doesn't guarantee transaction of modifying state and register timers in processElement() |  Major | Documentation | Bowen Li | Bowen Li |
| [FLINK-9392](https://issues.apache.org/jira/browse/FLINK-9392) | Add @FunctionalInterface annotations to all core functional interfaces |  Critical | . | Stephan Ewen | Stephan Ewen |
| [FLINK-9372](https://issues.apache.org/jira/browse/FLINK-9372) | Typo on Elasticsearch website link (elastic.io --\> elastic.co) |  Minor | Connectors / ElasticSearch, Documentation | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-7814](https://issues.apache.org/jira/browse/FLINK-7814) | Add BETWEEN and NOT BETWEEN expression to Table API |  Minor | Table SQL / API | Fabian Hueske | Ruidong Li |
| [FLINK-8511](https://issues.apache.org/jira/browse/FLINK-8511) | Remove legacy code for the TableType annotation |  Critical | Table SQL / API | Timo Walther | boshu Zheng |
| [FLINK-9305](https://issues.apache.org/jira/browse/FLINK-9305) | Register flink-s3-fs-hadoop for the s3a:// scheme as well |  Major | Connectors / FileSystem | Nico Kruber | Nico Kruber |
| [FLINK-9088](https://issues.apache.org/jira/browse/FLINK-9088) | Upgrade Nifi connector dependency to 1.6.0 |  Major | Connectors / Common | Ted Yu | Hai Zhou |
| [FLINK-9409](https://issues.apache.org/jira/browse/FLINK-9409) | Remove flink-avro and flink-json from /opt |  Major | Build System | Nico Kruber | Timo Walther |
| [FLINK-9355](https://issues.apache.org/jira/browse/FLINK-9355) | Simplify configuration of local recovery to a simple on/off |  Major | Runtime / State Backends | Stefan Richter | Stefan Richter |
| [FLINK-8655](https://issues.apache.org/jira/browse/FLINK-8655) | Add a default keyspace to CassandraSink |  Minor | Connectors / Cassandra | Christopher Hughes |  |
| [FLINK-7850](https://issues.apache.org/jira/browse/FLINK-7850) | Given each maven profile an activation property |  Major | Build System | Chesnay Schepler |  |
| [FLINK-9383](https://issues.apache.org/jira/browse/FLINK-9383) | Extend DistributedCache E2E test to cover directories |  Minor | Runtime / Task, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9436](https://issues.apache.org/jira/browse/FLINK-9436) | Remove generic parameter namespace from InternalTimeServiceManager |  Minor | Runtime / State Backends | Stefan Richter | Stefan Richter |
| [FLINK-9423](https://issues.apache.org/jira/browse/FLINK-9423) | Implement efficient deletes for heap based timer service |  Major | . | Stefan Richter | Stefan Richter |
| [FLINK-9464](https://issues.apache.org/jira/browse/FLINK-9464) | Clean up pom files |  Minor | Build System | Till Rohrmann | Till Rohrmann |
| [FLINK-7789](https://issues.apache.org/jira/browse/FLINK-7789) | Add handler for Async IO operator timeouts |  Major | API / DataStream | Karthik Deivasigamani | boshu Zheng |
| [FLINK-9476](https://issues.apache.org/jira/browse/FLINK-9476) | Lost sideOutPut Late Elements in CEP Operator |  Major | Library / CEP | Aitozi | Aitozi |
| [FLINK-7866](https://issues.apache.org/jira/browse/FLINK-7866) | Weigh list of preferred locations for scheduling |  Major | Runtime / Coordination | Till Rohrmann | Sihua Zhou |
| [FLINK-9518](https://issues.apache.org/jira/browse/FLINK-9518) | SSL setup Docs config example has wrong keys password |  Minor | Documentation | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-9517](https://issues.apache.org/jira/browse/FLINK-9517) | Fixing broken links on CLI and Upgrade Docs |  Trivial | Documentation | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-8790](https://issues.apache.org/jira/browse/FLINK-8790) | Improve performance for recovery from incremental checkpoint |  Major | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-9549](https://issues.apache.org/jira/browse/FLINK-9549) | Fix FlickCEP Docs broken link and minor style changes |  Trivial | Documentation, Library / CEP | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-9539](https://issues.apache.org/jira/browse/FLINK-9539) | Integrate flink-shaded 4.0 |  Major | Build System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9508](https://issues.apache.org/jira/browse/FLINK-9508) | General Spell Check on Flink Docs |  Trivial | Documentation | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-8759](https://issues.apache.org/jira/browse/FLINK-8759) | Prepare LengthFieldBasedFrameDecoder for Netty upgrade |  Major | Runtime / Network | Nico Kruber | Nico Kruber |
| [FLINK-8768](https://issues.apache.org/jira/browse/FLINK-8768) | Change NettyMessageDecoder to inherit from LengthFieldBasedFrameDecoder |  Major | Runtime / Network | Nico Kruber | Nico Kruber |
| [FLINK-3952](https://issues.apache.org/jira/browse/FLINK-3952) | Bump Netty to 4.1 |  Major | Runtime / Network | rektide de la fey | Piotr Nowojski |
| [FLINK-9538](https://issues.apache.org/jira/browse/FLINK-9538) | Make KeyedStateFunction an interface |  Major | . | Dawid Wysakowicz | vinoyang |
| [FLINK-9418](https://issues.apache.org/jira/browse/FLINK-9418) | Migrate SharedBuffer to use MapState |  Major | Library / CEP | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-6983](https://issues.apache.org/jira/browse/FLINK-6983) | Do not serialize States with NFA |  Major | Library / CEP | Dawid Wysakowicz | Dian Fu |
| [FLINK-9573](https://issues.apache.org/jira/browse/FLINK-9573) | Check for leadership with leader session id |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-8573](https://issues.apache.org/jira/browse/FLINK-8573) | Print JobID for failed jobs |  Major | Command Line Client | Chesnay Schepler | Andrey Zagrebin |
| [FLINK-9551](https://issues.apache.org/jira/browse/FLINK-9551) | FlinkCEP Scala Combining Patterns table has a missing pattern |  Minor | Documentation | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-9579](https://issues.apache.org/jira/browse/FLINK-9579) | Remove unnecessary clear with cep elementQueue |  Major | Library / CEP | Aitozi | Aitozi |
| [FLINK-9623](https://issues.apache.org/jira/browse/FLINK-9623) | Move zipping logic out of blobservice |  Major | Runtime / Coordination | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8944](https://issues.apache.org/jira/browse/FLINK-8944) | Use ListShards for shard discovery in the flink kinesis connector |  Minor | . | Kailash Hassan Dayanand | Kailash Hassan Dayanand |
| [FLINK-9638](https://issues.apache.org/jira/browse/FLINK-9638) | Add helper script to run single e2e test |  Minor | Tests | Florian Schmidt | Florian Schmidt |
| [FLINK-9594](https://issues.apache.org/jira/browse/FLINK-9594) | Add documentation for e2e test changes introduced with FLINK-9257 |  Minor | Tests | Florian Schmidt | Florian Schmidt |
| [FLINK-9595](https://issues.apache.org/jira/browse/FLINK-9595) | Add instructions to docs about ceased support of KPL version used in Kinesis connector |  Critical | Connectors / Kinesis, Documentation | Tzu-Li (Gordon) Tai | Tzu-Li (Gordon) Tai |
| [FLINK-8468](https://issues.apache.org/jira/browse/FLINK-8468) | Make the connector to take advantage of AMQP features (routing key, exchange and message properties) |  Major | Connectors/ RabbitMQ | Ph.Duveau | Ph.Duveau |
| [FLINK-9624](https://issues.apache.org/jira/browse/FLINK-9624) | Move jar/artifact upload logic out of JobGraph |  Major | Runtime / Coordination | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9666](https://issues.apache.org/jira/browse/FLINK-9666) | short-circuit logic should be used in boolean contexts |  Minor | API / DataStream | lamber-ken | lamber-ken |
| [FLINK-9672](https://issues.apache.org/jira/browse/FLINK-9672) | Fail fatally if we cannot submit job on added JobGraph signal |  Critical | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9660](https://issues.apache.org/jira/browse/FLINK-9660) | Allow passing custom artifacts to Mesos workers |  Major | Deployment / Mesos | Leonid Ishimnikov | Leonid Ishimnikov |
| [FLINK-9456](https://issues.apache.org/jira/browse/FLINK-9456) | Let ResourceManager notify JobManager about failed/killed TaskManagers |  Major | Runtime / Coordination | Till Rohrmann | Sihua Zhou |
| [FLINK-4301](https://issues.apache.org/jira/browse/FLINK-4301) | Parameterize Flink version in Quickstart bash script |  Major | Documentation | Timo Walther | Simone Robutti |
| [FLINK-8650](https://issues.apache.org/jira/browse/FLINK-8650) | Add tests and documentation for WINDOW clause |  Major | Table SQL / API | Timo Walther | Sergey Nuyanzin |
| [FLINK-9674](https://issues.apache.org/jira/browse/FLINK-9674) | Remove 65s sleep in QueryableState E2E test |  Major | Runtime / Queryable State, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8654](https://issues.apache.org/jira/browse/FLINK-8654) | Extend quickstart docs on how to submit jobs |  Major | Documentation, Quickstarts | Chesnay Schepler | Yazdan Shirvany |
| [FLINK-9578](https://issues.apache.org/jira/browse/FLINK-9578) | Allow to define an auto watermark interval in SQL Client |  Major | Table SQL / API, Table SQL / Client | Timo Walther | Timo Walther |
| [FLINK-9301](https://issues.apache.org/jira/browse/FLINK-9301) | NotSoMiniClusterIterations job fails on travis |  Critical | Tests | Chesnay Schepler | Andrey Zagrebin |
| [FLINK-9695](https://issues.apache.org/jira/browse/FLINK-9695) | Add option for Mesos executor to forcefully pull Docker images |  Major | Deployment / Mesos | Leonid Ishimnikov | Leonid Ishimnikov |
| [FLINK-9686](https://issues.apache.org/jira/browse/FLINK-9686) | Flink Kinesis Producer: Enable Kinesis authentication via AssumeRole |  Major | Connectors / Kinesis | Franz Thoma | Franz Thoma |
| [FLINK-9707](https://issues.apache.org/jira/browse/FLINK-9707) | LocalFileSystem does not support concurrent directory creations |  Blocker | FileSystems | Till Rohrmann | Till Rohrmann |
| [FLINK-9109](https://issues.apache.org/jira/browse/FLINK-9109) | Add flink modify command to documentation |  Major | Documentation | Till Rohrmann | Till Rohrmann |
| [FLINK-9729](https://issues.apache.org/jira/browse/FLINK-9729) | Duplicate lines for "Weekday name (Sunday .. Saturday)" |  Trivial | Documentation, Table SQL / API | Sergey Nuyanzin | Sergey Nuyanzin |
| [FLINK-9734](https://issues.apache.org/jira/browse/FLINK-9734) | Typo 'field-deleimiter' in SQL client docs |  Trivial | Documentation, Table SQL / API, Table SQL / Client | Sergey Nuyanzin | Sergey Nuyanzin |
| [FLINK-6469](https://issues.apache.org/jira/browse/FLINK-6469) | Configure Memory Sizes with units |  Major | . | Stephan Ewen | vinoyang |
| [FLINK-9593](https://issues.apache.org/jira/browse/FLINK-9593) | Unify AfterMatch semantics with SQL MATCH\_RECOGNIZE |  Major | Library / CEP | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9588](https://issues.apache.org/jira/browse/FLINK-9588) | Reuse the same conditionContext with in a same computationState |  Major | Library / CEP | Aitozi | Aitozi |
| [FLINK-9757](https://issues.apache.org/jira/browse/FLINK-9757) | Typos found in docs after hunspell run |  Trivial | Documentation | Sergey Nuyanzin | Sergey Nuyanzin |
| [FLINK-9742](https://issues.apache.org/jira/browse/FLINK-9742) | Expose Expression.resultType to public |  Major | Table SQL / API | Jungtaek Lim | Jungtaek Lim |
| [FLINK-9659](https://issues.apache.org/jira/browse/FLINK-9659) | Remove hard-coded sleeps in bucketing sink E2E test |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9352](https://issues.apache.org/jira/browse/FLINK-9352) | In Standalone checkpoint recover mode many jobs with same checkpoint interval cause IO pressure |  Major | Runtime / State Backends | vinoyang | vinoyang |
| [FLINK-9470](https://issues.apache.org/jira/browse/FLINK-9470) | Allow querying the key in KeyedProcessFunction |  Major | API / DataStream | Aljoscha Krettek | Aljoscha Krettek |
| [FLINK-9730](https://issues.apache.org/jira/browse/FLINK-9730) | avoid access static via class reference |  Major | . | lamber-ken | lamber-ken |
| [FLINK-9768](https://issues.apache.org/jira/browse/FLINK-9768) | Only build flink-dist for binary releases |  Major | Release System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9687](https://issues.apache.org/jira/browse/FLINK-9687) | Delay the state fetch only when the triggerResult is fire |  Major | API / DataStream | Aitozi | Aitozi |
| [FLINK-9809](https://issues.apache.org/jira/browse/FLINK-9809) | Support setting CoLocation constraints on the DataStream Transformations |  Major | . | Stephan Ewen | Stephan Ewen |
| [FLINK-9785](https://issues.apache.org/jira/browse/FLINK-9785) | Add remote addresses to LocalTransportException instances |  Major | Runtime / Network | Nico Kruber | Nico Kruber |
| [FLINK-9804](https://issues.apache.org/jira/browse/FLINK-9804) | KeyedStateBackend.getKeys() does not work on RocksDB MapState |  Blocker | Runtime / State Backends | Aljoscha Krettek | Sihua Zhou |
| [FLINK-9801](https://issues.apache.org/jira/browse/FLINK-9801) | flink-dist is missing dependency on flink-examples |  Major | Build System, Examples | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9619](https://issues.apache.org/jira/browse/FLINK-9619) | Always close the task manager connection when the container is completed in YarnResourceManager |  Major | Deployment / YARN | Sihua Zhou | Sihua Zhou |
| [FLINK-9821](https://issues.apache.org/jira/browse/FLINK-9821) | Let dynamic properties overwrite configuration settings in TaskManagerRunner |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9820](https://issues.apache.org/jira/browse/FLINK-9820) | Let dynamic properties overwrite configuration settings in ClusterEntrypoint |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9818](https://issues.apache.org/jira/browse/FLINK-9818) | Add cluster component command line parser |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9483](https://issues.apache.org/jira/browse/FLINK-9483) | "Building Flink" doc doesn't highlight quick build command |  Minor | Documentation | Bowen Li | Bowen Li |
| [FLINK-9692](https://issues.apache.org/jira/browse/FLINK-9692) | Adapt maxRecords parameter in the getRecords call to optimize bytes read from Kinesis |  Major | Connectors / Kinesis | Lakshmi Rao | Lakshmi Rao |
| [FLINK-9276](https://issues.apache.org/jira/browse/FLINK-9276) | Improve error message when TaskManager fails |  Critical | Runtime / Coordination | Stephan Ewen | vinoyang |
| [FLINK-9881](https://issues.apache.org/jira/browse/FLINK-9881) | Typo in a function name in table.scala |  Major | Table SQL / API | Ashwin Sinha | Ashwin Sinha |
| [FLINK-9811](https://issues.apache.org/jira/browse/FLINK-9811) | Add ITCase for interactions of Jar handlers |  Major | Runtime / Coordination, Runtime / REST, Runtime / Web Frontend | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9871](https://issues.apache.org/jira/browse/FLINK-9871) | Use Description class for ConfigOptions with rich formatting |  Major | Documentation | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9435](https://issues.apache.org/jira/browse/FLINK-9435) | Remove per-key selection Tuple instantiation via reflection in ComparableKeySelector and ArrayKeySelector |  Major | . | Nico Kruber | Nico Kruber |
| [FLINK-7251](https://issues.apache.org/jira/browse/FLINK-7251) | Merge the flink-java8 project into flink-core |  Major | Build System | Stephan Ewen | Timo Walther |
| [FLINK-9886](https://issues.apache.org/jira/browse/FLINK-9886) | Build SQL jars with every build |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9895](https://issues.apache.org/jira/browse/FLINK-9895) | Ensure correct logging settings for NettyLeakDetectionResource |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9873](https://issues.apache.org/jira/browse/FLINK-9873) | Log actual state when aborting checkpoint due to task not running |  Major | Runtime / State Backends | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9748](https://issues.apache.org/jira/browse/FLINK-9748) | create\_source\_release pollutes flink root directory |  Major | Release System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-7565](https://issues.apache.org/jira/browse/FLINK-7565) | Add support for HTTP 1.1 (Chunked transfer encoding) to Flink web UI |  Major | Runtime / Web Frontend | Robert Metzger |  |
| [FLINK-9888](https://issues.apache.org/jira/browse/FLINK-9888) | Remove unsafe defaults from release scripts |  Major | Release System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9909](https://issues.apache.org/jira/browse/FLINK-9909) | Remove cancellation of input futures from ConjunctFutures |  Major | . | Till Rohrmann | Till Rohrmann |
| [FLINK-9704](https://issues.apache.org/jira/browse/FLINK-9704) | QueryableState E2E test failed on travis |  Major | Runtime / Queryable State, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9765](https://issues.apache.org/jira/browse/FLINK-9765) | Improve CLI responsiveness when cluster is not reachable |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-6222](https://issues.apache.org/jira/browse/FLINK-6222) | YARN: setting environment variables in an easier fashion |  Major | Deployment / Scripts | Craig Foster | Dawid Wysakowicz |
| [FLINK-9806](https://issues.apache.org/jira/browse/FLINK-9806) | Add a canonical link element to documentation HTML |  Major | Documentation | Patrick Lucas | Patrick Lucas |
| [FLINK-9942](https://issues.apache.org/jira/browse/FLINK-9942) | Guard handlers against null fields in requests |  Major | Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8439](https://issues.apache.org/jira/browse/FLINK-8439) | Add Flink shading to AWS credential provider s3 hadoop config |  Critical | Documentation | Dyana Rose | Andrey Zagrebin |
| [FLINK-9987](https://issues.apache.org/jira/browse/FLINK-9987) | Rework ClassLoader E2E test to not rely on .version.properties file |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9986](https://issues.apache.org/jira/browse/FLINK-9986) | Remove unnecessary information from .version.properties file |  Major | Build System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-7386](https://issues.apache.org/jira/browse/FLINK-7386) | Flink Elasticsearch 5 connector is not compatible with Elasticsearch 5.2+ client |  Critical | Connectors / ElasticSearch | Dawid Wysakowicz | Fang Yong |
| [FLINK-9897](https://issues.apache.org/jira/browse/FLINK-9897) | Further enhance adaptive reads in Kinesis Connector to depend on run loop time |  Major | Connectors / Kinesis | Lakshmi Rao | Lakshmi Rao |
| [FLINK-10016](https://issues.apache.org/jira/browse/FLINK-10016) | Make YARN/Kerberos end-to-end test stricter |  Major | Tests | Aljoscha Krettek | Aljoscha Krettek |
| [FLINK-9947](https://issues.apache.org/jira/browse/FLINK-9947) | Document unified table sources/sinks/formats |  Major | Documentation, Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9944](https://issues.apache.org/jira/browse/FLINK-9944) | Cleanup end-to-end test poms |  Major | Build System, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8192](https://issues.apache.org/jira/browse/FLINK-8192) | Properly annotate APIs of all Flink connectors with @Public / @PublicEvolving / @Internal |  Major | Connectors / Common | Tzu-Li (Gordon) Tai |  |
| [FLINK-9691](https://issues.apache.org/jira/browse/FLINK-9691) | Modify run loop in Kinesis ShardConsumer to not sleep for a fixed fetchIntervalMillis |  Major | Connectors / Kinesis | Lakshmi Rao | Jamie Grier |
| [FLINK-9938](https://issues.apache.org/jira/browse/FLINK-9938) | State TTL cleanup of full state snapshot upon checkpointing |  Major | Runtime / State Backends | Andrey Zagrebin | Andrey Zagrebin |
| [FLINK-9438](https://issues.apache.org/jira/browse/FLINK-9438) | Add documentation for (Registry)AvroDeserializationSchema |  Critical | Documentation | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9976](https://issues.apache.org/jira/browse/FLINK-9976) | Odd signatures for streaming file sink format builders |  Major | Connectors / Common | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9792](https://issues.apache.org/jira/browse/FLINK-9792) | Cannot add html tags in options description |  Major | Documentation | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9776](https://issues.apache.org/jira/browse/FLINK-9776) | Interrupt TaskThread only while in User/Operator code |  Major | Runtime / Task | Stephan Ewen | Stephan Ewen |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-9269](https://issues.apache.org/jira/browse/FLINK-9269) | Concurrency problem in HeapKeyedStateBackend when performing checkpoint async |  Critical | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-9174](https://issues.apache.org/jira/browse/FLINK-9174) | The type of state created in ProccessWindowFunction.proccess() is inconsistency |  Major | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-9373](https://issues.apache.org/jira/browse/FLINK-9373) | Fix potential data losing for RocksDBBackend |  Blocker | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-8836](https://issues.apache.org/jira/browse/FLINK-8836) | Duplicating a KryoSerializer does not duplicate registered default serializers |  Blocker | API / Type Serialization System | Tzu-Li (Gordon) Tai | Stefan Richter |
| [FLINK-9384](https://issues.apache.org/jira/browse/FLINK-9384) | KafkaAvroTableSource failed to work due to type mismatch |  Blocker | Connectors / Kafka, Table SQL / API | Jun Zhang |  |
| [FLINK-9258](https://issues.apache.org/jira/browse/FLINK-9258) | ConcurrentModificationException in ComponentMetricGroup.getAllVariables |  Major | Runtime / Metrics | Narayanan Arunachalam | Chesnay Schepler |
| [FLINK-9326](https://issues.apache.org/jira/browse/FLINK-9326) | TaskManagerOptions.NUM\_TASK\_SLOTS does not work for local/embedded mode |  Major | . | Samuel Doyle | vinoyang |
| [FLINK-9370](https://issues.apache.org/jira/browse/FLINK-9370) | Activate distributed cache end-to-end test |  Critical | Runtime / Task, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9215](https://issues.apache.org/jira/browse/FLINK-9215) | TaskManager Releasing  - org.apache.flink.util.FlinkException |  Major | Runtime / Coordination | Bob Lau | Sihua Zhou |
| [FLINK-9440](https://issues.apache.org/jira/browse/FLINK-9440) | Allow cancelation and reset of timers |  Major | . | Elias Levy | Stefan Richter |
| [FLINK-7917](https://issues.apache.org/jira/browse/FLINK-7917) | The return of taskInformationOrBlobKey should be placed inside synchronized in ExecutionJobVertex |  Minor | Runtime / Task | Ted Yu | vinoyang |
| [FLINK-9398](https://issues.apache.org/jira/browse/FLINK-9398) | Flink CLI list running job returns all jobs except in CREATE state |  Major | Command Line Client | Rong Rong | Rong Rong |
| [FLINK-8946](https://issues.apache.org/jira/browse/FLINK-8946) | TaskManager stop sending metrics after JobManager failover |  Critical | Runtime / Coordination, Runtime / Metrics | Truong Duc Kien | vinoyang |
| [FLINK-9458](https://issues.apache.org/jira/browse/FLINK-9458) | Unable to recover from job failure on YARN with NPE |  Blocker | . | Truong Duc Kien | Till Rohrmann |
| [FLINK-9463](https://issues.apache.org/jira/browse/FLINK-9463) | Setting taskmanager.network.netty.transport to epoll |  Major | Runtime / Network | Piotr Nowojski | Piotr Nowojski |
| [FLINK-9570](https://issues.apache.org/jira/browse/FLINK-9570) | SQL Client merging environments uses AbstractMap |  Major | . | Dominik Wosiński | Dominik Wosiński |
| [FLINK-8725](https://issues.apache.org/jira/browse/FLINK-8725) | Separate NFA-state from NFA in CEP library |  Major | Library / CEP | Aljoscha Krettek | Aljoscha Krettek |
| [FLINK-9494](https://issues.apache.org/jira/browse/FLINK-9494) | Race condition in Dispatcher with concurrent granting and revoking of leaderhship |  Critical | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9530](https://issues.apache.org/jira/browse/FLINK-9530) | Task numRecords metrics broken for chains |  Blocker | Runtime / Metrics | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9257](https://issues.apache.org/jira/browse/FLINK-9257) | End-to-end tests prints "All tests PASS" even if individual test-script returns non-zero exit code |  Critical | Tests | Florian Schmidt | Florian Schmidt |
| [FLINK-9589](https://issues.apache.org/jira/browse/FLINK-9589) | PythonOperationInfo should be immutable |  Major | API / Python | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9590](https://issues.apache.org/jira/browse/FLINK-9590) | HistogramDump should be immutable |  Trivial | Runtime / Metrics | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9591](https://issues.apache.org/jira/browse/FLINK-9591) | Remove remnants of distributed-cache logic |  Major | API / Python | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9468](https://issues.apache.org/jira/browse/FLINK-9468) | Wrong calculation of outputLimit in LimitedConnectionsFileSystem |  Critical | FileSystems | Sihua Zhou | Sihua Zhou |
| [FLINK-9366](https://issues.apache.org/jira/browse/FLINK-9366) | Distribute Cache only works for client-accessible files |  Blocker | Command Line Client, Runtime / Task | Chesnay Schepler | Dawid Wysakowicz |
| [FLINK-9601](https://issues.apache.org/jira/browse/FLINK-9601) | Snapshot of CopyOnWriteStateTable will failed when the amount of record is more than MAXIMUM\_CAPACITY |  Major | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-9467](https://issues.apache.org/jira/browse/FLINK-9467) | No Watermark display on Web UI |  Blocker | Runtime / Metrics, Runtime / Web Frontend | Truong Duc Kien | Chesnay Schepler |
| [FLINK-8795](https://issues.apache.org/jira/browse/FLINK-8795) | Scala shell broken for Flip6 |  Blocker | Scala Shell | kant kodali | Dawid Wysakowicz |
| [FLINK-9374](https://issues.apache.org/jira/browse/FLINK-9374) | Flink Kinesis Producer does not backpressure |  Critical | Connectors / Kinesis | Franz Thoma | Franz Thoma |
| [FLINK-9500](https://issues.apache.org/jira/browse/FLINK-9500) | FileUploadHandler does not handle EmptyLastHttpContent |  Major | Command Line Client, Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9493](https://issues.apache.org/jira/browse/FLINK-9493) | Forward exception when releasing a TaskManager at the SlotPool |  Critical | Runtime / Coordination | Till Rohrmann | Andrey Zagrebin |
| [FLINK-9585](https://issues.apache.org/jira/browse/FLINK-9585) | Logger in ZooKeeperStateHandleStore is public and non-final |  Trivial | Runtime / Task | Chesnay Schepler | vinoyang |
| [FLINK-9634](https://issues.apache.org/jira/browse/FLINK-9634) | Deactivate previous location based scheduling if local recovery is disabled |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9524](https://issues.apache.org/jira/browse/FLINK-9524) | NPE from ProcTimeBoundedRangeOver.scala |  Major | Table SQL / API | yan zhou | yan zhou |
| [FLINK-9629](https://issues.apache.org/jira/browse/FLINK-9629) | Datadog metrics reporter does not have shaded dependencies |  Major | Runtime / Metrics | Georgii Gobozov | Georgii Gobozov |
| [FLINK-8067](https://issues.apache.org/jira/browse/FLINK-8067) | User code ClassLoader not set before calling ProcessingTimeCallback |  Minor | . | Gary Yao | vinoyang |
| [FLINK-9627](https://issues.apache.org/jira/browse/FLINK-9627) | Extending 'KafkaJsonTableSource' according to comments will result in NPE |  Major | . | Dominik Wosiński | vinoyang |
| [FLINK-9532](https://issues.apache.org/jira/browse/FLINK-9532) | Flink Overview of Jobs Documentation Incorrect |  Trivial | Documentation | Abdul Qadeer | vinoyang |
| [FLINK-9684](https://issues.apache.org/jira/browse/FLINK-9684) | HistoryServerArchiveFetcher not working properly with secure hdfs cluster |  Major | Runtime / Coordination | Ethan Li | Ethan Li |
| [FLINK-9580](https://issues.apache.org/jira/browse/FLINK-9580) | Potentially unclosed ByteBufInputStream in RestClient#readRawResponse |  Minor | Runtime / REST | Ted Yu | vinoyang |
| [FLINK-9677](https://issues.apache.org/jira/browse/FLINK-9677) | RestClient fails for large uploads |  Major | Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9665](https://issues.apache.org/jira/browse/FLINK-9665) | PrometheusReporter does not properly unregister metrics |  Major | Runtime / Metrics | Chesnay Schepler | Jelmer Kuperus |
| [FLINK-9444](https://issues.apache.org/jira/browse/FLINK-9444) | Add full SQL support for Avro formats |  Blocker | Connectors / Kafka, Table SQL / API | Jun Zhang | Jun Zhang |
| [FLINK-8785](https://issues.apache.org/jira/browse/FLINK-8785) | JobSubmitHandler does not handle JobSubmissionExceptions |  Blocker | Runtime / Coordination, Runtime / REST | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9708](https://issues.apache.org/jira/browse/FLINK-9708) | Network buffer leaks when buffer request fails during buffer redistribution |  Major | Runtime / Network | Nico Kruber | Nico Kruber |
| [FLINK-9636](https://issues.apache.org/jira/browse/FLINK-9636) | Network buffer leaks in requesting a batch of segments during canceling |  Major | Runtime / Network | Zhijiang | Nico Kruber |
| [FLINK-9633](https://issues.apache.org/jira/browse/FLINK-9633) | Flink doesn't use the Savepoint path's filesystem to create the OuptutStream on Task. |  Critical | Runtime / State Backends | Sihua Zhou | Sihua Zhou |
| [FLINK-9654](https://issues.apache.org/jira/browse/FLINK-9654) | Internal error while deserializing custom Scala TypeSerializer instances |  Major | . | Zsolt Donca | Zsolt Donca |
| [FLINK-9622](https://issues.apache.org/jira/browse/FLINK-9622) | DistributedCacheDfsTest failed on travis |  Blocker | Tests | Sihua Zhou | Till Rohrmann |
| [FLINK-9554](https://issues.apache.org/jira/browse/FLINK-9554) | flink scala shell doesn't work in yarn mode |  Blocker | Scala Shell | Jeff Zhang | Jeff Zhang |
| [FLINK-9676](https://issues.apache.org/jira/browse/FLINK-9676) | Deadlock during canceling task and recycling exclusive buffer |  Critical | Runtime / Network | Zhijiang | Nico Kruber |
| [FLINK-9581](https://issues.apache.org/jira/browse/FLINK-9581) | Redundant spaces for Collect at sql.md |  Trivial | Documentation, Table SQL / API | Sergey Nuyanzin | Sergey Nuyanzin |
| [FLINK-9769](https://issues.apache.org/jira/browse/FLINK-9769) | FileUploads may be shared across requests |  Blocker | Runtime / Coordination, Runtime / REST, Runtime / Web Frontend | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9770](https://issues.apache.org/jira/browse/FLINK-9770) | UI jar list broken |  Blocker | Runtime / Coordination, Runtime / REST, Runtime / Web Frontend | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9772](https://issues.apache.org/jira/browse/FLINK-9772) | Documentation of Hadoop API outdated |  Minor | Documentation | Lorenz Bühmann | vinoyang |
| [FLINK-8161](https://issues.apache.org/jira/browse/FLINK-8161) | Flakey YARNSessionCapacitySchedulerITCase on Travis |  Critical | Deployment / YARN, Tests | Till Rohrmann | Till Rohrmann |
| [FLINK-9789](https://issues.apache.org/jira/browse/FLINK-9789) | Watermark metrics for an operator&task shadow each other |  Blocker | Runtime / Metrics | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9743](https://issues.apache.org/jira/browse/FLINK-9743) | PackagedProgram.extractContainedLibraries fails on Windows |  Major | Command Line Client, Runtime / Coordination | Chesnay Schepler | Sergey Nuyanzin |
| [FLINK-9584](https://issues.apache.org/jira/browse/FLINK-9584) | Unclosed streams in Bucketing-/RollingSink |  Major | Connectors / FileSystem | Chesnay Schepler | Sihua Zhou |
| [FLINK-9754](https://issues.apache.org/jira/browse/FLINK-9754) | Release scripts refers to non-existing profile |  Major | Release System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-5363](https://issues.apache.org/jira/browse/FLINK-5363) | Fire timers when window state is currently empty |  Major | API / DataStream | Aljoscha Krettek | Aitozi |
| [FLINK-9706](https://issues.apache.org/jira/browse/FLINK-9706) | DispatcherTest#testSubmittedJobGraphListener fails on Travis |  Critical | Runtime / Coordination, Tests | Chesnay Schepler | Till Rohrmann |
| [FLINK-9439](https://issues.apache.org/jira/browse/FLINK-9439) | DispatcherTest#testJobRecovery dead locks |  Critical | Runtime / Coordination | Piotr Nowojski | Till Rohrmann |
| [FLINK-9766](https://issues.apache.org/jira/browse/FLINK-9766) | Incomplete/incorrect cleanup in RemoteInputChannelTest |  Major | Runtime / Network, Tests | Nico Kruber | Nico Kruber |
| [FLINK-9784](https://issues.apache.org/jira/browse/FLINK-9784) | Inconsistent use of 'static' in AsyncIOExample.java |  Minor | Examples | Alexei Nekrassov | Alexei Nekrassov |
| [FLINK-9603](https://issues.apache.org/jira/browse/FLINK-9603) | Incorrect indexing of part files, when part suffix is specified (FileAlreadyExistsException) |  Major | Connectors / FileSystem | Rinat Sharipov | Kostas Kloudas |
| [FLINK-9810](https://issues.apache.org/jira/browse/FLINK-9810) | JarListHandler does not close opened jars |  Major | Runtime / REST, Runtime / Web Frontend | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9771](https://issues.apache.org/jira/browse/FLINK-9771) |  "Show Plan" option under Submit New Job in WebUI not working |  Major | Runtime / Coordination, Runtime / Web Frontend | Yazdan Shirvany | Chesnay Schepler |
| [FLINK-9091](https://issues.apache.org/jira/browse/FLINK-9091) | Failure while enforcing releasability in building flink-json module |  Major | Build System | Ted Yu | Hai Zhou |
| [FLINK-9703](https://issues.apache.org/jira/browse/FLINK-9703) | Mesos does not expose TM Prometheus port |  Major | Deployment / Mesos | Rune Skou Larsen | Rune Skou Larsen |
| [FLINK-9143](https://issues.apache.org/jira/browse/FLINK-9143) | Restart strategy defined in flink-conf.yaml is ignored |  Major | Runtime / Configuration | Alex Smirnov | Dawid Wysakowicz |
| [FLINK-9758](https://issues.apache.org/jira/browse/FLINK-9758) | ContinuousFileProcessingTest failed due to not setting runtimeContext |  Minor | API / DataStream, Tests | Yun Tang | Yun Tang |
| [FLINK-8544](https://issues.apache.org/jira/browse/FLINK-8544) | JSONKeyValueDeserializationSchema throws NPE when message key is null |  Major | Connectors / Kafka | Bill Lee |  |
| [FLINK-8731](https://issues.apache.org/jira/browse/FLINK-8731) | TwoInputStreamTaskTest flaky on travis |  Critical | Tests | Chesnay Schepler | Dawid Wysakowicz |
| [FLINK-9847](https://issues.apache.org/jira/browse/FLINK-9847) | OneInputStreamTaskTest.testWatermarksNotForwardedWithinChainWhenIdle unstable |  Critical | Tests | Till Rohrmann |  |
| [FLINK-9380](https://issues.apache.org/jira/browse/FLINK-9380) | Failing end-to-end tests should not clean up logs |  Critical | Tests | Till Rohrmann | Deepak Sharma |
| [FLINK-9842](https://issues.apache.org/jira/browse/FLINK-9842) | Job submission fails via CLI with SSL enabled |  Blocker | Command Line Client, Runtime / Coordination | Nico Kruber | Chesnay Schepler |
| [FLINK-9857](https://issues.apache.org/jira/browse/FLINK-9857) | Processing-time timers fire too early |  Blocker | API / DataStream | Aljoscha Krettek | Aljoscha Krettek |
| [FLINK-9865](https://issues.apache.org/jira/browse/FLINK-9865) | flink-hadoop-compatibility should assume Hadoop as provided |  Major | Build System | Stephan Ewen | Stephan Ewen |
| [FLINK-9880](https://issues.apache.org/jira/browse/FLINK-9880) | Incorrect argument order calling BucketerContext#update |  Major | Connectors / FileSystem | Ted Yu | Kostas Kloudas |
| [FLINK-9777](https://issues.apache.org/jira/browse/FLINK-9777) | YARN: JM and TM Memory must be specified with Units |  Blocker | Deployment / YARN, Documentation | Gary Yao | vinoyang |
| [FLINK-9658](https://issues.apache.org/jira/browse/FLINK-9658) | Test data output directories are no longer cleaned up |  Major | Tests | Chesnay Schepler | zhangminglei |
| [FLINK-9866](https://issues.apache.org/jira/browse/FLINK-9866) | Allow passing program arguments to StandaloneJobCluster |  Major | Runtime / Coordination | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-9575](https://issues.apache.org/jira/browse/FLINK-9575) | Potential race condition when removing JobGraph in HA |  Critical | . | Dominik Wosiński | Dominik Wosiński |
| [FLINK-9872](https://issues.apache.org/jira/browse/FLINK-9872) | SavepointITCase#testSavepointForJobWithIteration does not properly cancel jobs |  Minor | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9815](https://issues.apache.org/jira/browse/FLINK-9815) | YARNSessionCapacitySchedulerITCase flaky |  Blocker | . | Dawid Wysakowicz | Chesnay Schepler |
| [FLINK-9762](https://issues.apache.org/jira/browse/FLINK-9762) | CoreOptions.TMP\_DIRS wrongly managed on Yarn |  Major | Deployment / YARN | Oleksandr Nitavskyi | Oleksandr Nitavskyi |
| [FLINK-9860](https://issues.apache.org/jira/browse/FLINK-9860) | Netty resource leak on receiver side |  Blocker | Runtime / Network | Till Rohrmann | Nico Kruber |
| [FLINK-9755](https://issues.apache.org/jira/browse/FLINK-9755) | Exceptions in RemoteInputChannel#notifyBufferAvailable() are not propagated to the responsible thread |  Critical | Runtime / Network | Nico Kruber | Nico Kruber |
| [FLINK-9841](https://issues.apache.org/jira/browse/FLINK-9841) | Web UI only show partial taskmanager log |  Major | Runtime / REST, Runtime / Web Frontend | vinoyang | vinoyang |
| [FLINK-9793](https://issues.apache.org/jira/browse/FLINK-9793) | When submitting a flink job with yarn-cluster, flink-dist\*.jar is repeatedly uploaded |  Minor | Deployment / YARN | linzhongjun | linzhongjun |
| [FLINK-9911](https://issues.apache.org/jira/browse/FLINK-9911) | SlotPool#failAllocation is called outside of main thread |  Blocker | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9910](https://issues.apache.org/jira/browse/FLINK-9910) | Non-queued scheduling failure sometimes does not return the slot |  Blocker | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9908](https://issues.apache.org/jira/browse/FLINK-9908) | Inconsistent state of SlotPool after ExecutionGraph cancellation |  Blocker | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-9838](https://issues.apache.org/jira/browse/FLINK-9838) | Slot request failed Exceptions after completing a job |  Major | Runtime / Coordination | Nico Kruber | Till Rohrmann |
| [FLINK-9892](https://issues.apache.org/jira/browse/FLINK-9892) | Disable local recovery in Jepsen tests |  Major | Tests | Gary Yao | Gary Yao |
| [FLINK-9906](https://issues.apache.org/jira/browse/FLINK-9906) | Flink Job not running with no resource |  Major | Runtime / Coordination | Godfrey He |  |
| [FLINK-5750](https://issues.apache.org/jira/browse/FLINK-5750) | Incorrect translation of n-ary Union |  Critical | Table SQL / API | Anton Mushin | Alexander Koltsov |
| [FLINK-9934](https://issues.apache.org/jira/browse/FLINK-9934) | Kafka table source factory produces invalid field mapping |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9949](https://issues.apache.org/jira/browse/FLINK-9949) | Jepsen: Kill Flink processes when tearing down cluster |  Critical | Tests | Gary Yao | Gary Yao |
| [FLINK-9939](https://issues.apache.org/jira/browse/FLINK-9939) | Mesos: Not setting TMP dirs causes NPE |  Blocker | Deployment / Mesos | Gary Yao | Gary Yao |
| [FLINK-9994](https://issues.apache.org/jira/browse/FLINK-9994) | IntervalJoinOperator#Context#getTimestamp does not return the Max timestamp. |  Major | API / DataStream | Kostas Kloudas | Kostas Kloudas |
| [FLINK-9985](https://issues.apache.org/jira/browse/FLINK-9985) | Incorrect parameter order in document |  Major | Documentation | zhangminglei | zhangminglei |
| [FLINK-9996](https://issues.apache.org/jira/browse/FLINK-9996) | PrestoS3FileSystemITCase#testConfigKeysForwarding fails on travis |  Major | FileSystems, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9923](https://issues.apache.org/jira/browse/FLINK-9923) | OneInputStreamTaskTest.testWatermarkMetrics fails on Travis |  Critical | Tests | Till Rohrmann | Till Rohrmann |
| [FLINK-9159](https://issues.apache.org/jira/browse/FLINK-9159) | Sanity check default timeout values |  Blocker | Runtime / Coordination | Till Rohrmann | Gary Yao |
| [FLINK-9978](https://issues.apache.org/jira/browse/FLINK-9978) | Source release sha contains absolute file path |  Major | Release System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9988](https://issues.apache.org/jira/browse/FLINK-9988) |   job manager does not respect property jobmanager.web.address |  Major | . | Pavlo Petrychenko | Chesnay Schepler |
| [FLINK-10005](https://issues.apache.org/jira/browse/FLINK-10005) | StreamingFileSink ignores checkpoint/processing time rolling policies |  Blocker | Connectors / Common | Chesnay Schepler | Kostas Kloudas |
| [FLINK-9874](https://issues.apache.org/jira/browse/FLINK-9874) | set\_conf\_ssl in E2E tests fails on macOS |  Critical | Tests | Florian Schmidt | Florian Schmidt |
| [FLINK-9946](https://issues.apache.org/jira/browse/FLINK-9946) | Quickstart E2E test archetype version is hard-coded |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9694](https://issues.apache.org/jira/browse/FLINK-9694) | Potentially NPE in CompositeTypeSerializerConfigSnapshot constructor |  Minor | Table SQL / API | vinoyang | Piotr Nowojski |
| [FLINK-9655](https://issues.apache.org/jira/browse/FLINK-9655) | Externalized checkpoint E2E test fails on travis |  Major | Runtime / State Backends, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-10021](https://issues.apache.org/jira/browse/FLINK-10021) | All-round E2E tests query metric with wrong operator name |  Major | Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9936](https://issues.apache.org/jira/browse/FLINK-9936) | Mesos resource manager unable to connect to master after failover |  Blocker | Deployment / Mesos, Runtime / Coordination | Renjie Liu | Gary Yao |
| [FLINK-9969](https://issues.apache.org/jira/browse/FLINK-9969) | Unreasonable memory requirements to complete examples/batch/WordCount |  Blocker | Runtime / Coordination | Piotr Nowojski | Till Rohrmann |
| [FLINK-10033](https://issues.apache.org/jira/browse/FLINK-10033) | Let Task release reference to Invokable on shutdown |  Major | Runtime / Coordination | Stephan Ewen | Stephan Ewen |
| [FLINK-9995](https://issues.apache.org/jira/browse/FLINK-9995) | Jepsen: Clean up Mesos Logs and Working Directory |  Major | Tests | Gary Yao | Gary Yao |
| [FLINK-10070](https://issues.apache.org/jira/browse/FLINK-10070) | Flink cannot be compiled with maven 3.0.x |  Major | Build System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-10064](https://issues.apache.org/jira/browse/FLINK-10064) | Fix a typo in ExternalCatalogTable |  Critical | Table SQL / API | Jun Zhang | Jun Zhang |
| [FLINK-10051](https://issues.apache.org/jira/browse/FLINK-10051) | SQL client E2E test is missing dependencies |  Major | Build System, Table SQL / API, Table SQL / Client, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-9576](https://issues.apache.org/jira/browse/FLINK-9576) | Wrong contiguity documentation |  Critical | Documentation, Library / CEP | Dawid Wysakowicz | Dawid Wysakowicz |
| [FLINK-8893](https://issues.apache.org/jira/browse/FLINK-8893) | NPE when netty try to allocate directBuffer |  Blocker | Runtime / Network | Aitozi |  |
| [FLINK-9217](https://issues.apache.org/jira/browse/FLINK-9217) | Kafka010ITCase hanging after timeout in testTimestamps() |  Critical | Connectors / Kafka, Tests | Nico Kruber | Aljoscha Krettek |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-9420](https://issues.apache.org/jira/browse/FLINK-9420) | Add tests for SQL IN sub-query operator in streaming |  Major | Table SQL / API | Timo Walther | Ruidong Li |
| [FLINK-9424](https://issues.apache.org/jira/browse/FLINK-9424) | BlobClientSslTest does not work in all environments |  Major | Runtime / Coordination, Tests | Timo Walther | Stephan Ewen |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-6924](https://issues.apache.org/jira/browse/FLINK-6924) | ADD LOG(X) supported in TableAPI |  Major | Table SQL / API | sunjincheng | Jiayi Liao |
| [FLINK-8537](https://issues.apache.org/jira/browse/FLINK-8537) | Add a Kafka table source factory with Avro format support |  Major | Table SQL / API | Timo Walther | Xingcan Cui |
| [FLINK-8978](https://issues.apache.org/jira/browse/FLINK-8978) | End-to-end test: Job upgrade |  Blocker | Tests | Till Rohrmann | Andrey Zagrebin |
| [FLINK-9181](https://issues.apache.org/jira/browse/FLINK-9181) | Add SQL Client documentation page |  Major | Table SQL / Client | Timo Walther | Timo Walther |
| [FLINK-6926](https://issues.apache.org/jira/browse/FLINK-6926) | Add support for MD5, SHA1 and SHA2 |  Major | Table SQL / API | sunjincheng | Michael Gendelman |
| [FLINK-8910](https://issues.apache.org/jira/browse/FLINK-8910) | Introduce automated end-to-end test for local recovery (including sticky scheduling) |  Blocker | Runtime / State Backends | Stefan Richter | Stefan Richter |
| [FLINK-8428](https://issues.apache.org/jira/browse/FLINK-8428) | Implement stream-stream non-window left outer join |  Major | Table SQL / API | Hequn Cheng | Hequn Cheng |
| [FLINK-8996](https://issues.apache.org/jira/browse/FLINK-8996) | Include an operator with broadcast and union state |  Major | Tests | Stefan Richter | Tzu-Li (Gordon) Tai |
| [FLINK-9322](https://issues.apache.org/jira/browse/FLINK-9322) | Add exception throwing map function that simulates failures to the general purpose DataStream job |  Major | Tests | Tzu-Li (Gordon) Tai | Tzu-Li (Gordon) Tai |
| [FLINK-9320](https://issues.apache.org/jira/browse/FLINK-9320) | Update \`test-ha.sh\` end-to-end test to use general purpose DataStream job |  Critical | Tests | Tzu-Li (Gordon) Tai | Tzu-Li (Gordon) Tai |
| [FLINK-8977](https://issues.apache.org/jira/browse/FLINK-8977) | End-to-end test: Manually resume job after terminal failure |  Blocker | Tests | Till Rohrmann | Tzu-Li (Gordon) Tai |
| [FLINK-8989](https://issues.apache.org/jira/browse/FLINK-8989) | End-to-end test: ElasticSearch connector |  Major | Connectors / ElasticSearch, Tests | Till Rohrmann | zhangminglei |
| [FLINK-9008](https://issues.apache.org/jira/browse/FLINK-9008) | End-to-end test: Quickstarts |  Blocker | Quickstarts, Tests | Till Rohrmann | zhangminglei |
| [FLINK-8429](https://issues.apache.org/jira/browse/FLINK-8429) | Implement stream-stream non-window right outer join |  Major | Table SQL / API | Hequn Cheng | Hequn Cheng |
| [FLINK-9386](https://issues.apache.org/jira/browse/FLINK-9386) | Remove netty-router dependency |  Major | . | Piotr Nowojski | Piotr Nowojski |
| [FLINK-8430](https://issues.apache.org/jira/browse/FLINK-8430) | Implement stream-stream non-window full outer join |  Major | Table SQL / API | Hequn Cheng | Hequn Cheng |
| [FLINK-8861](https://issues.apache.org/jira/browse/FLINK-8861) | Add support for batch queries in SQL Client |  Major | Table SQL / Client | Timo Walther | Xingcan Cui |
| [FLINK-9451](https://issues.apache.org/jira/browse/FLINK-9451) | End-to-end test: Scala Quickstarts |  Blocker | Quickstarts | Yazdan Shirvany | Yazdan Shirvany |
| [FLINK-9368](https://issues.apache.org/jira/browse/FLINK-9368) | End-to-end test: Python API |  Major | API / Python, Tests | Chesnay Schepler | Chesnay Schepler |
| [FLINK-6939](https://issues.apache.org/jira/browse/FLINK-6939) | Not store IterativeCondition with NFA state |  Major | Library / CEP | Jark Wu | Jark Wu |
| [FLINK-8982](https://issues.apache.org/jira/browse/FLINK-8982) | End-to-end test: Queryable state |  Blocker | Runtime / Queryable State, Tests | Till Rohrmann | Florian Schmidt |
| [FLINK-9394](https://issues.apache.org/jira/browse/FLINK-9394) | Let externalized checkpoint resume e2e also test rescaling |  Major | Tests | Tzu-Li (Gordon) Tai | Tzu-Li (Gordon) Tai |
| [FLINK-8983](https://issues.apache.org/jira/browse/FLINK-8983) | End-to-end test: Confluent schema registry |  Critical | Connectors / Kafka, Tests | Till Rohrmann | Yazdan Shirvany |
| [FLINK-9514](https://issues.apache.org/jira/browse/FLINK-9514) | Create wrapper with TTL logic for value state |  Major | Runtime / State Backends | Andrey Zagrebin | Andrey Zagrebin |
| [FLINK-9516](https://issues.apache.org/jira/browse/FLINK-9516) | Create wrapper with TTL logic for map state |  Major | Runtime / State Backends | Andrey Zagrebin | Andrey Zagrebin |
| [FLINK-8863](https://issues.apache.org/jira/browse/FLINK-8863) | Add user-defined function support in SQL Client |  Major | Table SQL / Client | Timo Walther | Xingcan Cui |
| [FLINK-9563](https://issues.apache.org/jira/browse/FLINK-9563) | Migrate integration tests for CEP |  Minor | . | Deepak Sharma | Deepak Sharma |
| [FLINK-9701](https://issues.apache.org/jira/browse/FLINK-9701) | Activate TTL in state descriptors |  Major | Runtime / State Backends | Andrey Zagrebin | Andrey Zagrebin |
| [FLINK-9488](https://issues.apache.org/jira/browse/FLINK-9488) | Create common entry point for master and workers |  Major | Runtime / Coordination | Till Rohrmann | Till Rohrmann |
| [FLINK-8858](https://issues.apache.org/jira/browse/FLINK-8858) | Add support for INSERT INTO in SQL Client |  Major | Table SQL / Client | Renjie Liu | Timo Walther |
| [FLINK-9751](https://issues.apache.org/jira/browse/FLINK-9751) | Add a RecoverableWriter to the FileSystem abstraction |  Major | Connectors / Common | Stephan Ewen | Stephan Ewen |
| [FLINK-9314](https://issues.apache.org/jira/browse/FLINK-9314) | Enable SSL mutual authentication for Netty / TaskManagers |  Major | Runtime / Coordination | Stephan Ewen | Stephan Ewen |
| [FLINK-9313](https://issues.apache.org/jira/browse/FLINK-9313) | Enable mutual authentication for RPC (akka) |  Major | Runtime / Coordination | Stephan Ewen | Stephan Ewen |
| [FLINK-9004](https://issues.apache.org/jira/browse/FLINK-9004) | Cluster test: Run general purpose job with failures with Yarn session |  Blocker | Tests | Till Rohrmann | Gary Yao |
| [FLINK-9006](https://issues.apache.org/jira/browse/FLINK-9006) | Cluster test: Run general purpose job with failures with Yarn and per-job mode |  Blocker | Deployment / YARN, Tests | Till Rohrmann | Gary Yao |
| [FLINK-9005](https://issues.apache.org/jira/browse/FLINK-9005) | Cluster test: Run general purpose job with failures with Mesos |  Blocker | Deployment / Mesos, Tests | Till Rohrmann | Gary Yao |
| [FLINK-9839](https://issues.apache.org/jira/browse/FLINK-9839) | End-to-end test: Streaming job with SSL |  Blocker | Tests | Nico Kruber | Nico Kruber |
| [FLINK-9750](https://issues.apache.org/jira/browse/FLINK-9750) | Create new StreamingFileSink that works on Flink's FileSystem abstraction |  Major | Connectors / Common | Stephan Ewen | Kostas Kloudas |
| [FLINK-9903](https://issues.apache.org/jira/browse/FLINK-9903) | Add support for bulk writers. |  Major | Connectors / FileSystem | Kostas Kloudas | Kostas Kloudas |
| [FLINK-9753](https://issues.apache.org/jira/browse/FLINK-9753) | Support Parquet for StreamingFileSink |  Major | Connectors / Common | Stephan Ewen | Kostas Kloudas |
| [FLINK-9921](https://issues.apache.org/jira/browse/FLINK-9921) | Update the rolling policy interface. |  Major | Connectors / FileSystem | Kostas Kloudas | Kostas Kloudas |
| [FLINK-9862](https://issues.apache.org/jira/browse/FLINK-9862) | Update end-to-end test to use RocksDB backed timers |  Blocker | Runtime / State Backends | Till Rohrmann | Tzu-Li (Gordon) Tai |
| [FLINK-9296](https://issues.apache.org/jira/browse/FLINK-9296) | Support distinct aggregation on non-windowed grouped streaming tables |  Blocker | Table SQL / API | Fabian Hueske | Fabian Hueske |
| [FLINK-9353](https://issues.apache.org/jira/browse/FLINK-9353) | End-to-end test: Kubernetes integration |  Blocker | Tests | Aljoscha Krettek | Dawid Wysakowicz |
| [FLINK-8981](https://issues.apache.org/jira/browse/FLINK-8981) | Add end-to-end test for running on YARN with Kerberos |  Blocker | Deployment / YARN, Tests | Till Rohrmann | Aljoscha Krettek |
| [FLINK-9951](https://issues.apache.org/jira/browse/FLINK-9951) | Update scm developerConnection |  Major | Build System | Chesnay Schepler | Chesnay Schepler |
| [FLINK-8974](https://issues.apache.org/jira/browse/FLINK-8974) | End-to-end test: Run general purpose DataSet job with failures in standalone mode |  Blocker | Tests | Till Rohrmann | Tuo Wang |
| [FLINK-8993](https://issues.apache.org/jira/browse/FLINK-8993) | Add a test operator with keyed state that uses Kryo serializer (registered/unregistered/custom) |  Major | Tests | Stefan Richter | Tzu-Li (Gordon) Tai |
| [FLINK-8994](https://issues.apache.org/jira/browse/FLINK-8994) | Add a test operator with keyed state that uses Avro serializer (from schema/by reflection) |  Major | Tests | Stefan Richter | Tzu-Li (Gordon) Tai |
| [FLINK-9790](https://issues.apache.org/jira/browse/FLINK-9790) | Add documentation for UDF in SQL Client |  Major | Table SQL / Client | Timo Walther | Xingcan Cui |
| [FLINK-9877](https://issues.apache.org/jira/browse/FLINK-9877) | Add separate docs page for different join types in DataStream API |  Major | Documentation | Florian Schmidt | Florian Schmidt |
| [FLINK-9885](https://issues.apache.org/jira/browse/FLINK-9885) | End-to-end test: Elasticsearch 6.x connector |  Blocker | Connectors / ElasticSearch, Tests | Tzu-Li (Gordon) Tai | Tzu-Li (Gordon) Tai |
| [FLINK-9979](https://issues.apache.org/jira/browse/FLINK-9979) | Support a custom FlinkKafkaPartitioner for a Kafka table sink factory |  Major | Table SQL / API | Timo Walther | Timo Walther |
| [FLINK-9833](https://issues.apache.org/jira/browse/FLINK-9833) | End-to-end test: SQL Client with unified source/sink/format |  Blocker | Table SQL / API, Table SQL / Client | Timo Walther | Timo Walther |
| [FLINK-10027](https://issues.apache.org/jira/browse/FLINK-10027) | Add logging to the StreamingFileSink |  Major | Connectors / FileSystem | Kostas Kloudas | Kostas Kloudas |
| [FLINK-9861](https://issues.apache.org/jira/browse/FLINK-9861) | Add end-to-end test for reworked BucketingSink |  Blocker | Connectors / Common | Till Rohrmann | Chesnay Schepler |
| [FLINK-8480](https://issues.apache.org/jira/browse/FLINK-8480) | Implement Java API to expose join functionality of TimeBoundedStreamJoinOperator |  Major | . | Florian Schmidt | Florian Schmidt |
| [FLINK-8479](https://issues.apache.org/jira/browse/FLINK-8479) | Implement time-bounded inner join of streams as a TwoInputStreamOperator |  Major | . | Florian Schmidt | Florian Schmidt |
| [FLINK-10029](https://issues.apache.org/jira/browse/FLINK-10029) | Refactor Streaming File Sink for better separation of concerns. |  Major | Connectors / FileSystem | Kostas Kloudas | Kostas Kloudas |
| [FLINK-10071](https://issues.apache.org/jira/browse/FLINK-10071) | Document usage of INSERT INTO in SQL Client |  Major | Documentation, Table SQL / Client | Timo Walther | Timo Walther |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [FLINK-9292](https://issues.apache.org/jira/browse/FLINK-9292) | Remove TypeInfoParser |  Major | . | Stephan Ewen | vinoyang |
| [FLINK-7775](https://issues.apache.org/jira/browse/FLINK-7775) | Remove unreferenced method PermanentBlobCache#getNumberOfCachedJobs |  Minor | Runtime / Task | Ted Yu | vinoyang |
| [FLINK-9926](https://issues.apache.org/jira/browse/FLINK-9926) | Allow for ShardConsumer override in Kinesis consumer |  Minor | Connectors / Kinesis | Thomas Weise | Thomas Weise |


