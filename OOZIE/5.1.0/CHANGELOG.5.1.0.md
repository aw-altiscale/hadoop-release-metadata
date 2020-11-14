
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
# Apache Oozie Changelog

## Release 5.1.0 - 2018-12-19



### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-2339](https://issues.apache.org/jira/browse/OOZIE-2339) | [fluent-job] Minimum Viable Fluent Job API |  Major | client, core, examples, fluent-job, tests | Robert Kanter | Andras Piros |
| [OOZIE-3229](https://issues.apache.org/jira/browse/OOZIE-3229) | [client] [ui] Improved SLA filtering options |  Major | client, ui | Andras Piros | Andras Salamon |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-3222](https://issues.apache.org/jira/browse/OOZIE-3222) | The description for DAG is not accurate in the documentation |  Minor | . | gongchuanjie | gongchuanjie |
| [OOZIE-3232](https://issues.apache.org/jira/browse/OOZIE-3232) | Reduce heap waste by reducing duplicate string count |  Major | core | Misha Dmitriev | Misha Dmitriev |
| [OOZIE-3217](https://issues.apache.org/jira/browse/OOZIE-3217) | Enable definition of admin users using oozie-site.xml |  Minor | . | Peter Orova | Peter Orova |
| [OOZIE-3250](https://issues.apache.org/jira/browse/OOZIE-3250) | Reduce heap waste by reducing duplicate byte[] count |  Major | core | Andras Piros | Andras Piros |
| [OOZIE-3094](https://issues.apache.org/jira/browse/OOZIE-3094) | [Docs] Fix for grammar mistake in DG\_ActionAuthentication.twiki |  Trivial | docs | Artem Ervits | Artem Ervits |
| [OOZIE-1393](https://issues.apache.org/jira/browse/OOZIE-1393) | Allow sending emails via TLS |  Major | . | Kiran Nagasubramanian | Mahesh Balakrishnan |
| [OOZIE-3284](https://issues.apache.org/jira/browse/OOZIE-3284) | Upgrade maven-javadoc-plugin to 3.0.1 |  Minor | build | Kinga Marton | Kinga Marton |
| [OOZIE-3275](https://issues.apache.org/jira/browse/OOZIE-3275) | [docs] Update AG\_Install.twiki with Access Control List documentation |  Major | docs | Andras Piros | Andras Piros |
| [OOZIE-3270](https://issues.apache.org/jira/browse/OOZIE-3270) |  Upgrade Derby to 10.14.1.0 |  Major | . | Gézapeti | Gézapeti |
| [OOZIE-3306](https://issues.apache.org/jira/browse/OOZIE-3306) | Make it possible to override maven dependency plugin version number |  Minor | build | Andras Salamon | Andras Salamon |
| [OOZIE-3332](https://issues.apache.org/jira/browse/OOZIE-3332) | [examples] Spark examples should feature yarn client and cluster modes |  Trivial | examples | Daniel Becker | Daniel Becker |
| [OOZIE-2734](https://issues.apache.org/jira/browse/OOZIE-2734) | [docs] Switch from TWiki to Markdown |  Major | docs | Robert Kanter | Andras Piros |
| [OOZIE-3342](https://issues.apache.org/jira/browse/OOZIE-3342) | [examples] Missing archive tag from Fluent Job examples |  Major | examples | Andras Salamon | Andras Salamon |
| [OOZIE-3347](https://issues.apache.org/jira/browse/OOZIE-3347) | [examples] Fix Fluent Job global example |  Major | fluent-job | Andras Salamon | Andras Salamon |
| [OOZIE-3346](https://issues.apache.org/jira/browse/OOZIE-3346) | [examples] [action] Fix Git example. PrepareActionsHandler should support XML namespace prefixes |  Major | action, examples | Andras Salamon | Andras Piros |
| [OOZIE-3340](https://issues.apache.org/jira/browse/OOZIE-3340) | [fluent-job] Create error handler ACTION only if needed |  Major | fluent-job | Andras Salamon | Kinga Marton |
| [OOZIE-3348](https://issues.apache.org/jira/browse/OOZIE-3348) | [Hive action] Remove dependency hive-contrib |  Major | action | Andras Piros | Kinga Marton |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-3209](https://issues.apache.org/jira/browse/OOZIE-3209) | XML schema error when submitting pyspark example |  Minor | examples | Kinga Marton | Kinga Marton |
| [OOZIE-3134](https://issues.apache.org/jira/browse/OOZIE-3134) | Potential inconsistency between the in-memory SLA map and the Oozie database |  Major | . | Attila Sasvári | Kinga Marton |
| [OOZIE-3192](https://issues.apache.org/jira/browse/OOZIE-3192) | OozieDBCLI does not clean up temporary files |  Major | core | Prabhu Joseph | Prabhu Joseph |
| [OOZIE-2427](https://issues.apache.org/jira/browse/OOZIE-2427) | [Kerberos] Authentication failure for the javascript resources under /ext-2.2 |  Major | security | Gao Zhong Liang | Gao Zhong Liang |
| [OOZIE-2494](https://issues.apache.org/jira/browse/OOZIE-2494) | Cron syntax not handling DST properly |  Blocker | coordinator | Dennis Pallett | Kinga Marton |
| [OOZIE-3225](https://issues.apache.org/jira/browse/OOZIE-3225) | [Kerberos] Webconsole disabled message shown instead of 401 error |  Major | . | Kinga Marton | Kinga Marton |
| [OOZIE-2914](https://issues.apache.org/jira/browse/OOZIE-2914) | Consolidate trim calls |  Major | . | Gézapeti | Jan Hentschel |
| [OOZIE-3219](https://issues.apache.org/jira/browse/OOZIE-3219) | Cannot compile with hadoop 3.1.0 |  Major | core | Artem Ervits | Artem Ervits |
| [OOZIE-3235](https://issues.apache.org/jira/browse/OOZIE-3235) | Upgrade ActiveMQ to 5.15.3 |  Minor | client | Mate Juhasz | Mate Juhasz |
| [OOZIE-3221](https://issues.apache.org/jira/browse/OOZIE-3221) | Rename DEFAULT\_LAUNCHER\_MAX\_ATTEMPS |  Trivial | . | Artem Ervits | Artem Ervits |
| [OOZIE-2826](https://issues.apache.org/jira/browse/OOZIE-2826) | Upgrade joda-time to 2.9.9 |  Minor | workflow | Péter Gergő Barna | Artem Ervits |
| [OOZIE-2883](https://issues.apache.org/jira/browse/OOZIE-2883) | ProxyUserService: invalid configuration error message is misleading |  Major | core | yangfang | yangfang |
| [OOZIE-3185](https://issues.apache.org/jira/browse/OOZIE-3185) | Upgrade org.apache.derby to 10.11.1.1 |  Major | core | PandaMonkey | PandaMonkey |
| [OOZIE-2352](https://issues.apache.org/jira/browse/OOZIE-2352) | Unportable shebang in shell scripts |  Major | scripts | Dmitry Sivachenko | Artem Ervits |
| [OOZIE-3228](https://issues.apache.org/jira/browse/OOZIE-3228) | [Spark action] Can't load properties from spark-defaults.conf |  Major | action | Tang Yan | Andras Piros |
| [OOZIE-3258](https://issues.apache.org/jira/browse/OOZIE-3258) | Surefire should not trim stack traces |  Major | core, tests | Peter Bacsko | Peter Bacsko |
| [OOZIE-3233](https://issues.apache.org/jira/browse/OOZIE-3233) | Remove DST shift from the coordinator job's end time |  Major | coordinator | Kinga Marton | Kinga Marton |
| [OOZIE-3260](https://issues.apache.org/jira/browse/OOZIE-3260) | [sla] Remove stale item above max retries on JPA related errors from in-memory SLA map |  Major | coordinator, core, workflow | Andras Piros | Andras Piros |
| [OOZIE-3278](https://issues.apache.org/jira/browse/OOZIE-3278) | Oozie fails to start with Hadoop 2.6.0 |  Major | . | Kinga Marton | Kinga Marton |
| [OOZIE-3109](https://issues.apache.org/jira/browse/OOZIE-3109) | [log-streaming] Escape HTML-specific characters |  Major | . | Dénes Bodó | Dénes Bodó |
| [OOZIE-3297](https://issues.apache.org/jira/browse/OOZIE-3297) | Retry logic does not handle the exception from BulkJPAExecutor properly |  Critical | core | Peter Bacsko | Andras Piros |
| [OOZIE-2791](https://issues.apache.org/jira/browse/OOZIE-2791) | ShareLib installation may fail on busy Hadoop clusters |  Major | . | Attila Sasvári | Kinga Marton |
| [OOZIE-3208](https://issues.apache.org/jira/browse/OOZIE-3208) | "It should never happen" error messages should be more specific to root cause |  Critical | . | Robert Kanter | Kinga Marton |
| [OOZIE-3309](https://issues.apache.org/jira/browse/OOZIE-3309) | Runtime error during /v2/sla filtering for bundle |  Minor | client | Andras Salamon | Andras Salamon |
| [OOZIE-2829](https://issues.apache.org/jira/browse/OOZIE-2829) | Improve sharelib upload to accept multiple source folders |  Major | tools | Gézapeti | Kinga Marton |
| [OOZIE-3303](https://issues.apache.org/jira/browse/OOZIE-3303) | Oozie UI does not work after Jetty 9.3 upgrade |  Blocker | build, ui | Andras Salamon | Andras Salamon |
| [OOZIE-3156](https://issues.apache.org/jira/browse/OOZIE-3156) | Retry SSH action check when cannot connect to remote host |  Major | action | TIAN XING | TIAN XING |
| [OOZIE-2718](https://issues.apache.org/jira/browse/OOZIE-2718) | Improve -dryrun for bundles |  Major | . | Gézapeti | Andras Salamon |
| [OOZIE-3310](https://issues.apache.org/jira/browse/OOZIE-3310) | SQL error during /v2/sla filtering |  Minor | client | Andras Salamon | Andras Salamon |
| [OOZIE-3193](https://issues.apache.org/jira/browse/OOZIE-3193) | Applications are not killed when submitted via subworkflow |  Major | . | Gézapeti | Kinga Marton |
| [OOZIE-3313](https://issues.apache.org/jira/browse/OOZIE-3313) | Hive example action fails |  Minor | action, workflow | Daniel Becker | Daniel Becker |
| [OOZIE-3178](https://issues.apache.org/jira/browse/OOZIE-3178) | ./bin/mkdistro.sh -Papache-release fails due to javadoc errors |  Blocker | build | Gézapeti | Kinga Marton |
| [OOZIE-3315](https://issues.apache.org/jira/browse/OOZIE-3315) | DateList example fails |  Minor | examples | Daniel Becker | Daniel Becker |
| [OOZIE-3321](https://issues.apache.org/jira/browse/OOZIE-3321) | PySpark example fails |  Minor | examples | Daniel Becker | Daniel Becker |
| [OOZIE-3314](https://issues.apache.org/jira/browse/OOZIE-3314) | Remove findbugs-filter.xml and convert its contents to annotations |  Major | core | Peter Bacsko | Andras Salamon |
| [OOZIE-3304](https://issues.apache.org/jira/browse/OOZIE-3304) | Parsing sharelib timestamps is not threadsafe |  Critical | core | Dénes Bodó | Dénes Bodó |
| [OOZIE-3324](https://issues.apache.org/jira/browse/OOZIE-3324) | Cannot compile with findbugs check |  Critical | . | Andras Salamon | Andras Salamon |
| [OOZIE-3330](https://issues.apache.org/jira/browse/OOZIE-3330) | [spark-action] Remove double quotes inside plain option values |  Major | action | Andras Piros | Andras Salamon |
| [OOZIE-3316](https://issues.apache.org/jira/browse/OOZIE-3316) | Fix precommit script |  Major | scripts | Kinga Marton | Kinga Marton |
| [OOZIE-2684](https://issues.apache.org/jira/browse/OOZIE-2684) | Bad database schema error for WF\_ACTIONS table |  Blocker | core | Abhishek Bafna | Kinga Marton |
| [OOZIE-3210](https://issues.apache.org/jira/browse/OOZIE-3210) | [build] Revision information is empty |  Major | . | Artem Ervits | Andras Salamon |
| [OOZIE-3334](https://issues.apache.org/jira/browse/OOZIE-3334) | Don't use org.apache.hadoop.hbase.security.User in HDFSCredentials |  Major | . | Gézapeti | Gézapeti |
| [OOZIE-3155](https://issues.apache.org/jira/browse/OOZIE-3155) | [ui] Job DAG is not refreshed when a job is finished |  Critical | client | Kinga Marton | Andras Salamon |
| [OOZIE-3061](https://issues.apache.org/jira/browse/OOZIE-3061) | Kill only those child jobs which are not already killed |  Trivial | . | Satish Saley | Mate Juhasz |
| [OOZIE-3298](https://issues.apache.org/jira/browse/OOZIE-3298) | [MapReduce action] External ID is not filled properly and failing MR job is treated as SUCCEEDED |  Blocker | . | Peter Bacsko | Andras Piros |
| [OOZIE-3349](https://issues.apache.org/jira/browse/OOZIE-3349) | Test cases in oozie fail with java.net.ConnectException |  Major | . | Alisha Prabhu | Andras Piros |
| [OOZIE-3307](https://issues.apache.org/jira/browse/OOZIE-3307) | [core] Limit heap usage of LauncherAM |  Critical | core | Sabir Naikwadi | Andras Piros |
| [OOZIE-3343](https://issues.apache.org/jira/browse/OOZIE-3343) | [build] [tests] Add the first five test errors per module to the report |  Major | build, tests | Kinga Marton | Kinga Marton |
| [OOZIE-3354](https://issues.apache.org/jira/browse/OOZIE-3354) | [core] [SSH action] SSH action gets hung |  Major | action, core | Andras Piros | Andras Piros |
| [OOZIE-3160](https://issues.apache.org/jira/browse/OOZIE-3160) | PriorityDelayQueue put()/take() can cause significant CPU load due to busy waiting |  Major | core | jj | Peter Bacsko |
| [OOZIE-3358](https://issues.apache.org/jira/browse/OOZIE-3358) | [docs] Check and fix differences between help and command line documentation for Fluent Job API |  Critical | docs, fluent-job | Kinga Marton | Kinga Marton |
| [OOZIE-3370](https://issues.apache.org/jira/browse/OOZIE-3370) | Property filtering is not consistent across job submission |  Major | . | Gézapeti | Andras Piros |
| [OOZIE-3376](https://issues.apache.org/jira/browse/OOZIE-3376) | [tests] TestGraphGenerator should assume JDK8 minor version at least 1.8.0\_u40 |  Major | docs, tests | Andras Piros | Andras Piros |
| [OOZIE-3386](https://issues.apache.org/jira/browse/OOZIE-3386) | Misleading error message when workflow application does not exist |  Major | . | Attila Sasvári | Kinga Marton |
| [OOZIE-3389](https://issues.apache.org/jira/browse/OOZIE-3389) | Getting input dependency list on the UI throws NPE |  Blocker | . | Attila Sasvári | Andras Piros |
| [OOZIE-3390](https://issues.apache.org/jira/browse/OOZIE-3390) | [Shell action] STDERR contains a bogus error message |  Blocker | action | Attila Sasvári | Kinga Marton |
| [OOZIE-3388](https://issues.apache.org/jira/browse/OOZIE-3388) | When use oozie5.0.0 submit a  Action on Yarn,Launcher filed |  Major | core | duan xiong |  |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-3329](https://issues.apache.org/jira/browse/OOZIE-3329) | [build] test-patch-30-distro improvement |  Minor | build | Andras Salamon | Andras Salamon |
| [OOZIE-3331](https://issues.apache.org/jira/browse/OOZIE-3331) | [spark-action] Inconsistency while parsing quoted Spark options |  Minor | action | Andras Salamon | Andras Salamon |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-3017](https://issues.apache.org/jira/browse/OOZIE-3017) | API for workflows: other action types |  Major | client | Daniel Becker | Andras Piros |
| [OOZIE-3154](https://issues.apache.org/jira/browse/OOZIE-3154) | CLI: generate, check, submit and run workflow definitions based on API jars |  Major | client | Andras Piros | Andras Piros |
| [OOZIE-2934](https://issues.apache.org/jira/browse/OOZIE-2934) | [sharelib/spark] Fix Findbugs error |  Major | build | Jan Hentschel | Jan Hentschel |
| [OOZIE-3236](https://issues.apache.org/jira/browse/OOZIE-3236) | Fix flaky test TestHiveActionExecutor#testHiveAction |  Major | action, tests | Peter Bacsko | Peter Bacsko |
| [OOZIE-3240](https://issues.apache.org/jira/browse/OOZIE-3240) | Flaky test TestJMSAccessorService#testConnectionRetry |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3246](https://issues.apache.org/jira/browse/OOZIE-3246) | Flaky test TestJMSJobEventListener#testConnectionDrop |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-2968](https://issues.apache.org/jira/browse/OOZIE-2968) | TestJavaActionExecutor.testCredentialsSkip fails intermittently |  Major | tests | Parita Johari | Peter Bacsko |
| [OOZIE-3226](https://issues.apache.org/jira/browse/OOZIE-3226) | [tools] TestOozieDBCLI#testOozieDBCLI() fails |  Major | tools | Alisha Prabhu | Peter Bacsko |
| [OOZIE-3242](https://issues.apache.org/jira/browse/OOZIE-3242) | Flaky test TestXCommand#testXCommandLifecycleLockingFailingToLock |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3239](https://issues.apache.org/jira/browse/OOZIE-3239) | Flaky test TestJMSAccessorService#testConnectionRetryExceptionListener |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3241](https://issues.apache.org/jira/browse/OOZIE-3241) | Flaky test TestRecoveryService#testCoordActionRecoveryServiceForWaitingRegisterPartition |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-2867](https://issues.apache.org/jira/browse/OOZIE-2867) | [Coordinators] Emphasize Region/City timezone format |  Major | coordinator | Andras Piros | Artem Ervits |
| [OOZIE-3251](https://issues.apache.org/jira/browse/OOZIE-3251) | Disable JMX for ActiveMQ in the tests |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3237](https://issues.apache.org/jira/browse/OOZIE-3237) | Flaky test TestZKLocksService#testWriteReadLockThreads |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3238](https://issues.apache.org/jira/browse/OOZIE-3238) | Flaky test TestStatusTransitService#testBundleStatusTransitWithLock |  Major | tests | Peter Bacsko | Peter Bacsko |
| [OOZIE-3253](https://issues.apache.org/jira/browse/OOZIE-3253) | Flaky test TestStatusTransitService#testCoordStatusTransitWithLock |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-2967](https://issues.apache.org/jira/browse/OOZIE-2967) | TestStatusTransitService.testBundleStatusCoordSubmitFails fails intermittently in Apache Oozie Core 5.0.0-SNAPSHOT |  Major | tests | Parita Johari | Peter Bacsko |
| [OOZIE-3257](https://issues.apache.org/jira/browse/OOZIE-3257) | TestHiveActionExecutor#testHiveAction still fails |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3269](https://issues.apache.org/jira/browse/OOZIE-3269) | Flaky tests in TestCoordMaterializeTriggerService class |  Major | coordinator, core, tests | Peter Bacsko | Peter Bacsko |
| [OOZIE-3015](https://issues.apache.org/jira/browse/OOZIE-3015) | Documentation: public part (TWiki) |  Major | client | Daniel Becker | Daniel Becker |
| [OOZIE-2097](https://issues.apache.org/jira/browse/OOZIE-2097) | Get rid of non-Javadoc comments |  Major | . | Rohini Palaniswamy | Jan Hentschel |
| [OOZIE-3227](https://issues.apache.org/jira/browse/OOZIE-3227) | Eliminate duplicate dependencies when using Hadoop 3 DistributedCache |  Major | core | Dénes Bodó | Dénes Bodó |
| [OOZIE-3289](https://issues.apache.org/jira/browse/OOZIE-3289) | TestJMSAccessorService#testConnectionRetry is still flaky |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3292](https://issues.apache.org/jira/browse/OOZIE-3292) | Test TestJMSAccessorService#testConnectionRetryExceptionListener is still flaky |  Major | . | Peter Bacsko | Peter Bacsko |
| [OOZIE-3295](https://issues.apache.org/jira/browse/OOZIE-3295) | Flaky test TestSLACalculatorMemory#testAddMultipleRestartRemoveMultipleInstrumentedCorrectly |  Major | core, tests | Peter Bacsko | Peter Bacsko |
| [OOZIE-2956](https://issues.apache.org/jira/browse/OOZIE-2956) | Fix Findbugs warnings related to reliance on default encoding in oozie-core |  Major | build, core | Jan Hentschel | Kinga Marton |
| [OOZIE-2955](https://issues.apache.org/jira/browse/OOZIE-2955) | [oozie-client] Fix Findbugs warnings |  Major | build, client | Jan Hentschel | Kinga Marton |
| [OOZIE-2942](https://issues.apache.org/jira/browse/OOZIE-2942) | [examples] Fix Findbugs warnings |  Major | build | Jan Hentschel | Kinga Marton |
| [OOZIE-3264](https://issues.apache.org/jira/browse/OOZIE-3264) | Flaky test TestCoordMaterializeTransitionXCommand#testLastOnlyMaterialization |  Major | . | Peter Bacsko | Andras Salamon |
| [OOZIE-3318](https://issues.apache.org/jira/browse/OOZIE-3318) | [build] Fix Javadoc check in the pre-commit |  Blocker | scripts | Kinga Marton | Kinga Marton |
| [OOZIE-2877](https://issues.apache.org/jira/browse/OOZIE-2877) | Git action |  Major | action | Clay B. | Clay B. |
| [OOZIE-3317](https://issues.apache.org/jira/browse/OOZIE-3317) | [build] Fix false positive precommit reports |  Critical | scripts | Kinga Marton | Kinga Marton |
| [OOZIE-3351](https://issues.apache.org/jira/browse/OOZIE-3351) | [tests] Flaky test TestMemoryLocks#testWriteLockSameThreadNoWait() |  Major | tests | Andras Piros | Peter Bacsko |
| [OOZIE-3352](https://issues.apache.org/jira/browse/OOZIE-3352) | [tests] TestCallableQueueService#testPriorityExecutionOrder() is flaky |  Major | tests | Kinga Marton | Peter Bacsko |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [OOZIE-2937](https://issues.apache.org/jira/browse/OOZIE-2937) | Remove redundant groupId from the child POMs |  Trivial | build | Jan Hentschel | Jan Hentschel |
| [OOZIE-2211](https://issues.apache.org/jira/browse/OOZIE-2211) | Remove OozieCLI#validateCommandV41 |  Trivial | . | seoeun | Artem Ervits |
| [OOZIE-3224](https://issues.apache.org/jira/browse/OOZIE-3224) | Upgrade Jetty to 9.3 |  Major | . | Attila Sasvári | Kinga Marton |
| [OOZIE-3369](https://issues.apache.org/jira/browse/OOZIE-3369) | [core] Upgrade guru.nidi:graphviz-java to 0.7.0 |  Major | core | Andras Piros | Andras Piros |
| [OOZIE-3377](https://issues.apache.org/jira/browse/OOZIE-3377) | [docs] Remaining 5.1.0 documentation changes |  Major | docs | Andras Piros | Andras Piros |


