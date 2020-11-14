
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
# Apache Spark Changelog

## Release 2.4.0 - 2018-11-02



### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-23680](https://issues.apache.org/jira/browse/SPARK-23680) | entrypoint.sh does not accept arbitrary UIDs, returning as an error |  Major | Kubernetes, Spark Core | Ricardo Martinelli de Oliveira | Ricardo Martinelli de Oliveira |
| [SPARK-24021](https://issues.apache.org/jira/browse/SPARK-24021) | Fix bug in BlacklistTracker's updateBlacklistForFetchFailure |  Major | Spark Core | wuyi | wuyi |
| [SPARK-25275](https://issues.apache.org/jira/browse/SPARK-25275) | require memberhip in wheel to run 'su' (in dockerfiles) |  Major | Kubernetes, Spark Core | Erik Erlandson | Erik Erlandson |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-22119](https://issues.apache.org/jira/browse/SPARK-22119) | Add cosine distance to KMeans |  Minor | ML, MLlib | Marco Gaido | Marco Gaido |
| [SPARK-23235](https://issues.apache.org/jira/browse/SPARK-23235) | Add executor Threaddump to api |  Minor | Web UI | Imran Rashid | Attila Zsolt Piros |
| [SPARK-23541](https://issues.apache.org/jira/browse/SPARK-23541) | Allow Kafka source to read data with greater parallelism than the number of topic-partitions |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23751](https://issues.apache.org/jira/browse/SPARK-23751) | Kolmogorov-Smirnoff test Python API in pyspark.ml |  Major | ML, PySpark | Joseph K. Bradley | Weichen Xu |
| [SPARK-23948](https://issues.apache.org/jira/browse/SPARK-23948) | Trigger mapstage's job listener in submitMissingTasks |  Major | Scheduler, Spark Core | Jin Xing | Jin Xing |
| [SPARK-23846](https://issues.apache.org/jira/browse/SPARK-23846) | samplingRatio for schema inferring of CSV datasource |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-14682](https://issues.apache.org/jira/browse/SPARK-14682) | Provide evaluateEachIteration method or equivalent for spark.ml GBTs |  Minor | ML | Joseph K. Bradley | Weichen Xu |
| [SPARK-24027](https://issues.apache.org/jira/browse/SPARK-24027) | Support MapType(StringType, DataType) as root type by from\_json |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24231](https://issues.apache.org/jira/browse/SPARK-24231) | Python API: Provide evaluateEachIteration method or equivalent for spark.ml GBTs |  Minor | ML, PySpark | Weichen Xu | Lu Wang |
| [SPARK-24193](https://issues.apache.org/jira/browse/SPARK-24193) | Sort by disk when number of limit is big in TakeOrderedAndProjectExec |  Major | SQL | Jin Xing | Jin Xing |
| [SPARK-23856](https://issues.apache.org/jira/browse/SPARK-23856) | Spark jdbc setQueryTimeout option |  Minor | SQL | Dmitry Mikhailov | Takeshi Yamamuro |
| [SPARK-24371](https://issues.apache.org/jira/browse/SPARK-24371) | Added isInCollection in DataFrame API for Scala and Java. |  Major | SQL | DB Tsai | DB Tsai |
| [SPARK-24397](https://issues.apache.org/jira/browse/SPARK-24397) | Add TaskContext.getLocalProperties in Python |  Major | PySpark | Tathagata Das | Tathagata Das |
| [SPARK-24232](https://issues.apache.org/jira/browse/SPARK-24232) | Allow referring to kubernetes secrets as env variable |  Major | Kubernetes, Spark Core | Dharmesh Kakadia | Stavros Kontopoulos |
| [SPARK-15784](https://issues.apache.org/jira/browse/SPARK-15784) | Add Power Iteration Clustering to spark.ml |  Major | ML | Xinh Huynh | Miao Wang |
| [SPARK-23984](https://issues.apache.org/jira/browse/SPARK-23984) | PySpark Bindings for K8S |  Major | Kubernetes, PySpark, Spark Core | Ilan Filonenko |  |
| [SPARK-23010](https://issues.apache.org/jira/browse/SPARK-23010) | Add integration testing for Kubernetes backend into the apache/spark repository |  Major | Kubernetes, Spark Core | Anirudh Ramanathan |  |
| [SPARK-24412](https://issues.apache.org/jira/browse/SPARK-24412) | Adding docs about automagical type casting in \`isin\` and \`isInCollection\` APIs |  Major | SQL | DB Tsai | thrvskn |
| [SPARK-15064](https://issues.apache.org/jira/browse/SPARK-15064) | Locale support in StopWordsRemover |  Major | ML | Xiangrui Meng |  |
| [SPARK-24479](https://issues.apache.org/jira/browse/SPARK-24479) | Register StreamingQueryListener in Spark Conf |  Major | Structured Streaming | Mingjie Tang | Arun Mahadevan |
| [SPARK-24396](https://issues.apache.org/jira/browse/SPARK-24396) | Add Structured Streaming ForeachWriter for python |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24542](https://issues.apache.org/jira/browse/SPARK-24542) | Hive UDF series UDFXPathXXXX allow users to pass carefully crafted XML to access arbitrary files |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-24372](https://issues.apache.org/jira/browse/SPARK-24372) | Create script for preparing RCs |  Major | Project Infra | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24465](https://issues.apache.org/jira/browse/SPARK-24465) | LSHModel should support Structured Streaming for transform |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-24662](https://issues.apache.org/jira/browse/SPARK-24662) | Structured Streaming should support LIMIT |  Major | Structured Streaming | Mukul Murthy | Mukul Murthy |
| [SPARK-24730](https://issues.apache.org/jira/browse/SPARK-24730) | Add policy to choose max as global watermark when streaming query has multiple watermarks |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-22880](https://issues.apache.org/jira/browse/SPARK-22880) | Add option to cascade jdbc truncate if database supports this (PostgreSQL and Oracle) |  Minor | SQL | Daniel van der Ende | Daniel van der Ende |
| [SPARK-24802](https://issues.apache.org/jira/browse/SPARK-24802) | Optimization Rule Exclusion |  Major | SQL | Wei Xue | Wei Xue |
| [SPARK-23146](https://issues.apache.org/jira/browse/SPARK-23146) | Support client mode for Kubernetes cluster backend |  Major | Kubernetes, Spark Core | Anirudh Ramanathan |  |
| [SPARK-24795](https://issues.apache.org/jira/browse/SPARK-24795) | Implement barrier execution mode |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24288](https://issues.apache.org/jira/browse/SPARK-24288) | Enable preventing predicate pushdown |  Major | SQL | Tomasz Gawęda | Wei Xue |
| [SPARK-21274](https://issues.apache.org/jira/browse/SPARK-21274) | Implement EXCEPT ALL and INTERSECT ALL |  Major | SQL | Ruslan Dautkhanov | Dilip Biswal |
| [SPARK-24820](https://issues.apache.org/jira/browse/SPARK-24820) | Fail fast when submitted job contains PartitionPruningRDD in a barrier stage |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24821](https://issues.apache.org/jira/browse/SPARK-24821) | Fail fast when submitted job compute on a subset of all the partitions for a barrier stage |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24817](https://issues.apache.org/jira/browse/SPARK-24817) | Implement BarrierTaskContext.barrier() |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24822](https://issues.apache.org/jira/browse/SPARK-24822) | Python support for barrier execution mode |  Major | PySpark, Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24819](https://issues.apache.org/jira/browse/SPARK-24819) | Fail fast when no enough slots to launch the barrier stage on job submitted |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24433](https://issues.apache.org/jira/browse/SPARK-24433) | R Bindings for K8S |  Major | Kubernetes, Spark Core | Yinan Li | Ilan Filonenko |
| [SPARK-24411](https://issues.apache.org/jira/browse/SPARK-24411) | Adding native Java tests for \`isInCollection\` |  Minor | SQL | DB Tsai |  |
| [SPARK-10697](https://issues.apache.org/jira/browse/SPARK-10697) | Lift Calculation in Association Rule mining |  Minor | MLlib | Yashwanth Kumar | Marco Gaido |
| [SPARK-24768](https://issues.apache.org/jira/browse/SPARK-24768) | Have a built-in AVRO data source implementation |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24918](https://issues.apache.org/jira/browse/SPARK-24918) | Executor Plugin API |  Major | Spark Core | Imran Rashid | Nihar Sheth |
| [SPARK-25468](https://issues.apache.org/jira/browse/SPARK-25468) | Highlight current page index in the history server |  Trivial | Web UI | Dhruve Ashar | Adam Wang |
| [SPARK-24499](https://issues.apache.org/jira/browse/SPARK-24499) | Split the page of sql-programming-guide.html to multiple separate pages |  Major | Documentation, SQL | Xiao Li | Yuanjian Li |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-23043](https://issues.apache.org/jira/browse/SPARK-23043) | Upgrade json4s-jackson to 3.5.3 |  Minor | Build | Takako Shimamoto | Takako Shimamoto |
| [SPARK-22959](https://issues.apache.org/jira/browse/SPARK-22959) | Configuration to select the modules for daemon and worker in PySpark |  Major | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23031](https://issues.apache.org/jira/browse/SPARK-23031) | Merge script should allow arbitrary assignees |  Minor | Project Infra | Marcelo Masiero Vanzin | Imran Rashid |
| [SPARK-23024](https://issues.apache.org/jira/browse/SPARK-23024) | Spark ui about the contents of the form need to have hidden and show features, when the table records very much. |  Minor | Web UI | guoxiaolong | guoxiaolong |
| [SPARK-23085](https://issues.apache.org/jira/browse/SPARK-23085) | API parity for mllib.linalg.Vectors.sparse |  Minor | ML | zhengruifeng | zhengruifeng |
| [SPARK-11630](https://issues.apache.org/jira/browse/SPARK-11630) | ClosureCleaner incorrectly warns for class based closures |  Trivial | Spark Core | Frens Jan Rumph | Rekha Joshi |
| [SPARK-23174](https://issues.apache.org/jira/browse/SPARK-23174) | Fix pep8 to latest official version |  Trivial | Build | Rekha Joshi | Rekha Joshi |
| [SPARK-22068](https://issues.apache.org/jira/browse/SPARK-22068) | Reduce the duplicate code between putIteratorAsValues and putIteratorAsBytes |  Major | Spark Core | Xianyang Liu | Xianyang Liu |
| [SPARK-23166](https://issues.apache.org/jira/browse/SPARK-23166) | Add maxDF Parameter to CountVectorizer |  Minor | ML | Yacine Mazari | Yacine Mazari |
| [SPARK-23228](https://issues.apache.org/jira/browse/SPARK-23228) | Able to track Python create SparkSession in JVM |  Minor | PySpark | Saisai Shao | Saisai Shao |
| [SPARK-23247](https://issues.apache.org/jira/browse/SPARK-23247) | combines Unsafe operations and statistics operations in Scan Data Source |  Major | SQL | caoxuewen | caoxuewen |
| [SPARK-23188](https://issues.apache.org/jira/browse/SPARK-23188) | Make vectorized columar reader batch size configurable |  Major | SQL | Xingbo Jiang | Xingbo Jiang |
| [SPARK-23202](https://issues.apache.org/jira/browse/SPARK-23202) | Add new API in DataSourceWriter: onDataWriterCommit |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23253](https://issues.apache.org/jira/browse/SPARK-23253) | Only write shuffle temporary index file when there is not an existing one |  Major | Shuffle, Spark Core | Kent Yao | Kent Yao |
| [SPARK-23295](https://issues.apache.org/jira/browse/SPARK-23295) | Exclude Waring message when generating versions  in make-distribution.sh |  Minor | Build | Kent Yao | Kent Yao |
| [SPARK-21860](https://issues.apache.org/jira/browse/SPARK-21860) | Improve memory reuse for heap memory in \`HeapMemoryAllocator\` |  Minor | Spark Core | liuxian | liuxian |
| [SPARK-23336](https://issues.apache.org/jira/browse/SPARK-23336) | Upgrade snappy-java to 1.1.7.1 |  Minor | Build | Yuming Wang | Yuming Wang |
| [SPARK-16501](https://issues.apache.org/jira/browse/SPARK-16501) | spark.mesos.secret exposed on UI and command line |  Major | Spark Submit, Web UI | Eric Daniel | Rob Vesse |
| [SPARK-23378](https://issues.apache.org/jira/browse/SPARK-23378) | move setCurrentDatabase from HiveExternalCatalog to HiveClientImpl |  Major | SQL | Feng Liu | Feng Liu |
| [SPARK-23379](https://issues.apache.org/jira/browse/SPARK-23379) | remove redundant metastore access if the current database name is the same |  Major | SQL | Feng Liu | Feng Liu |
| [SPARK-23303](https://issues.apache.org/jira/browse/SPARK-23303) | improve the explain result for data source v2 relations |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-23318](https://issues.apache.org/jira/browse/SPARK-23318) | FP-growth: WARN FPGrowth: Input data is not cached |  Minor | ML | Arseniy Tashoyan | Arseniy Tashoyan |
| [SPARK-20659](https://issues.apache.org/jira/browse/SPARK-20659) | Remove StorageStatus, or make it private. |  Major | Spark Core | Marcelo Masiero Vanzin | Attila Zsolt Piros |
| [SPARK-23382](https://issues.apache.org/jira/browse/SPARK-23382) | Spark Streaming ui about the contents of the form need to have hidden and show features, when the table records very much. |  Minor | Web UI | guoxiaolong | guoxiaolong |
| [SPARK-23217](https://issues.apache.org/jira/browse/SPARK-23217) | Add cosine distance measure to ClusteringEvaluator |  Major | ML | Marco Gaido | Marco Gaido |
| [SPARK-23366](https://issues.apache.org/jira/browse/SPARK-23366) | Improve hot reading path in ReadAheadInputStream |  Major | Spark Core | Juliusz Sompolski | Juliusz Sompolski |
| [SPARK-23359](https://issues.apache.org/jira/browse/SPARK-23359) | Adds an alias 'names' of 'fieldNames' in Scala's StructType |  Trivial | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23447](https://issues.apache.org/jira/browse/SPARK-23447) | Cleanup codegen template for Literal |  Major | SQL | Kris Mok | Kris Mok |
| [SPARK-23383](https://issues.apache.org/jira/browse/SPARK-23383) | Make a distribution should exit with usage while detecting wrong options |  Minor | Build | Kent Yao | Kent Yao |
| [SPARK-23456](https://issues.apache.org/jira/browse/SPARK-23456) | Turn on \`native\` ORC implementation by default |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-21783](https://issues.apache.org/jira/browse/SPARK-21783) | Turn on ORC filter push-down by default |  Minor | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23424](https://issues.apache.org/jira/browse/SPARK-23424) | Add codegenStageId in comment |  Minor | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-23445](https://issues.apache.org/jira/browse/SPARK-23445) | ColumnStat refactoring |  Major | SQL | Juliusz Sompolski | Juliusz Sompolski |
| [SPARK-23389](https://issues.apache.org/jira/browse/SPARK-23389) | When the shuffle dependency specifies aggregation ,and \`dependency.mapSideCombine=false\`,  we should be able to use serialized sorting. |  Major | Spark Core | liuxian | liuxian |
| [SPARK-23510](https://issues.apache.org/jira/browse/SPARK-23510) | Support read data from Hive 2.2 and Hive 2.3 metastore |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-23518](https://issues.apache.org/jira/browse/SPARK-23518) | Avoid metastore access when users only want to read and store data frames |  Major | SQL | Feng Liu | Feng Liu |
| [SPARK-3159](https://issues.apache.org/jira/browse/SPARK-3159) | Check for reducible DecisionTree |  Minor | MLlib | Joseph K. Bradley | Alessandro Solimando |
| [SPARK-23040](https://issues.apache.org/jira/browse/SPARK-23040) | BlockStoreShuffleReader's return Iterator isn't interruptible if aggregator or ordering is specified |  Minor | Spark Core | Xianjin YE | Xianjin YE |
| [SPARK-23538](https://issues.apache.org/jira/browse/SPARK-23538) | Simplify SSL configuration for https client |  Minor | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23604](https://issues.apache.org/jira/browse/SPARK-23604) | ParquetInteroperabilityTest timestamp test should use Statistics.hasNonNullValue |  Minor | SQL | Henry Robinson | Henry Robinson |
| [SPARK-23159](https://issues.apache.org/jira/browse/SPARK-23159) | Update Cloudpickle to match version 0.4.3 |  Major | PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-22751](https://issues.apache.org/jira/browse/SPARK-22751) | Improve ML RandomForest shuffle performance |  Minor | ML | lucio35 | lucio35 |
| [SPARK-23628](https://issues.apache.org/jira/browse/SPARK-23628) | WholeStageCodegen can generate methods with too many params |  Major | SQL | Marco Gaido | Marco Gaido |
| [SPARK-23624](https://issues.apache.org/jira/browse/SPARK-23624) | Revise doc of method pushFilters |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23412](https://issues.apache.org/jira/browse/SPARK-23412) | Add cosine distance measure to BisectingKMeans |  Minor | ML, MLlib | Marco Gaido | Marco Gaido |
| [SPARK-23550](https://issues.apache.org/jira/browse/SPARK-23550) | Cleanup unused / redundant methods in Utils object |  Trivial | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23656](https://issues.apache.org/jira/browse/SPARK-23656) | Assertion in XXH64Suite.testKnownByteArrayInputs() is not performed on big endian platform |  Minor | Tests | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-23695](https://issues.apache.org/jira/browse/SPARK-23695) | Confusing error message for PySpark's Kinesis tests when its jar is missing but enabled |  Trivial | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23644](https://issues.apache.org/jira/browse/SPARK-23644) | SHS with proxy doesn't show applications |  Minor | Spark Core, Web UI | Marco Gaido | Marco Gaido |
| [SPARK-23553](https://issues.apache.org/jira/browse/SPARK-23553) | Tests should not assume the default value of \`spark.sql.sources.default\` |  Major | Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-15009](https://issues.apache.org/jira/browse/SPARK-15009) | PySpark CountVectorizerModel should be able to construct from vocabulary list |  Minor | ML, PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-23683](https://issues.apache.org/jira/browse/SPARK-23683) | FileCommitProtocol.instantiate to require 3-arg constructor for dynamic partition overwrite |  Major | Spark Core | Steve Loughran | Steve Loughran |
| [SPARK-23708](https://issues.apache.org/jira/browse/SPARK-23708) | Comment of ShutdownHookManager.addShutdownHook is error |  Minor | Spark Core | zhoukang | zhoukang |
| [SPARK-23691](https://issues.apache.org/jira/browse/SPARK-23691) | Use sql\_conf util in PySpark tests where possible |  Minor | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23500](https://issues.apache.org/jira/browse/SPARK-23500) | Filters on named\_structs could be pushed into scans |  Major | SQL | Henry Robinson | Henry Robinson |
| [SPARK-23568](https://issues.apache.org/jira/browse/SPARK-23568) | Silhouette should get number of features from metadata if available |  Minor | ML | Marco Gaido | Marco Gaido |
| [SPARK-23372](https://issues.apache.org/jira/browse/SPARK-23372) | Writing empty struct in parquet fails during execution. It should fail earlier during analysis. |  Minor | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-23769](https://issues.apache.org/jira/browse/SPARK-23769) | Remove unnecessary scalastyle check disabling |  Minor | Spark Core | Riaas Mokiem | Riaas Mokiem |
| [SPARK-23167](https://issues.apache.org/jira/browse/SPARK-23167) | Update TPCDS queries from v1.4 to v2.7 (latest) |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-23700](https://issues.apache.org/jira/browse/SPARK-23700) | Cleanup unused imports |  Major | PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-23645](https://issues.apache.org/jira/browse/SPARK-23645) | pandas\_udf can not be called with keyword arguments |  Minor | PySpark | Stu (Michael Stewart) | Stu (Michael Stewart) |
| [SPARK-23572](https://issues.apache.org/jira/browse/SPARK-23572) | Update security.md to cover new features |  Major | Documentation | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23162](https://issues.apache.org/jira/browse/SPARK-23162) | PySpark ML LinearRegressionSummary missing r2adj |  Minor | ML, PySpark | Bryan Cutler | kevin yu |
| [SPARK-23699](https://issues.apache.org/jira/browse/SPARK-23699) | PySpark should raise same Error when Arrow fallback is disabled |  Minor | PySpark, SQL | Bryan Cutler | Bryan Cutler |
| [SPARK-23675](https://issues.apache.org/jira/browse/SPARK-23675) | Title add spark logo, use spark logo image |  Minor | Web UI | guoxiaolong | guoxiaolong |
| [SPARK-23770](https://issues.apache.org/jira/browse/SPARK-23770) | Expose repartitionByRange in SparkR |  Major | SparkR | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23285](https://issues.apache.org/jira/browse/SPARK-23285) | Allow spark.executor.cores to be fractional |  Minor | Kubernetes, Scheduler, Spark Core, Spark Submit | Anirudh Ramanathan | Yinan Li |
| [SPARK-23838](https://issues.apache.org/jira/browse/SPARK-23838) | SparkUI: Running SQL query displayed as "completed" in SQL tab |  Major | Web UI | Gengliang Wang | Gengliang Wang |
| [SPARK-23822](https://issues.apache.org/jira/browse/SPARK-23822) | Improve error message for Parquet schema mismatches |  Major | SQL | Yuchen Huo | Yuchen Huo |
| [SPARK-23861](https://issues.apache.org/jira/browse/SPARK-23861) | Clarify behavior of default window frame boundaries with and without orderBy clause |  Minor | SQL | Li Jin | Li Jin |
| [SPARK-23828](https://issues.apache.org/jira/browse/SPARK-23828) | PySpark StringIndexerModel should have constructor from labels |  Minor | ML, PySpark | Bryan Cutler | Huaxin Gao |
| [SPARK-23892](https://issues.apache.org/jira/browse/SPARK-23892) | Improve coverage and fix lint error in UTF8String-related Suite |  Minor | Spark Core | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-22856](https://issues.apache.org/jira/browse/SPARK-22856) | Add wrapper for codegen output and nullability |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-23947](https://issues.apache.org/jira/browse/SPARK-23947) | Add hashUTF8String convenience method to hasher classes |  Minor | SQL | Kris Mok | Kris Mok |
| [SPARK-23841](https://issues.apache.org/jira/browse/SPARK-23841) | NodeIdCache should unpersist the last cached nodeIdsForInstances |  Minor | ML | zhengruifeng | zhengruifeng |
| [SPARK-23944](https://issues.apache.org/jira/browse/SPARK-23944) | Add Param set functions to LSHModel types |  Major | MLlib | Lu Wang | Lu Wang |
| [SPARK-23562](https://issues.apache.org/jira/browse/SPARK-23562) | RFormula handleInvalid should handle invalid values in non-string columns. |  Major | ML | Bago Amirbekian |  |
| [SPARK-19947](https://issues.apache.org/jira/browse/SPARK-19947) | RFormulaModel always throws Exception on transforming data with NULL or Unseen labels |  Major | ML | Andrei Iatsuk |  |
| [SPARK-23960](https://issues.apache.org/jira/browse/SPARK-23960) | Mark HashAggregateExec.bufVars as transient |  Minor | SQL | Kris Mok | Kris Mok |
| [SPARK-22941](https://issues.apache.org/jira/browse/SPARK-22941) | Allow SparkSubmit to throw exceptions instead of exiting / printing errors. |  Major | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23962](https://issues.apache.org/jira/browse/SPARK-23962) | Flaky tests from SQLMetricsTestUtils.currentExecutionIds |  Minor | SQL, Tests | Imran Rashid | Imran Rashid |
| [SPARK-23867](https://issues.apache.org/jira/browse/SPARK-23867) | com.codahale.metrics.Counter output in log message has no toString method |  Minor | Scheduler, Spark Core | Patrick Pisciuneri | Patrick Pisciuneri |
| [SPARK-22839](https://issues.apache.org/jira/browse/SPARK-22839) | Refactor Kubernetes code for configuring driver/executor pods to use consistent and cleaner abstraction |  Major | Kubernetes, Spark Core | Yinan Li | Matt Cheah |
| [SPARK-23896](https://issues.apache.org/jira/browse/SPARK-23896) | Improve PartitioningAwareFileIndex |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23375](https://issues.apache.org/jira/browse/SPARK-23375) | Optimizer should remove unneeded Sort |  Minor | SQL | Marco Gaido | Marco Gaido |
| [SPARK-23963](https://issues.apache.org/jira/browse/SPARK-23963) | Queries on text-based Hive tables grow disproportionately slower as the number of columns increase |  Minor | SQL | Bruce Robbins | Bruce Robbins |
| [SPARK-23966](https://issues.apache.org/jira/browse/SPARK-23966) | Refactoring all checkpoint file writing logic in a common interface |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23979](https://issues.apache.org/jira/browse/SPARK-23979) | MultiAlias should not be a CodegenFallback |  Trivial | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-23956](https://issues.apache.org/jira/browse/SPARK-23956) | Use effective RPC port in AM registration |  Minor | Spark Core, YARN | Gera Shegalov | Gera Shegalov |
| [SPARK-9312](https://issues.apache.org/jira/browse/SPARK-9312) | The OneVsRest model does not provide rawPrediction |  Major | ML, MLlib | Badari Madhav | Lu Wang |
| [SPARK-23873](https://issues.apache.org/jira/browse/SPARK-23873) | Use accessors in interpreted LambdaVariable |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-23875](https://issues.apache.org/jira/browse/SPARK-23875) | Create IndexedSeq wrapper for ArrayData |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-21741](https://issues.apache.org/jira/browse/SPARK-21741) | Python API for DataFrame-based multivariate summarizer |  Major | ML, PySpark | Yanbo Liang | Weichen Xu |
| [SPARK-24014](https://issues.apache.org/jira/browse/SPARK-24014) | Add onStreamingStarted method to StreamingListener |  Trivial | PySpark | L. C. Hsieh | L. C. Hsieh |
| [SPARK-23877](https://issues.apache.org/jira/browse/SPARK-23877) | Metadata-only queries do not push down filter conditions |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-24029](https://issues.apache.org/jira/browse/SPARK-24029) | Set "reuse address" flag on listen sockets |  Minor | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23564](https://issues.apache.org/jira/browse/SPARK-23564) | the  optimized logical plan about Left anti join should be further optimization |  Major | SQL | KaiXinXIaoLei | Marco Gaido |
| [SPARK-24024](https://issues.apache.org/jira/browse/SPARK-24024) | Fix deviance calculations in GLM to handle corner cases |  Minor | ML | Teng Peng | Teng Peng |
| [SPARK-23973](https://issues.apache.org/jira/browse/SPARK-23973) | Remove consecutive sorts |  Minor | SQL | Henry Robinson | Marco Gaido |
| [SPARK-22683](https://issues.apache.org/jira/browse/SPARK-22683) | DynamicAllocation wastes resources by allocating containers that will barely be used |  Major | Spark Core | Julien Cuquemelle | Julien Cuquemelle |
| [SPARK-23455](https://issues.apache.org/jira/browse/SPARK-23455) | Default Params in ML should be saved separately |  Major | ML | L. C. Hsieh | L. C. Hsieh |
| [SPARK-23880](https://issues.apache.org/jira/browse/SPARK-23880) | table cache should be lazy and don't trigger any job |  Major | SQL | Wenchen Fan | Takeshi Yamamuro |
| [SPARK-24094](https://issues.apache.org/jira/browse/SPARK-24094) | Change description strings of v2 streaming sources to reflect the change |  Trivial | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24057](https://issues.apache.org/jira/browse/SPARK-24057) | put the real data type in the AssertionError message |  Minor | PySpark | Huaxin Gao | Huaxin Gao |
| [SPARK-24083](https://issues.apache.org/jira/browse/SPARK-24083) | Diagnostics message for uncaught exceptions should include the stacktrace |  Minor | Spark Core, YARN | zhoukang | zhoukang |
| [SPARK-23830](https://issues.apache.org/jira/browse/SPARK-23830) | Spark on YARN in cluster deploy mode fail with NullPointerException when a Spark application is a Scala class not object |  Trivial | Spark Core, YARN | Jacek Laskowski | Eric Maynard |
| [SPARK-23565](https://issues.apache.org/jira/browse/SPARK-23565) | Improved error message for when the number of sources for a query changes |  Minor | Structured Streaming | Patrick McGloin | Patrick McGloin |
| [SPARK-24072](https://issues.apache.org/jira/browse/SPARK-24072) | clearly define pushed filters |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24003](https://issues.apache.org/jira/browse/SPARK-24003) | Add support to provide spark.executor.extraJavaOptions in terms of App Id and/or Executor Id's |  Major | Mesos, Spark Core, YARN | Devaraj Kavali | Devaraj Kavali |
| [SPARK-24131](https://issues.apache.org/jira/browse/SPARK-24131) | Add majorMinorVersion API to PySpark for determining Spark versions |  Minor | PySpark | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24111](https://issues.apache.org/jira/browse/SPARK-24111) | Add TPCDS v2.7 (latest) queries in TPCDSQueryBenchmark |  Trivial | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-24035](https://issues.apache.org/jira/browse/SPARK-24035) | SQL syntax for Pivot |  Major | SQL | Xiao Li | Wei Xue |
| [SPARK-24136](https://issues.apache.org/jira/browse/SPARK-24136) | MemoryStreamDataReader.next should skip sleeping if record is available |  Minor | Structured Streaming | Arun Mahadevan | Arun Mahadevan |
| [SPARK-24017](https://issues.apache.org/jira/browse/SPARK-24017) | Refactor ExternalCatalog to be an interface |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-24126](https://issues.apache.org/jira/browse/SPARK-24126) | PySpark tests leave a lot of garbage in /tmp |  Minor | PySpark, Tests | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24160](https://issues.apache.org/jira/browse/SPARK-24160) | ShuffleBlockFetcherIterator should fail if it receives zero-size blocks |  Major | Shuffle, Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-16406](https://issues.apache.org/jira/browse/SPARK-16406) | Reference resolution for large number of columns should be faster |  Major | SQL | Herman van Hövell | Herman van Hövell |
| [SPARK-24128](https://issues.apache.org/jira/browse/SPARK-24128) | Mention spark.sql.crossJoin.enabled in implicit cartesian product error msg |  Minor | SQL | Henry Robinson | Henry Robinson |
| [SPARK-24188](https://issues.apache.org/jira/browse/SPARK-24188) | /api/v1/version not working |  Major | Web UI | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24117](https://issues.apache.org/jira/browse/SPARK-24117) | Unified the getSizePerRow |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-23972](https://issues.apache.org/jira/browse/SPARK-23972) | Upgrade to Parquet 1.10 |  Major | Spark Core | Henry Robinson | Ryan Blue |
| [SPARK-24181](https://issues.apache.org/jira/browse/SPARK-24181) | Better error message for writing sorted data |  Major | SQL | DB Tsai | DB Tsai |
| [SPARK-24182](https://issues.apache.org/jira/browse/SPARK-24182) | Improve error message for client mode when AM fails |  Minor | Spark Core, YARN | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24172](https://issues.apache.org/jira/browse/SPARK-24172) | we should not apply operator pushdown to data source v2 many times |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24246](https://issues.apache.org/jira/browse/SPARK-24246) | Improve AnalysisException by setting the cause when it's available |  Major | SQL | Shixiong Zhu | Shixiong Zhu |
| [SPARK-24262](https://issues.apache.org/jira/browse/SPARK-24262) | Fix typo in UDF error message |  Trivial | PySpark | Holden Karau | Kelley Robinson |
| [SPARK-23627](https://issues.apache.org/jira/browse/SPARK-23627) | Provide isEmpty() function in DataSet |  Trivial | Spark Core, SQL | Goun Na | Goun Na |
| [SPARK-24058](https://issues.apache.org/jira/browse/SPARK-24058) | Default Params in ML should be saved separately: Python API |  Major | ML, PySpark | Joseph K. Bradley | L. C. Hsieh |
| [SPARK-24275](https://issues.apache.org/jira/browse/SPARK-24275) | Revise doc comments in InputPartition |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-22210](https://issues.apache.org/jira/browse/SPARK-22210) | Online LDA variationalTopicInference  should use random seed to have stable behavior |  Minor | ML | yuhao yang | Lu Wang |
| [SPARK-24277](https://issues.apache.org/jira/browse/SPARK-24277) | Code clean up in SQL module: HadoopMapReduceCommitProtocol/FileFormatWriter |  Trivial | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24303](https://issues.apache.org/jira/browse/SPARK-24303) | Update cloudpickle to v0.4.4 |  Minor | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-20538](https://issues.apache.org/jira/browse/SPARK-20538) | Dataset.reduce operator should use withNewExecutionId (as foreach or foreachPartition) |  Trivial | SQL | Jacek Laskowski | Soham Aurangabadkar |
| [SPARK-24312](https://issues.apache.org/jira/browse/SPARK-24312) | Upgrade to 2.3.3 for Hive Metastore Client 2.3 |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24149](https://issues.apache.org/jira/browse/SPARK-24149) | Automatic namespaces discovery in HDFS federation |  Minor | Spark Core, YARN | Marco Gaido | Marco Gaido |
| [SPARK-24308](https://issues.apache.org/jira/browse/SPARK-24308) | Handle DataReaderFactory to InputPartition renames in left over classes |  Major | SQL | Arun Mahadevan | Arun Mahadevan |
| [SPARK-24250](https://issues.apache.org/jira/browse/SPARK-24250) | support accessing SQLConf inside tasks |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24242](https://issues.apache.org/jira/browse/SPARK-24242) | RangeExec should have correct outputOrdering |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-7132](https://issues.apache.org/jira/browse/SPARK-7132) | Add fit with validation set to spark.ml GBT |  Minor | ML | Joseph K. Bradley | Weichen Xu |
| [SPARK-24209](https://issues.apache.org/jira/browse/SPARK-24209) | 0 configuration Knox gateway support in SHS |  Minor | Web UI | Marco Gaido | Marco Gaido |
| [SPARK-24321](https://issues.apache.org/jira/browse/SPARK-24321) | Extract common code from Divide/Remainder to a base trait |  Minor | SQL | Kris Mok | Kris Mok |
| [SPARK-20087](https://issues.apache.org/jira/browse/SPARK-20087) | Include accumulators / taskMetrics when sending TaskKilled to onTaskEnd listeners |  Major | Spark Core | Charles Lewis | Xianjin YE |
| [SPARK-24121](https://issues.apache.org/jira/browse/SPARK-24121) | The API for handling expression code generation in expression codegen |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24206](https://issues.apache.org/jira/browse/SPARK-24206) | Improve DataSource benchmark code for read and pushdown |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-22269](https://issues.apache.org/jira/browse/SPARK-22269) | Java style checks should be run in Jenkins |  Major | Build | Andrew Ash | Hyukjin Kwon |
| [SPARK-24329](https://issues.apache.org/jira/browse/SPARK-24329) | Remove comments filtering before parsing of CSV files |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24332](https://issues.apache.org/jira/browse/SPARK-24332) | Fix places reading 'spark.network.timeout' as milliseconds |  Major | Mesos, Structured Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-24367](https://issues.apache.org/jira/browse/SPARK-24367) | Parquet: use JOB\_SUMMARY\_LEVEL instead of deprecated flag ENABLE\_JOB\_SUMMARY |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24244](https://issues.apache.org/jira/browse/SPARK-24244) | Parse only required columns of CSV file |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24366](https://issues.apache.org/jira/browse/SPARK-24366) | Improve error message for Catalyst type converters |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24381](https://issues.apache.org/jira/browse/SPARK-24381) | Improve Unit Test Coverage of NOT IN subqueries |  Major | SQL | Miles Yucht |  |
| [SPARK-24365](https://issues.apache.org/jira/browse/SPARK-24365) | Add data source write benchmark |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23161](https://issues.apache.org/jira/browse/SPARK-23161) | Add missing APIs to Python GBTClassifier |  Minor | ML, PySpark | Bryan Cutler | Huaxin Gao |
| [SPARK-24337](https://issues.apache.org/jira/browse/SPARK-24337) | Improve the error message for invalid SQL conf value |  Major | SQL | Shixiong Zhu |  |
| [SPARK-24330](https://issues.apache.org/jira/browse/SPARK-24330) | Refactor ExecuteWriteTask in FileFormatWriter with DataWriter(V2) |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24326](https://issues.apache.org/jira/browse/SPARK-24326) |  Add local:// scheme support for the app jar in mesos cluster mode |  Major | Mesos | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-24356](https://issues.apache.org/jira/browse/SPARK-24356) | Duplicate strings in File.path managed by FileSegmentManagedBuffer |  Major | Shuffle, Spark Core | Misha Dmitriev | Misha Dmitriev |
| [SPARK-24455](https://issues.apache.org/jira/browse/SPARK-24455) | fix typo in TaskSchedulerImpl's comments |  Trivial | Spark Core | xueyu | xueyu |
| [SPARK-24215](https://issues.apache.org/jira/browse/SPARK-24215) | Implement eager evaluation for DataFrame APIs |  Major | PySpark, Spark Core, SQL | Ryan Blue | Yuanjian Li |
| [SPARK-23803](https://issues.apache.org/jira/browse/SPARK-23803) | Support bucket pruning to optimize filtering on a bucketed column |  Major | SQL | Asher Saban | Asher Saban |
| [SPARK-24477](https://issues.apache.org/jira/browse/SPARK-24477) | Import submodules under pyspark.ml by default |  Major | ML, PySpark | Xiangrui Meng | Hyukjin Kwon |
| [SPARK-24454](https://issues.apache.org/jira/browse/SPARK-24454) | ml.image doesn't have \_\_all\_\_ explicitly defined |  Minor | ML, PySpark | Xiangrui Meng | Hyukjin Kwon |
| [SPARK-22144](https://issues.apache.org/jira/browse/SPARK-22144) | ExchangeCoordinator will not combine the partitions of an 0 sized pre-shuffle |  Major | SQL | Lijia Liu | Lijia Liu |
| [SPARK-24485](https://issues.apache.org/jira/browse/SPARK-24485) | Measure and log elapsed time for filesystem operations in HDFSBackedStateStoreProvider |  Minor | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-24543](https://issues.apache.org/jira/browse/SPARK-24543) | Support any DataType as DDL string for from\_json's schema |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24248](https://issues.apache.org/jira/browse/SPARK-24248) | [K8S] Use the Kubernetes cluster as the backing store for the state of pods |  Major | Kubernetes, Spark Core | Matt Cheah |  |
| [SPARK-24490](https://issues.apache.org/jira/browse/SPARK-24490) | Use WebUI.addStaticHandler in web UIs |  Trivial | Web UI | Jacek Laskowski | Jacek Laskowski |
| [SPARK-24525](https://issues.apache.org/jira/browse/SPARK-24525) | Provide an option to limit MemorySink memory usage |  Major | Structured Streaming | Mukul Murthy | Mukul Murthy |
| [SPARK-23772](https://issues.apache.org/jira/browse/SPARK-23772) | Provide an option to ignore column of all null values or empty map/array during JSON schema inference |  Major | SQL | Xiangrui Meng | Takeshi Yamamuro |
| [SPARK-24534](https://issues.apache.org/jira/browse/SPARK-24534) | Add a way to bypass entrypoint.sh script if no spark cmd is passed |  Minor | Kubernetes, Spark Core | Ricardo Martinelli de Oliveira |  |
| [SPARK-24565](https://issues.apache.org/jira/browse/SPARK-24565) | Add API for in Structured Streaming for exposing output rows of each microbatch as a DataFrame |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24575](https://issues.apache.org/jira/browse/SPARK-24575) | Prohibit window expressions inside WHERE and HAVING clauses |  Minor | SQL | Anton Okolnychyi | Anton Okolnychyi |
| [SPARK-24547](https://issues.apache.org/jira/browse/SPARK-24547) | Spark on K8s docker-image-tool.sh improvements |  Minor | Kubernetes, Spark Core | Ray Burgemeestre |  |
| [SPARK-24571](https://issues.apache.org/jira/browse/SPARK-24571) | Support literals with values of the Char type |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24574](https://issues.apache.org/jira/browse/SPARK-24574) | improve array\_contains function of the sql component to deal with Column type |  Major | SQL | Chongguang LIU | Chongguang LIU |
| [SPARK-24614](https://issues.apache.org/jira/browse/SPARK-24614) | PySpark - Fix SyntaxWarning on tests.py |  Trivial | PySpark | Rekha Joshi | Rekha Joshi |
| [SPARK-16630](https://issues.apache.org/jira/browse/SPARK-16630) | Blacklist a node if executors won't launch on it. |  Major | Spark Core, YARN | Thomas Graves | Attila Zsolt Piros |
| [SPARK-24519](https://issues.apache.org/jira/browse/SPARK-24519) | MapStatus has 2000 hardcoded |  Minor | Spark Core | Hieu Tri Huynh | Hieu Tri Huynh |
| [SPARK-24518](https://issues.apache.org/jira/browse/SPARK-24518) | Using Hadoop credential provider API to store password |  Minor | Spark Core | Saisai Shao | Saisai Shao |
| [SPARK-24327](https://issues.apache.org/jira/browse/SPARK-24327) | Verify and normalize a partition column name based on the JDBC resolved schema |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-24596](https://issues.apache.org/jira/browse/SPARK-24596) | Non-cascading Cache Invalidation |  Major | SQL | Wei Xue | Wei Xue |
| [SPARK-23776](https://issues.apache.org/jira/browse/SPARK-23776) | pyspark-sql tests should display build instructions when components are missing |  Minor | PySpark | Bruce Robbins | Bruce Robbins |
| [SPARK-24636](https://issues.apache.org/jira/browse/SPARK-24636) | Type Coercion of Arrays for array\_join Function |  Major | SQL | Marek Novotny | Marek Novotny |
| [SPARK-24658](https://issues.apache.org/jira/browse/SPARK-24658) | Remove workaround for ANTLR bug |  Critical | SQL | Yuming Wang | Yuming Wang |
| [SPARK-24423](https://issues.apache.org/jira/browse/SPARK-24423) | Add a new option \`query\` for JDBC sources |  Major | SQL | Xiao Li | Dilip Biswal |
| [SPARK-24605](https://issues.apache.org/jira/browse/SPARK-24605) | size(null) should return null |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-21687](https://issues.apache.org/jira/browse/SPARK-21687) | Spark SQL should set createTime for Hive partition |  Minor | SQL | Chaozhong Yang | Chaozhong Yang |
| [SPARK-24204](https://issues.apache.org/jira/browse/SPARK-24204) | Verify a write schema in Json/Orc/ParquetFileFormat |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-14712](https://issues.apache.org/jira/browse/SPARK-14712) | spark.ml LogisticRegressionModel.toString should summarize model |  Trivial | ML | Joseph K. Bradley | Bravo Zhang |
| [SPARK-24408](https://issues.apache.org/jira/browse/SPARK-24408) | Move abs function to math\_funcs group |  Trivial | Documentation, SQL | Jacek Laskowski | Jacek Laskowski |
| [SPARK-24566](https://issues.apache.org/jira/browse/SPARK-24566) | Fix spark.storage.blockManagerSlaveTimeoutMs default config |  Major | Spark Core | xueyu | xueyu |
| [SPARK-24696](https://issues.apache.org/jira/browse/SPARK-24696) | ColumnPruning rule fails to remove extra Project |  Major | SQL | Xiao Li | Wei Xue |
| [SPARK-24665](https://issues.apache.org/jira/browse/SPARK-24665) | Add SQLConf in PySpark to manage all sql configs |  Major | PySpark | Yuanjian Li | Yuanjian Li |
| [SPARK-24683](https://issues.apache.org/jira/browse/SPARK-24683) | SparkLauncher.NO\_RESOURCE doesn't work with Java applications |  Critical | Kubernetes, Spark Core | Matt Cheah |  |
| [SPARK-24428](https://issues.apache.org/jira/browse/SPARK-24428) | Remove unused code and fix any related doc in K8s module |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos |  |
| [SPARK-24709](https://issues.apache.org/jira/browse/SPARK-24709) | Inferring schema from JSON string literal |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24732](https://issues.apache.org/jira/browse/SPARK-24732) | Type coercion between MapTypes. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24727](https://issues.apache.org/jira/browse/SPARK-24727) | The cache 100 in CodeGenerator is too small for streaming |  Major | SQL | ant\_nebula | Takeshi Yamamuro |
| [SPARK-24635](https://issues.apache.org/jira/browse/SPARK-24635) | Remove Blocks class |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24673](https://issues.apache.org/jira/browse/SPARK-24673) | scala sql function from\_utc\_timestamp second argument could be Column instead of String |  Minor | SQL | Antonio Murgia | Antonio Murgia |
| [SPARK-24361](https://issues.apache.org/jira/browse/SPARK-24361) | Polish code block manipulation API |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24675](https://issues.apache.org/jira/browse/SPARK-24675) | Rename table: validate existence of new location |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24737](https://issues.apache.org/jira/browse/SPARK-24737) | Type coercion between StructTypes. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24692](https://issues.apache.org/jira/browse/SPARK-24692) | Improvement FilterPushdownBenchmark |  Major | Tests | Yuming Wang | Yuming Wang |
| [SPARK-24757](https://issues.apache.org/jira/browse/SPARK-24757) | Improve error message for broadcast timeouts |  Trivial | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24646](https://issues.apache.org/jira/browse/SPARK-24646) | Support wildcard '\*' for to spark.yarn.dist.forceDownloadSchemes |  Minor | Spark Core | Saisai Shao | Saisai Shao |
| [SPARK-24759](https://issues.apache.org/jira/browse/SPARK-24759) | No reordering keys for broadcast hash join |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-24678](https://issues.apache.org/jira/browse/SPARK-24678) | We should use 'PROCESS\_LOCAL' first for Spark-Streaming |  Major | Block Manager, Spark Core | sharkd tu | sharkd tu |
| [SPARK-23529](https://issues.apache.org/jira/browse/SPARK-23529) | Specify hostpath volume and mount the volume in Spark driver and executor pods in Kubernetes |  Minor | Kubernetes, Spark Core | Suman Somasundar | Andrew Korzhuev |
| [SPARK-24470](https://issues.apache.org/jira/browse/SPARK-24470) | RestSubmissionClient to be robust against 404 & non json responses |  Minor | Spark Core | Steve Loughran | Rekha Joshi |
| [SPARK-24697](https://issues.apache.org/jira/browse/SPARK-24697) | Fix the reported start offsets in streaming query progress |  Major | Structured Streaming | Arun Mahadevan | Tathagata Das |
| [SPARK-24782](https://issues.apache.org/jira/browse/SPARK-24782) | Simplify conf access in expressions |  Minor | SQL | Marco Gaido | Marco Gaido |
| [SPARK-24761](https://issues.apache.org/jira/browse/SPARK-24761) | Check modifiability of config parameters |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24691](https://issues.apache.org/jira/browse/SPARK-24691) | Add new API \`supportDataType\` in FileFormat |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-20168](https://issues.apache.org/jira/browse/SPARK-20168) | Enable kinesis to start stream from Initial position specified by a timestamp |  Minor | DStreams | Yash Sharma | Yash Sharma |
| [SPARK-24790](https://issues.apache.org/jira/browse/SPARK-24790) | Allow complex aggregate expressions in Pivot |  Minor | SQL | Wei Xue | Wei Xue |
| [SPARK-23528](https://issues.apache.org/jira/browse/SPARK-23528) | Add numIter to ClusteringSummary |  Minor | ML | Erich Schubert | Marco Gaido |
| [SPARK-24807](https://issues.apache.org/jira/browse/SPARK-24807) | Adding files/jars twice: output a warning and add a note |  Trivial | Spark Core | Maxim Gekk | Maxim Gekk |
| [SPARK-24558](https://issues.apache.org/jira/browse/SPARK-24558) | Driver prints the wrong info in the log when the executor which holds cacheBlock is IDLE.Time-out value displayed is not as per configuration value. |  Minor | Spark Core | Sandeep Katta | Sandeep Katta |
| [SPARK-18230](https://issues.apache.org/jira/browse/SPARK-18230) | MatrixFactorizationModel.recommendProducts throws NoSuchElement exception when the user does not exist |  Minor | MLlib | Mikael Ståldal | shahid |
| [SPARK-23259](https://issues.apache.org/jira/browse/SPARK-23259) | Clean up legacy code around hive external catalog |  Major | SQL | Feng Liu | Feng Liu |
| [SPARK-24305](https://issues.apache.org/jira/browse/SPARK-24305) | Avoid serialization of private fields in new collection expressions |  Minor | SQL | Marek Novotny | Marek Novotny |
| [SPARK-21590](https://issues.apache.org/jira/browse/SPARK-21590) | Structured Streaming window start time should support negative values to adjust time zone |  Major | Structured Streaming | Kevin Zhang | Kevin Zhang |
| [SPARK-24747](https://issues.apache.org/jira/browse/SPARK-24747) | Make spark.ml.util.Instrumentation class more flexible |  Major | ML | Bago Amirbekian | Bago Amirbekian |
| [SPARK-24576](https://issues.apache.org/jira/browse/SPARK-24576) |  Upgrade Apache ORC to 1.5.2 |  Major | Build | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24129](https://issues.apache.org/jira/browse/SPARK-24129) | Add option to pass --build-arg's to docker-image-tool.sh |  Minor | Kubernetes, Spark Core | Devaraj Kavali | Devaraj Kavali |
| [SPARK-24858](https://issues.apache.org/jira/browse/SPARK-24858) | Avoid unnecessary parquet footer reads |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24268](https://issues.apache.org/jira/browse/SPARK-24268) | DataType in error messages are not coherent |  Minor | ML, SQL | Marco Gaido | Marco Gaido |
| [SPARK-24424](https://issues.apache.org/jira/browse/SPARK-24424) | Support ANSI-SQL compliant syntax for  GROUPING SET |  Major | SQL | Xiao Li | Dilip Biswal |
| [SPARK-24868](https://issues.apache.org/jira/browse/SPARK-24868) | add sequence function in Python |  Minor | PySpark | Huaxin Gao | Huaxin Gao |
| [SPARK-24871](https://issues.apache.org/jira/browse/SPARK-24871) | Refactor Concat and MapConcat to avoid creating concatenator object for each row. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24551](https://issues.apache.org/jira/browse/SPARK-24551) | Add Integration tests for Secrets |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-24339](https://issues.apache.org/jira/browse/SPARK-24339) | spark sql can not prune column in transform/map/reduce query |  Minor | SQL | xdcjie | Yuanjian Li |
| [SPARK-24890](https://issues.apache.org/jira/browse/SPARK-24890) | Short circuiting the \`if\` condition when \`trueValue\` and \`falseValue\` are the same |  Major | SQL | DB Tsai | DB Tsai |
| [SPARK-23957](https://issues.apache.org/jira/browse/SPARK-23957) | Sorts in subqueries are redundant and can be removed |  Major | SQL | Henry Robinson | Henry Robinson |
| [SPARK-19018](https://issues.apache.org/jira/browse/SPARK-19018) | spark csv writer charset support |  Major | SQL | todd.chen | Carlos Peña |
| [SPARK-24849](https://issues.apache.org/jira/browse/SPARK-24849) | Convert StructType to DDL string |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24860](https://issues.apache.org/jira/browse/SPARK-24860) | Expose dynamic partition overwrite per write operation |  Minor | SQL | koert kuipers | Koert Kuipers |
| [SPARK-24801](https://issues.apache.org/jira/browse/SPARK-24801) | Empty byte[] arrays in spark.network.sasl.SaslEncryption$EncryptedMessage can waste a lot of memory |  Major | Spark Core, YARN | Misha Dmitriev | Misha Dmitriev |
| [SPARK-24929](https://issues.apache.org/jira/browse/SPARK-24929) | Merge script swallow KeyboardInterrupt |  Trivial | Project Infra | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24865](https://issues.apache.org/jira/browse/SPARK-24865) | Remove AnalysisBarrier |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-21960](https://issues.apache.org/jira/browse/SPARK-21960) | Spark Streaming Dynamic Allocation should respect spark.executor.instances |  Minor | DStreams | Karthik Palaniappan | Karthik Palaniappan |
| [SPARK-13343](https://issues.apache.org/jira/browse/SPARK-13343) | speculative tasks that didn't commit shouldn't be marked as success |  Major | Spark Core | Thomas Graves | Hieu Tri Huynh |
| [SPARK-24956](https://issues.apache.org/jira/browse/SPARK-24956) | Upgrade maven from 3.3.9 to 3.5.4 |  Minor | Build | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-22814](https://issues.apache.org/jira/browse/SPARK-22814) | JDBC support date/timestamp type as partitionColumn |  Major | SQL | Yuechen Chen | Takeshi Yamamuro |
| [SPARK-24952](https://issues.apache.org/jira/browse/SPARK-24952) | Support LZMA2 compression by Avro datasource |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24609](https://issues.apache.org/jira/browse/SPARK-24609) | PySpark/SparkR doc doesn't explain RandomForestClassifier.featureSubsetStrategy well |  Minor | PySpark | Xiangrui Meng | zhengruifeng |
| [SPARK-24893](https://issues.apache.org/jira/browse/SPARK-24893) | Remove the entire CaseWhen if all the outputs are semantic equivalence |  Major | SQL | DB Tsai | DB Tsai |
| [SPARK-24951](https://issues.apache.org/jira/browse/SPARK-24951) | Table valued functions should throw AnalysisException instead of IllegalArgumentException |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-24982](https://issues.apache.org/jira/browse/SPARK-24982) | UDAF resolution should not throw java.lang.AssertionError |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-24960](https://issues.apache.org/jira/browse/SPARK-24960) | k8s: explicitly expose ports on driver container |  Minor | Deploy, Kubernetes, Scheduler, Spark Core | Adelbert Chang |  |
| [SPARK-24557](https://issues.apache.org/jira/browse/SPARK-24557) | ClusteringEvaluator support array input |  Major | ML | zhengruifeng | zhengruifeng |
| [SPARK-22219](https://issues.apache.org/jira/browse/SPARK-22219) | Refector "spark.sql.codegen.comments" |  Minor | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-24945](https://issues.apache.org/jira/browse/SPARK-24945) | Switch to uniVocity \>= 2.7.2 |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24993](https://issues.apache.org/jira/browse/SPARK-24993) | Make Avro fast again |  Major | SQL | DB Tsai |  |
| [SPARK-18057](https://issues.apache.org/jira/browse/SPARK-18057) | Update structured streaming kafka from 0.10.0.1 to 2.0.0 |  Major | Structured Streaming | Cody Koeninger | Ted Yu |
| [SPARK-24954](https://issues.apache.org/jira/browse/SPARK-24954) | Fail fast on job submit if run a barrier stage with dynamic resource allocation enabled |  Blocker | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24722](https://issues.apache.org/jira/browse/SPARK-24722) | Column-based API for pivoting |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24940](https://issues.apache.org/jira/browse/SPARK-24940) | Coalesce and Repartition Hint for SQL Queries |  Major | SQL | John Zhuge | John Zhuge |
| [SPARK-24926](https://issues.apache.org/jira/browse/SPARK-24926) | Ensure numCores is used consistently in all netty configuration (driver and executors) |  Minor | Spark Core | Imran Rashid | Nihar Sheth |
| [SPARK-25001](https://issues.apache.org/jira/browse/SPARK-25001) | Fix build miscellaneous warnings |  Major | Build | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-25025](https://issues.apache.org/jira/browse/SPARK-25025) | Remove the default value of isAll in INTERSECT/EXCEPT |  Major | SQL | Xiao Li | Dilip Biswal |
| [SPARK-24992](https://issues.apache.org/jira/browse/SPARK-24992) | spark should randomize yarn local dir selection |  Minor | Spark Core | Hieu Tri Huynh | Hieu Tri Huynh |
| [SPARK-24161](https://issues.apache.org/jira/browse/SPARK-24161) | Enable debug package feature on structured streaming |  Major | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-24996](https://issues.apache.org/jira/browse/SPARK-24996) | Use DSL to simplify DeclarativeAggregate |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-24637](https://issues.apache.org/jira/browse/SPARK-24637) | Add metrics regarding state and watermark to dropwizard metrics |  Major | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-25018](https://issues.apache.org/jira/browse/SPARK-25018) | Use \`Co-Authored-By\` git trailer in \`merge\_spark\_pr.py\` |  Major | Project Infra | DB Tsai | DB Tsai |
| [SPARK-24005](https://issues.apache.org/jira/browse/SPARK-24005) | Remove usage of Scala’s parallel collection |  Major | Spark Core, SQL | Xiao Li | Maxim Gekk |
| [SPARK-19602](https://issues.apache.org/jira/browse/SPARK-19602) | Unable to query using the fully qualified column name of the form ( \<DBNAME\>.\<TABLENAME\>.\<COLUMNNAME\>) |  Major | SQL | Sunitha Kambhampati | Sunitha Kambhampati |
| [SPARK-24979](https://issues.apache.org/jira/browse/SPARK-24979) | add AnalysisHelper#resolveOperatorsUp |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25045](https://issues.apache.org/jira/browse/SPARK-25045) | Make \`RDDBarrier.mapParititions\` similar to \`RDD.mapPartitions\` |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-25077](https://issues.apache.org/jira/browse/SPARK-25077) | Delete unused variable in WindowExec |  Trivial | SQL | Yuanjian Li | Yuanjian Li |
| [SPARK-24127](https://issues.apache.org/jira/browse/SPARK-24127) | Support text socket source in continuous mode |  Minor | Structured Streaming | Arun Mahadevan | Arun Mahadevan |
| [SPARK-25069](https://issues.apache.org/jira/browse/SPARK-25069) | Using UnsafeAlignedOffset to make the entire record of 8 byte Items aligned like which is used in UnsafeExternalSorter |  Major | Shuffle, Spark Core | eaton | eaton |
| [SPARK-25088](https://issues.apache.org/jira/browse/SPARK-25088) | Rest Server default & doc updates |  Major | Deploy, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-25043](https://issues.apache.org/jira/browse/SPARK-25043) | spark-sql should print the appId and master on startup |  Trivial | SQL | Alessandro Bellina | Alessandro Bellina |
| [SPARK-25113](https://issues.apache.org/jira/browse/SPARK-25113) | Add logging to CodeGenerator when any generated method's bytecode size goes above HugeMethodLimit |  Major | SQL | Kris Mok | Kris Mok |
| [SPARK-25115](https://issues.apache.org/jira/browse/SPARK-25115) |     Eliminate extra memory copy done when a ByteBuf is used that is backed by \> 1 ByteBuffer. |  Major | Input/Output | Norman Maurer | Norman Maurer |
| [SPARK-23874](https://issues.apache.org/jira/browse/SPARK-23874) | Upgrade apache/arrow to 0.10.0 |  Major | PySpark | Xiao Li | Bryan Cutler |
| [SPARK-24505](https://issues.apache.org/jira/browse/SPARK-24505) | Convert strings in codegen to blocks: Cast and BoundAttribute |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-25111](https://issues.apache.org/jira/browse/SPARK-25111) | increment kinesis client/producer lib versions & aws-sdk to match |  Major | DStreams | Steve Loughran | Steve Loughran |
| [SPARK-24685](https://issues.apache.org/jira/browse/SPARK-24685) | Adjust release scripts to build all versions for older releases |  Minor | Build | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23654](https://issues.apache.org/jira/browse/SPARK-23654) | Cut jets3t as a dependency of spark-core |  Minor | Spark Core | Steve Loughran | Steve Loughran |
| [SPARK-24555](https://issues.apache.org/jira/browse/SPARK-24555) | logNumExamples in KMeans/BiKM/GMM/AFT/NB |  Minor | ML | zhengruifeng | zhengruifeng |
| [SPARK-25122](https://issues.apache.org/jira/browse/SPARK-25122) | Deduplication of supports equals code |  Trivial | SQL | Marek Novotny | Marek Novotny |
| [SPARK-25142](https://issues.apache.org/jira/browse/SPARK-25142) | Add error messages when Python worker could not open socket in \`\_load\_from\_socket\`. |  Major | PySpark | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24441](https://issues.apache.org/jira/browse/SPARK-24441) | Expose total estimated size of states in HDFSBackedStateStoreProvider |  Major | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-25140](https://issues.apache.org/jira/browse/SPARK-25140) | Add optional logging to UnsafeProjection.create when it falls back to interpreted mode |  Minor | SQL | Kris Mok | Takeshi Yamamuro |
| [SPARK-25093](https://issues.apache.org/jira/browse/SPARK-25093) | CodeFormatter could avoid creating regex object again and again |  Minor | Spark Core | Izek Greenfield | Marco Gaido |
| [SPARK-25105](https://issues.apache.org/jira/browse/SPARK-25105) | Importing all of pyspark.sql.functions should bring PandasUDFType in as well |  Trivial | PySpark | Holden Karau | kevin yu |
| [SPARK-24785](https://issues.apache.org/jira/browse/SPARK-24785) | Making sure REPL prints Spark UI info and then Welcome message |  Major | Spark Shell | DB Tsai | DB Tsai |
| [SPARK-23034](https://issues.apache.org/jira/browse/SPARK-23034) | Display tablename for \`HiveTableScan\` node in UI |  Trivial | SQL, Web UI | Tejas Patil | Takeshi Yamamuro |
| [SPARK-25208](https://issues.apache.org/jira/browse/SPARK-25208) | Loosen Cast.forceNullable for DecimalType. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-25209](https://issues.apache.org/jira/browse/SPARK-25209) | Optimization in Dataset.apply for DataFrames |  Major | SQL | Bogdan Raducanu | Bogdan Raducanu |
| [SPARK-4502](https://issues.apache.org/jira/browse/SPARK-4502) | Spark SQL reads unneccesary nested fields from Parquet |  Critical | SQL | Liwen Sun | Michael MacFadden |
| [SPARK-25178](https://issues.apache.org/jira/browse/SPARK-25178) | Directly ship the StructType objects of the keySchema / valueSchema for xxxHashMapGenerator |  Minor | SQL | Kris Mok | Kazuaki Ishizaki |
| [SPARK-25073](https://issues.apache.org/jira/browse/SPARK-25073) | Spark-submit on Yarn Task : When the yarn.nodemanager.resource.memory-mb and/or yarn.scheduler.maximum-allocation-mb is insufficient, Spark always reports an error request to adjust yarn.scheduler.maximum-allocation-mb |  Trivial | Spark Submit | vivek kumar | Sujith Chacko |
| [SPARK-24688](https://issues.apache.org/jira/browse/SPARK-24688) | Clarify comments about LabeledPoint as (label, feature) pair rather than (feature, label) |  Minor | Examples | Weizhe Huang | Weizhe Huang |
| [SPARK-24978](https://issues.apache.org/jira/browse/SPARK-24978) | Add spark.sql.fast.hash.aggregate.row.max.capacity to configure the capacity of fast aggregation. |  Major | SQL | caoxuewen | caoxuewen |
| [SPARK-25212](https://issues.apache.org/jira/browse/SPARK-25212) | Support Filter in ConvertToLocalRelation |  Major | SQL | Bogdan Raducanu | Bogdan Raducanu |
| [SPARK-25260](https://issues.apache.org/jira/browse/SPARK-25260) | Fix namespace handling in SchemaConverters.toAvroType |  Major | SQL | Arun Mahadevan | Arun Mahadevan |
| [SPARK-25253](https://issues.apache.org/jira/browse/SPARK-25253) | Refactor pyspark connection & authentication |  Minor | PySpark | Imran Rashid | Imran Rashid |
| [SPARK-25235](https://issues.apache.org/jira/browse/SPARK-25235) | Merge the REPL code in Scala 2.11 and 2.12 branches |  Major | Spark Shell | DB Tsai | DB Tsai |
| [SPARK-25233](https://issues.apache.org/jira/browse/SPARK-25233) | Give the user the option of specifying a fixed minimum message per partition per batch when using kafka direct API with backpressure |  Major | DStreams | Reza Safi | Reza Safi |
| [SPARK-25287](https://issues.apache.org/jira/browse/SPARK-25287) | Check for JIRA\_USERNAME and JIRA\_PASSWORD up front in merge\_spark\_pr.py |  Minor | Project Infra | Erik Erlandson | Erik Erlandson |
| [SPARK-25286](https://issues.apache.org/jira/browse/SPARK-25286) | Remove dangerous parmap |  Major | Spark Core | Maxim Gekk | Maxim Gekk |
| [SPARK-23466](https://issues.apache.org/jira/browse/SPARK-23466) | Remove redundant null checks in generated Java code by GenerateUnsafeProjection |  Major | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-25117](https://issues.apache.org/jira/browse/SPARK-25117) | Add EXEPT ALL and INTERSECT ALL support in R. |  Major | SparkR | Dilip Biswal | Dilip Biswal |
| [SPARK-24962](https://issues.apache.org/jira/browse/SPARK-24962) | refactor CodeGenerator.createUnsafeArray |  Major | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-25300](https://issues.apache.org/jira/browse/SPARK-25300) | Unified the configuration parameter \`spark.shuffle.service.enabled\` |  Minor | Spark Core | liuxian | liuxian |
| [SPARK-25228](https://issues.apache.org/jira/browse/SPARK-25228) | Add executor CPU Time metric |  Minor | Spark Core | Luca Canali | Luca Canali |
| [SPARK-22666](https://issues.apache.org/jira/browse/SPARK-22666) | Spark datasource for image format |  Major | ML | Timothy Hunter | Weichen Xu |
| [SPARK-25335](https://issues.apache.org/jira/browse/SPARK-25335) | Skip Zinc downloading if it's installed in the system |  Minor | Build | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25252](https://issues.apache.org/jira/browse/SPARK-25252) | Support arrays of any types in to\_json |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25108](https://issues.apache.org/jira/browse/SPARK-25108) | Dataset.show() generates incorrect padding for Unicode Character |  Minor | SQL | xuejianbest | xuejianbest |
| [SPARK-25375](https://issues.apache.org/jira/browse/SPARK-25375) | Reenable qualified perm. function checks in UDFSuite |  Minor | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24999](https://issues.apache.org/jira/browse/SPARK-24999) | Reduce unnecessary 'new' memory operations |  Major | SQL | caoxuewen | caoxuewen |
| [SPARK-24156](https://issues.apache.org/jira/browse/SPARK-24156) | Enable no-data micro batches for more eager streaming state clean up |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23672](https://issues.apache.org/jira/browse/SPARK-23672) | Document Support returning lists in Arrow UDFs |  Major | PySpark, SQL | Holden Karau | Holden Karau |
| [SPARK-25241](https://issues.apache.org/jira/browse/SPARK-25241) | Configurable empty values when reading/writing CSV files |  Minor | SQL | Mario Molina | Mario Molina |
| [SPARK-23820](https://issues.apache.org/jira/browse/SPARK-23820) | Allow the long form of call sites to be recorded in the log |  Trivial | Spark Core | Michael Mior | Michael Mior |
| [SPARK-25170](https://issues.apache.org/jira/browse/SPARK-25170) | Add Task Metrics description to the documentation |  Minor | Spark Core | Luca Canali | Luca Canali |
| [SPARK-25400](https://issues.apache.org/jira/browse/SPARK-25400) | Increase timeouts in schedulerIntegrationSuite |  Major | Scheduler, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-25445](https://issues.apache.org/jira/browse/SPARK-25445) | publish a scala 2.12 build with Spark 2.4 |  Major | Build | Wenchen Fan | Wenchen Fan |
| [SPARK-24626](https://issues.apache.org/jira/browse/SPARK-24626) | Parallelize size calculation in Analyze Table command |  Major | SQL | Achuth Narayan Rajagopal | Reynold Xin |
| [SPARK-19724](https://issues.apache.org/jira/browse/SPARK-19724) | create a managed table with an existed default location should throw an exception |  Major | SQL | Song Jun | Gengliang Wang |
| [SPARK-25384](https://issues.apache.org/jira/browse/SPARK-25384) | Clarify fromJsonForceNullableSchema will be removed in Spark 3.0 |  Trivial | SQL | Maxim Gekk | Reynold Xin |
| [SPARK-25469](https://issues.apache.org/jira/browse/SPARK-25469) | Eval methods of Concat, Reverse and ElementAt should use pattern matching only once |  Major | SQL | Marek Novotny | Marek Novotny |
| [SPARK-21318](https://issues.apache.org/jira/browse/SPARK-21318) | The exception message thrown by \`lookupFunction\` is ambiguous. |  Minor | SQL | StanZhai | StanZhai |
| [SPARK-20937](https://issues.apache.org/jira/browse/SPARK-20937) | Describe spark.sql.parquet.writeLegacyFormat property in Spark SQL, DataFrames and Datasets Guide |  Trivial | Documentation, SQL | Jacek Laskowski | Chenxiao Mao |
| [SPARK-25318](https://issues.apache.org/jira/browse/SPARK-25318) | Add exception handling when wrapping the input stream during the the fetch or stage retry in response to a corrupted block |  Minor | Spark Core | Reza Safi | Reza Safi |
| [SPARK-25639](https://issues.apache.org/jira/browse/SPARK-25639) | Add documentation on foreachBatch, and multiple watermark policy |  Blocker | Documentation | Tathagata Das | Tathagata Das |
| [SPARK-25754](https://issues.apache.org/jira/browse/SPARK-25754) | Change CDN for MathJax |  Trivial | Documentation | Gengliang Wang | Gengliang Wang |
| [SPARK-25859](https://issues.apache.org/jira/browse/SPARK-25859) | add scala/java/python example and doc for PrefixSpan |  Major | ML | Huaxin Gao | Huaxin Gao |
| [SPARK-23012](https://issues.apache.org/jira/browse/SPARK-23012) | Support for predicate pushdown and partition pruning when left joining large Hive tables |  Major | Optimizer, SQL | Rick Kramer |  |
| [SPARK-25261](https://issues.apache.org/jira/browse/SPARK-25261) | Standardize the default units of spark.driver\|executor.memory |  Minor | Kubernetes, Spark Core, YARN | huangtengfei | huangtengfei |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-22949](https://issues.apache.org/jira/browse/SPARK-22949) | Reduce memory requirement for TrainValidationSplit |  Critical | ML | Bago Amirbekian | Bago Amirbekian |
| [SPARK-23028](https://issues.apache.org/jira/browse/SPARK-23028) | Bump master branch version to 2.4.0-SNAPSHOT |  Major | Build | Xiao Li | Xiao Li |
| [SPARK-23038](https://issues.apache.org/jira/browse/SPARK-23038) | Update docker/spark-test (JDK/OS) |  Minor | Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23044](https://issues.apache.org/jira/browse/SPARK-23044) | merge script has bug when assigning jiras to non-contributors |  Minor | Project Infra | Imran Rashid | Imran Rashid |
| [SPARK-20947](https://issues.apache.org/jira/browse/SPARK-20947) | Encoding/decoding issue in PySpark pipe implementation |  Major | PySpark | Xiaozhe Wang | Xiaozhe Wang |
| [SPARK-17088](https://issues.apache.org/jira/browse/SPARK-17088) | IsolatedClientLoader fails to load Hive client when sharesHadoopClasses is false |  Minor | SQL | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-22577](https://issues.apache.org/jira/browse/SPARK-22577) | executor page blacklist status should update with TaskSet level blacklisting |  Major | Scheduler, Spark Core | Thomas Graves | Attila Zsolt Piros |
| [SPARK-23152](https://issues.apache.org/jira/browse/SPARK-23152) | Invalid guard condition in org.apache.spark.ml.classification.Classifier |  Minor | ML, MLlib | Matthew Tovbin | Matthew Tovbin |
| [SPARK-22297](https://issues.apache.org/jira/browse/SPARK-22297) | Flaky test: BlockManagerSuite "Shuffle registration timeout and maxAttempts conf" |  Minor | Spark Core, Tests | Marcelo Masiero Vanzin | Mark Petruska |
| [SPARK-23059](https://issues.apache.org/jira/browse/SPARK-23059) | Correct some improper with view related method usage |  Minor | SQL, Tests | Bo Xu | Bo Xu |
| [SPARK-23088](https://issues.apache.org/jira/browse/SPARK-23088) | History server not showing incomplete/running applications |  Minor | Spark Core, Web UI | paul mackles | paul mackles |
| [SPARK-21525](https://issues.apache.org/jira/browse/SPARK-21525) | ReceiverSupervisorImpl seems to ignore the error code when writing to the WAL |  Major | DStreams | Mark Grover | Marcelo Masiero Vanzin |
| [SPARK-23020](https://issues.apache.org/jira/browse/SPARK-23020) | Re-enable Flaky Test: org.apache.spark.launcher.SparkLauncherSuite.testInProcessLauncher |  Blocker | Tests | Sameer Agarwal | Marcelo Masiero Vanzin |
| [SPARK-23306](https://issues.apache.org/jira/browse/SPARK-23306) | Race condition in TaskMemoryManager |  Minor | Spark Core | Zhan Zhang | Zhan Zhang |
| [SPARK-23189](https://issues.apache.org/jira/browse/SPARK-23189) | reflect stage level blacklisting on executor tab |  Major | Web UI | Attila Zsolt Piros | Attila Zsolt Piros |
| [SPARK-23394](https://issues.apache.org/jira/browse/SPARK-23394) | Storage info's Cached Partitions doesn't consider the replications (but sc.getRDDStorageInfo does) |  Major | Spark Core | Attila Zsolt Piros | Attila Zsolt Piros |
| [SPARK-23406](https://issues.apache.org/jira/browse/SPARK-23406) | Stream-stream self joins does not work |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23340](https://issues.apache.org/jira/browse/SPARK-23340) | Upgrade Apache ORC to 1.4.3 |  Major | Build, SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23377](https://issues.apache.org/jira/browse/SPARK-23377) | Bucketizer with multiple columns persistence bug |  Blocker | ML | Bago Amirbekian | L. C. Hsieh |
| [SPARK-23457](https://issues.apache.org/jira/browse/SPARK-23457) | Register task completion listeners first for ParquetFileFormat |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23436](https://issues.apache.org/jira/browse/SPARK-23436) | Incorrect Date column Inference in partition discovery |  Major | SQL | Apoorva Sareen | Marco Gaido |
| [SPARK-23240](https://issues.apache.org/jira/browse/SPARK-23240) | PythonWorkerFactory issues unhelpful message when pyspark.daemon produces bogus stdout |  Minor | PySpark | Bruce Robbins | Bruce Robbins |
| [SPARK-23434](https://issues.apache.org/jira/browse/SPARK-23434) | Spark should not warn \`metadata directory\` for a HDFS file path |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23476](https://issues.apache.org/jira/browse/SPARK-23476) | Spark will not start in local mode with authentication on |  Minor | Spark Core, Spark Shell | Gabor Somogyi | Gabor Somogyi |
| [SPARK-23490](https://issues.apache.org/jira/browse/SPARK-23490) | Check storage.locationUri with existing table in CreateTable |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23408](https://issues.apache.org/jira/browse/SPARK-23408) | Flaky test: StreamingOuterJoinSuite.left outer early state exclusion on right |  Minor | SQL, Tests | Marcelo Masiero Vanzin | Tathagata Das |
| [SPARK-23459](https://issues.apache.org/jira/browse/SPARK-23459) | Improve the error message when unknown column is specified in partition columns |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-23438](https://issues.apache.org/jira/browse/SPARK-23438) | DStreams could lose blocks with WAL enabled when driver crashes |  Critical | DStreams | Gabor Somogyi | Gabor Somogyi |
| [SPARK-23449](https://issues.apache.org/jira/browse/SPARK-23449) | Extra java options lose order in Docker context |  Minor | Kubernetes, Spark Core | Andrew Korzhuev | Andrew Korzhuev |
| [SPARK-17147](https://issues.apache.org/jira/browse/SPARK-17147) | Spark Streaming Kafka 0.10 Consumer Can't Handle Non-consecutive Offsets (i.e. Log Compaction) |  Major | DStreams | Robert Conrad | Cody Koeninger |
| [SPARK-23523](https://issues.apache.org/jira/browse/SPARK-23523) | Incorrect result caused by the rule OptimizeMetadataOnlyQuery |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-23365](https://issues.apache.org/jira/browse/SPARK-23365) | DynamicAllocation with failure in straggler task can lead to a hung spark job |  Major | Scheduler, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-23417](https://issues.apache.org/jira/browse/SPARK-23417) | pyspark tests give wrong sbt instructions |  Minor | PySpark | Jose Torres | Bruce Robbins |
| [SPARK-23508](https://issues.apache.org/jira/browse/SPARK-23508) | blockManagerIdCache in BlockManagerId may cause oom |  Major | Deploy, Spark Core | zhoukang | zhoukang |
| [SPARK-23514](https://issues.apache.org/jira/browse/SPARK-23514) | Replace spark.sparkContext.hadoopConfiguration by spark.sessionState.newHadoopConf() |  Major | SQL | Xiao Li | Juliusz Sompolski |
| [SPARK-23405](https://issues.apache.org/jira/browse/SPARK-23405) | The task will hang up when a small table left semi join a big table |  Major | SQL | KaiXinXIaoLei | KaiXinXIaoLei |
| [SPARK-23551](https://issues.apache.org/jira/browse/SPARK-23551) | Exclude \`hadoop-mapreduce-client-core\` dependency from \`orc-mapreduce\` |  Minor | Build | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23570](https://issues.apache.org/jira/browse/SPARK-23570) | Add Spark-2.3 in HiveExternalCatalogVersionsSuite |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-23569](https://issues.apache.org/jira/browse/SPARK-23569) | pandas\_udf does not work with type-annotated python functions |  Major | PySpark | Stu (Michael Stewart) | Stu (Michael Stewart) |
| [SPARK-23496](https://issues.apache.org/jira/browse/SPARK-23496) | Locality of coalesced partitions can be severely skewed by the order of input partitions |  Major | Spark Core | Ala Luszczak | Ala Luszczak |
| [SPARK-22430](https://issues.apache.org/jira/browse/SPARK-22430) | Unknown tag warnings when building R docs with Roxygen 6.0.1 |  Trivial | Documentation | Joel Croteau | Rekha Joshi |
| [SPARK-18630](https://issues.apache.org/jira/browse/SPARK-18630) | PySpark ML memory leak |  Minor | ML, PySpark | Holden Karau | yogesh garg |
| [SPARK-23291](https://issues.apache.org/jira/browse/SPARK-23291) | SparkR : substr : In SparkR dataframe , starting and ending position arguments in "substr" is giving wrong result  when the position is greater than 1 |  Major | SparkR | Narendra | L. C. Hsieh |
| [SPARK-23525](https://issues.apache.org/jira/browse/SPARK-23525) | ALTER TABLE CHANGE COLUMN COMMENT doesn't work for external hive table |  Major | SQL | Pavlo Skliar | Xingbo Jiang |
| [SPARK-23524](https://issues.apache.org/jira/browse/SPARK-23524) | Big local shuffle blocks should not be checked for corruption. |  Major | Spark Core | Jin Xing | Jin Xing |
| [SPARK-23620](https://issues.apache.org/jira/browse/SPARK-23620) | Split thread dump lines by using the br tag |  Minor | Web UI | Maxim Gekk | Maxim Gekk |
| [SPARK-23522](https://issues.apache.org/jira/browse/SPARK-23522) | pyspark should always use sys.exit rather than exit |  Major | PySpark | Benjamin Peterson | Benjamin Peterson |
| [SPARK-23602](https://issues.apache.org/jira/browse/SPARK-23602) | PrintToStderr should behave the same in interpreted mode |  Trivial | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23271](https://issues.apache.org/jira/browse/SPARK-23271) | Parquet output contains only "\_SUCCESS" file after empty DataFrame saving |  Minor | SQL | Pavlo Z. | Dilip Biswal |
| [SPARK-23630](https://issues.apache.org/jira/browse/SPARK-23630) | Spark-on-YARN missing user customizations of hadoop config |  Major | Spark Core, YARN | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23173](https://issues.apache.org/jira/browse/SPARK-23173) | from\_json can produce nulls for fields which are marked as non-nullable |  Major | SQL | Herman van Hövell | Michał Świtakowski |
| [SPARK-23462](https://issues.apache.org/jira/browse/SPARK-23462) | Improve the error message in \`StructType\` |  Major | SQL | Xiao Li | Xiayun Sun |
| [SPARK-23618](https://issues.apache.org/jira/browse/SPARK-23618) | docker-image-tool.sh Fails While Building Image |  Major | Kubernetes, Spark Core | Ninad Ingole |  |
| [SPARK-23547](https://issues.apache.org/jira/browse/SPARK-23547) | Cleanup the .pipeout file when the Hive Session closed |  Major | SQL | zuotingbing | zuotingbing |
| [SPARK-23598](https://issues.apache.org/jira/browse/SPARK-23598) | WholeStageCodegen can lead to IllegalAccessError  calling append for HashAggregateExec |  Major | Spark Core | David Vogelbacher | Kazuaki Ishizaki |
| [SPARK-23658](https://issues.apache.org/jira/browse/SPARK-23658) | InProcessAppHandle uses the wrong class in getLogger |  Minor | Spark Submit | Sahil Takiar | Sahil Takiar |
| [SPARK-23671](https://issues.apache.org/jira/browse/SPARK-23671) | SHS is ignoring number of replay threads |  Critical | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23608](https://issues.apache.org/jira/browse/SPARK-23608) | SHS needs synchronization between attachSparkUI and detachSparkUI functions |  Minor | Spark Core, Web UI | Ye Zhou | Ye Zhou |
| [SPARK-23670](https://issues.apache.org/jira/browse/SPARK-23670) | Memory leak of SparkPlanGraphWrapper in sparkUI |  Major | SQL | Myroslav Lisniak | Myroslav Lisniak |
| [SPARK-23635](https://issues.apache.org/jira/browse/SPARK-23635) | Spark executor env variable is overwritten by same name AM env variable |  Minor | Spark Core, YARN | Saisai Shao | Saisai Shao |
| [SPARK-18371](https://issues.apache.org/jira/browse/SPARK-18371) | Spark Streaming backpressure bug - generates a batch with large number of records |  Major | DStreams | mapreduced | Sebastian Arzt |
| [SPARK-23623](https://issues.apache.org/jira/browse/SPARK-23623) | Avoid concurrent use of cached KafkaConsumer in CachedKafkaConsumer (kafka-0-10-sql) |  Critical | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23660](https://issues.apache.org/jira/browse/SPARK-23660) | Yarn throws exception in cluster mode when the application is small |  Minor | Spark Core, YARN | Gabor Somogyi | Gabor Somogyi |
| [SPARK-23574](https://issues.apache.org/jira/browse/SPARK-23574) | SinglePartition in data source V2 scan |  Major | Spark Core | Jose Torres | Jose Torres |
| [SPARK-23666](https://issues.apache.org/jira/browse/SPARK-23666) | Undeterministic column name with UDFs |  Minor | SQL | Daniel Darabos | Takeshi Yamamuro |
| [SPARK-23288](https://issues.apache.org/jira/browse/SPARK-23288) | Incorrect number of written records in structured streaming |  Major | SQL, Structured Streaming | Yuriy Bondaruk | Gabor Somogyi |
| [SPARK-23729](https://issues.apache.org/jira/browse/SPARK-23729) | Glob resolution breaks remote naming of files/archives |  Major | Spark Submit | Mihaly Toth | Mihaly Toth |
| [SPARK-23760](https://issues.apache.org/jira/browse/SPARK-23760) | CodegenContext.withSubExprEliminationExprs should save/restore CSE state correctly |  Major | SQL | Kris Mok | Kris Mok |
| [SPARK-23599](https://issues.apache.org/jira/browse/SPARK-23599) | The UUID() expression is too non-deterministic |  Critical | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-23614](https://issues.apache.org/jira/browse/SPARK-23614) | Union produces incorrect results when caching is used |  Major | SQL | Morten Hornbech | L. C. Hsieh |
| [SPARK-23361](https://issues.apache.org/jira/browse/SPARK-23361) | Driver restart fails if it happens after 7 days from app submission |  Major | Spark Core, YARN | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23759](https://issues.apache.org/jira/browse/SPARK-23759) | Unable to bind Spark UI to specific host name / IP |  Major | Spark Core, Web UI | Felix Albani | Felix Albani |
| [SPARK-21685](https://issues.apache.org/jira/browse/SPARK-21685) | Params isSet in scala Transformer triggered by \_setDefault in pyspark |  Major | PySpark | Ratan Rai Sur | Bryan Cutler |
| [SPARK-23788](https://issues.apache.org/jira/browse/SPARK-23788) | Race condition in StreamingQuerySuite |  Minor | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23549](https://issues.apache.org/jira/browse/SPARK-23549) | Spark SQL unexpected behavior when comparing timestamp to date |  Major | SQL | Dong Jiang | Kazuaki Ishizaki |
| [SPARK-23787](https://issues.apache.org/jira/browse/SPARK-23787) | SparkSubmitSuite::"download remote resource if it is not supported by yarn" fails on Hadoop 2.9 |  Minor | Spark Core, Tests | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23794](https://issues.apache.org/jira/browse/SPARK-23794) | UUID() should be stateful |  Major | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-23806](https://issues.apache.org/jira/browse/SPARK-23806) | Broadcast. unpersist can cause fatal exception when used with dynamic allocation |  Major | Spark Core | Thomas Graves | Thomas Graves |
| [SPARK-23785](https://issues.apache.org/jira/browse/SPARK-23785) | LauncherBackend doesn't check state of connection before setting state |  Major | Spark Core | Sahil Takiar | Sahil Takiar |
| [SPARK-23639](https://issues.apache.org/jira/browse/SPARK-23639) | SparkSQL CLI fails talk to Kerberized metastore when use proxy user |  Major | SQL | Kent Yao | Kent Yao |
| [SPARK-23808](https://issues.apache.org/jira/browse/SPARK-23808) | Test spark sessions should set default session |  Major | SQL | Jose Torres | Jose Torres |
| [SPARK-23743](https://issues.apache.org/jira/browse/SPARK-23743) | IsolatedClientLoader.isSharedClass returns an unindented result against \`slf4j\` keyword |  Minor | SQL | Jongyoul Lee | Jongyoul Lee |
| [SPARK-23640](https://issues.apache.org/jira/browse/SPARK-23640) | Hadoop config may override spark config |  Major | Spark Core | Yuming Wang | Yuming Wang |
| [SPARK-23827](https://issues.apache.org/jira/browse/SPARK-23827) | StreamingJoinExec should ensure that input data is partitioned into specific number of partitions |  Critical | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23825](https://issues.apache.org/jira/browse/SPARK-23825) | [K8s] Spark pods should request memory + memoryOverhead as resources |  Major | Kubernetes, Spark Core | David Vogelbacher |  |
| [SPARK-23834](https://issues.apache.org/jira/browse/SPARK-23834) | Flaky test: LauncherServerSuite.testAppHandleDisconnect |  Major | Tests | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-23802](https://issues.apache.org/jira/browse/SPARK-23802) | PropagateEmptyRelation can leave query plan in unresolved state |  Minor | SQL | Robert Kruszewski | Robert Kruszewski |
| [SPARK-23868](https://issues.apache.org/jira/browse/SPARK-23868) | Fix scala.MatchError in literals.sql.out |  Major | SQL | Xiao Li | Takeshi Yamamuro |
| [SPARK-23637](https://issues.apache.org/jira/browse/SPARK-23637) | Yarn might allocate more resource if a same executor is killed multiple times. |  Major | Spark Core, YARN | Jin Xing | Jin Xing |
| [SPARK-23823](https://issues.apache.org/jira/browse/SPARK-23823) | ResolveReferences loses correct origin |  Major | SQL | Jiahui Jiang | Jiahui Jiang |
| [SPARK-23882](https://issues.apache.org/jira/browse/SPARK-23882) | Is UTF8StringSuite.writeToOutputStreamUnderflow() supported? |  Minor | Spark Core | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-23809](https://issues.apache.org/jira/browse/SPARK-23809) | Active SparkSession should be set by getOrCreate |  Minor | SQL | Eric Liang | Eric Liang |
| [SPARK-23893](https://issues.apache.org/jira/browse/SPARK-23893) | Possible overflow in long = int \* int |  Minor | Spark Core, SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-23816](https://issues.apache.org/jira/browse/SPARK-23816) | FetchFailedException when killing speculative task |  Major | SQL | chen xiao | Imran Rashid |
| [SPARK-23951](https://issues.apache.org/jira/browse/SPARK-23951) | Use java classed in ExprValue and simplify a bunch of stuff |  Major | SQL | Herman van Hövell | Herman van Hövell |
| [SPARK-6951](https://issues.apache.org/jira/browse/SPARK-6951) | History server slow startup if the event log directory is large |  Major | Web UI | Matt Cheah | Marcelo Masiero Vanzin |
| [SPARK-23971](https://issues.apache.org/jira/browse/SPARK-23971) | Should not leak Spark sessions across test suites |  Major | SQL, Tests | Eric Liang | Eric Liang |
| [SPARK-23815](https://issues.apache.org/jira/browse/SPARK-23815) | Spark writer dynamic partition overwrite mode fails to write output on multi level partition |  Major | Spark Core | Fangshi Li | Fangshi Li |
| [SPARK-23835](https://issues.apache.org/jira/browse/SPARK-23835) | When Dataset.as converts column from nullable to non-nullable type, null Doubles are converted silently to -1 |  Major | SQL | Joseph K. Bradley | Marco Gaido |
| [SPARK-22676](https://issues.apache.org/jira/browse/SPARK-22676) | Avoid iterating all partition paths when spark.sql.hive.verifyPartitionPath=true |  Major | SQL | Jin Xing | Jin Xing |
| [SPARK-23986](https://issues.apache.org/jira/browse/SPARK-23986) | CompileException when using too many avg aggregation after joining |  Major | SQL | Michel Davit | Marco Gaido |
| [SPARK-22968](https://issues.apache.org/jira/browse/SPARK-22968) | java.lang.IllegalStateException: No current assignment for partition kssh-2 |  Major | Spark Core | Jepson | Saisai Shao |
| [SPARK-21479](https://issues.apache.org/jira/browse/SPARK-21479) | Outer join filter pushdown in null supplying table when condition is on one of the joined columns |  Major | Optimizer, SQL | Abhijit Bhole | Wei Xue |
| [SPARK-24007](https://issues.apache.org/jira/browse/SPARK-24007) | EqualNullSafe for FloatType and DoubleType might generate a wrong result by codegen. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-21811](https://issues.apache.org/jira/browse/SPARK-21811) | Inconsistency when finding the widest common type of a combination of DateType, StringType, and NumericType |  Minor | SQL | Ryan Bald | Xingbo Jiang |
| [SPARK-23989](https://issues.apache.org/jira/browse/SPARK-23989) | When using \`SortShuffleWriter\`, the data will be overwritten |  Critical | Spark Core | liuxian | Wenchen Fan |
| [SPARK-23976](https://issues.apache.org/jira/browse/SPARK-23976) | UTF8String.concat() or ByteArray.concat() may allocate shorter structure. |  Minor | Spark Core | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-24022](https://issues.apache.org/jira/browse/SPARK-24022) | Flaky test: SparkContextSuite |  Major | Spark Core, Tests | Gabor Somogyi | Gabor Somogyi |
| [SPARK-24033](https://issues.apache.org/jira/browse/SPARK-24033) | LAG Window function broken in Spark 2.3 |  Major | SQL | Emlyn Corrin | Xiao Li |
| [SPARK-23799](https://issues.apache.org/jira/browse/SPARK-23799) | [CBO] FilterEstimation.evaluateInSet produces devision by zero in a case of empty table with analyzed statistics |  Major | Optimizer, SQL | Michael Shtelma | Michael Shtelma |
| [SPARK-21168](https://issues.apache.org/jira/browse/SPARK-21168) | KafkaRDD should always set kafka clientId. |  Trivial | DStreams | Xingxing Di | liuzhaokun |
| [SPARK-23004](https://issues.apache.org/jira/browse/SPARK-23004) | Structured Streaming raise "llegalStateException: Cannot remove after already committed or aborted" |  Major | Structured Streaming | secfree | Tathagata Das |
| [SPARK-23888](https://issues.apache.org/jira/browse/SPARK-23888) | speculative task should not run on a given host where another attempt is already running on |  Major | Scheduler, Spark Core | wuyi | wuyi |
| [SPARK-24002](https://issues.apache.org/jira/browse/SPARK-24002) | Task not serializable caused by org.apache.parquet.io.api.Binary$ByteBufferBackedBinary.getBytes |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-24056](https://issues.apache.org/jira/browse/SPARK-24056) | Make consumer creation lazy in Kafka source for Structured streaming |  Minor | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24012](https://issues.apache.org/jira/browse/SPARK-24012) | Union of map and other compatible column |  Major | SQL | Lijia Liu | Lijia Liu |
| [SPARK-24050](https://issues.apache.org/jira/browse/SPARK-24050) | StreamingQuery does not calculate input / processing rates in some cases |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24062](https://issues.apache.org/jira/browse/SPARK-24062) | SASL encryption cannot be worked in ThriftServer |  Major | Spark Core, SQL | Saisai Shao | Saisai Shao |
| [SPARK-23355](https://issues.apache.org/jira/browse/SPARK-23355) | convertMetastore should not ignore table properties |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24085](https://issues.apache.org/jira/browse/SPARK-24085) | Scalar subquery error |  Major | SQL | Alexey Baturin | Dilip Biswal |
| [SPARK-24104](https://issues.apache.org/jira/browse/SPARK-24104) | SQLAppStatusListener overwrites metrics onDriverAccumUpdates instead of updating them |  Major | SQL | Juliusz Sompolski | Juliusz Sompolski |
| [SPARK-23094](https://issues.apache.org/jira/browse/SPARK-23094) | Json Readers choose wrong encoding when bad records are present and fail |  Major | SQL | Burak Yavuz | Maxim Gekk |
| [SPARK-23853](https://issues.apache.org/jira/browse/SPARK-23853) | Skip doctests which require hive support built in PySpark |  Trivial | PySpark, SQL | Holden Karau | Dongjoon Hyun |
| [SPARK-24061](https://issues.apache.org/jira/browse/SPARK-24061) | [SS]TypedFilter is not supported in Continuous Processing |  Major | SQL | Wang Yanlin | Wang Yanlin |
| [SPARK-23941](https://issues.apache.org/jira/browse/SPARK-23941) | Mesos task failed on specific spark app name |  Major | Mesos, Spark Submit | bounkong khamphousone | bounkong khamphousone |
| [SPARK-24107](https://issues.apache.org/jira/browse/SPARK-24107) | ChunkedByteBuffer.writeFully method has not reset the limit value |  Blocker | Block Manager, Input/Output, Spark Core | jinhai | jinhai |
| [SPARK-24013](https://issues.apache.org/jira/browse/SPARK-24013) | ApproximatePercentile grinds to a halt on sorted input. |  Major | SQL | Juliusz Sompolski | Marco Gaido |
| [SPARK-24133](https://issues.apache.org/jira/browse/SPARK-24133) | Reading Parquet files containing large strings can fail with java.lang.ArrayIndexOutOfBoundsException |  Major | SQL | Ala Luszczak | Ala Luszczak |
| [SPARK-24123](https://issues.apache.org/jira/browse/SPARK-24123) | Fix a flaky test \`DateTimeUtilsSuite.monthsBetween\` |  Minor | SQL | Dongjoon Hyun | Marco Gaido |
| [SPARK-24110](https://issues.apache.org/jira/browse/SPARK-24110) | Avoid calling UGI loginUserFromKeytab in ThriftServer |  Major | SQL | Saisai Shao | Saisai Shao |
| [SPARK-23489](https://issues.apache.org/jira/browse/SPARK-23489) | Flaky Test: HiveExternalCatalogVersionsSuite |  Major | SQL, Tests | Marco Gaido | Dongjoon Hyun |
| [SPARK-24166](https://issues.apache.org/jira/browse/SPARK-24166) | InMemoryTableScanExec should not access SQLConf at executor side |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24169](https://issues.apache.org/jira/browse/SPARK-24169) | JsonToStructs should not access SQLConf at executor side |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-23433](https://issues.apache.org/jira/browse/SPARK-23433) | java.lang.IllegalStateException: more than one active taskSet for stage |  Major | Spark Core | Shixiong Zhu | Imran Rashid |
| [SPARK-24168](https://issues.apache.org/jira/browse/SPARK-24168) | WindowExec should not access SQLConf at executor side |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24167](https://issues.apache.org/jira/browse/SPARK-24167) | ParquetFilters should not access SQLConf at executor side |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-23697](https://issues.apache.org/jira/browse/SPARK-23697) | Accumulators of Spark 1.x no longer work with Spark 2.x |  Major | Spark Core | Sergey Zhemzhitsky | Wenchen Fan |
| [SPARK-24143](https://issues.apache.org/jira/browse/SPARK-24143) | filter empty blocks when convert mapstatus to (blockId, size) pair |  Major | Spark Core | Jin Xing | Jin Xing |
| [SPARK-23775](https://issues.apache.org/jira/browse/SPARK-23775) | Flaky test: DataFrameRangeSuite |  Major | SQL, Tests | Gabor Somogyi | Gabor Somogyi |
| [SPARK-24043](https://issues.apache.org/jira/browse/SPARK-24043) | InterpretedPredicate.eval fails if expression tree contains Nondeterministic expressions |  Minor | SQL | Bruce Robbins | Bruce Robbins |
| [SPARK-15750](https://issues.apache.org/jira/browse/SPARK-15750) | Constructing FPGrowth fails when no numPartitions specified in pyspark |  Major | MLlib, PySpark | Jeff Zhang | Jeff Zhang |
| [SPARK-23975](https://issues.apache.org/jira/browse/SPARK-23975) | Allow Clustering to take Arrays of Double as input features |  Major | ML | Lu Wang | Lu Wang |
| [SPARK-24076](https://issues.apache.org/jira/browse/SPARK-24076) | very bad performance when shuffle.partition = 8192 |  Major | SQL | yucai | yucai |
| [SPARK-24068](https://issues.apache.org/jira/browse/SPARK-24068) | CSV schema inferring doesn't work for compressed files |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24214](https://issues.apache.org/jira/browse/SPARK-24214) | StreamingRelationV2/StreamingExecutionRelation/ContinuousExecutionRelation.toJSON should not fail |  Major | Structured Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-24141](https://issues.apache.org/jira/browse/SPARK-24141) | Fix bug in CoarseGrainedSchedulerBackend.killExecutors |  Critical | Spark Core | wuyi | wuyi |
| [SPARK-23852](https://issues.apache.org/jira/browse/SPARK-23852) | Parquet MR bug can lead to incorrect SQL results |  Blocker | SQL | Henry Robinson | Ryan Blue |
| [SPARK-22279](https://issues.apache.org/jira/browse/SPARK-22279) | Turn on spark.sql.hive.convertMetastoreOrc by default |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24137](https://issues.apache.org/jira/browse/SPARK-24137) | [K8s] Mount temporary directories in emptydir volumes |  Major | Kubernetes, Spark Core | Matt Cheah | Matt Cheah |
| [SPARK-19181](https://issues.apache.org/jira/browse/SPARK-19181) | SparkListenerSuite.local metrics fails when average executorDeserializeTime is too short. |  Minor | Tests | Jose Soltren | Attila Zsolt Piros |
| [SPARK-10878](https://issues.apache.org/jira/browse/SPARK-10878) | Race condition when resolving Maven coordinates via Ivy |  Minor | Spark Core | Ryan Williams | Kazuaki Ishizaki |
| [SPARK-24255](https://issues.apache.org/jira/browse/SPARK-24255) | Require Java 8 in SparkR description |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-17916](https://issues.apache.org/jira/browse/SPARK-17916) | CSV data source treats empty string as null no matter what nullValue option is |  Major | SQL | Hossein Falaki | Maxim Gekk |
| [SPARK-24228](https://issues.apache.org/jira/browse/SPARK-24228) | Fix the lint error |  Minor | Build | Xiao Li |  |
| [SPARK-24263](https://issues.apache.org/jira/browse/SPARK-24263) | SparkR java check breaks on openjdk |  Blocker | SparkR | Felix Cheung | Felix Cheung |
| [SPARK-23780](https://issues.apache.org/jira/browse/SPARK-23780) | Failed to use googleVis library with new SparkR |  Major | SparkR | Ivan Dzikovsky | Felix Cheung |
| [SPARK-24241](https://issues.apache.org/jira/browse/SPARK-24241) | Do not fail fast when dynamic resource allocation enabled with 0 executor |  Minor | Spark Submit | Kent Yao | Kent Yao |
| [SPARK-24259](https://issues.apache.org/jira/browse/SPARK-24259) | ArrayWriter for Arrow produces wrong output |  Critical | PySpark, SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-21945](https://issues.apache.org/jira/browse/SPARK-21945) | pyspark --py-files doesn't work in yarn client mode |  Major | PySpark | Thomas Graves | Hyukjin Kwon |
| [SPARK-22371](https://issues.apache.org/jira/browse/SPARK-22371) | dag-scheduler-event-loop thread stopped with error  Attempted to access garbage collected accumulator 5605982 |  Major | Spark Core | Mayank Agarwal | Artem Rudoy |
| [SPARK-23850](https://issues.apache.org/jira/browse/SPARK-23850) | We should not redact username\|user\|url from UI by default |  Major | Web UI | Thomas Graves | Marcelo Masiero Vanzin |
| [SPARK-23857](https://issues.apache.org/jira/browse/SPARK-23857) | In mesos cluster mode spark submit requires the keytab to be available on the local file system. |  Minor | Mesos | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-24309](https://issues.apache.org/jira/browse/SPARK-24309) | AsyncEventQueue should handle an interrupt from a Listener |  Blocker | Scheduler, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-21673](https://issues.apache.org/jira/browse/SPARK-21673) | Spark local directory is not set correctly |  Major | Block Manager, Mesos, Spark Core | Jake Charland | Jake Charland |
| [SPARK-24313](https://issues.apache.org/jira/browse/SPARK-24313) | Collection functions interpreted execution doesn't work with complex types |  Critical | SQL | Marco Gaido | Marco Gaido |
| [SPARK-24348](https://issues.apache.org/jira/browse/SPARK-24348) | scala.MatchError in the "element\_at" expression |  Major | SQL | Alex Vayda | Alex Vayda |
| [SPARK-19185](https://issues.apache.org/jira/browse/SPARK-19185) | ConcurrentModificationExceptions with CachedKafkaConsumers when Windowing |  Major | DStreams | Kalvin Chau | Gabor Somogyi |
| [SPARK-24294](https://issues.apache.org/jira/browse/SPARK-24294) | Throw SparkException when OOM in BroadcastExchangeExec |  Major | SQL | Jin Xing | Jin Xing |
| [SPARK-23416](https://issues.apache.org/jira/browse/SPARK-23416) | Flaky test: KafkaSourceStressForDontFailOnDataLossSuite.stress test for failOnDataLoss=false |  Minor | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-24257](https://issues.apache.org/jira/browse/SPARK-24257) | LongToUnsafeRowMap calculate the new size may be wrong |  Blocker | SQL | dzcxzl | dzcxzl |
| [SPARK-24322](https://issues.apache.org/jira/browse/SPARK-24322) | Upgrade Apache ORC to 1.4.4 |  Major | Build | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24364](https://issues.apache.org/jira/browse/SPARK-24364) | Files deletion after globbing may fail StructuredStreaming jobs |  Major | Structured Streaming | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24230](https://issues.apache.org/jira/browse/SPARK-24230) | With Parquet 1.10 upgrade has errors in the vectorized reader |  Major | SQL | Ian O Connell | Ryan Blue |
| [SPARK-24350](https://issues.apache.org/jira/browse/SPARK-24350) | ClassCastException in "array\_position" function |  Major | SQL | Alex Vayda |  |
| [SPARK-24368](https://issues.apache.org/jira/browse/SPARK-24368) | Flaky tests: org.apache.spark.sql.execution.datasources.csv.UnivocityParserSuite |  Major | SQL, Tests | Xiao Li | Maxim Gekk |
| [SPARK-15125](https://issues.apache.org/jira/browse/SPARK-15125) | CSV data source recognizes empty quoted strings in the input as null. |  Major | SQL | Suresh Thalamati |  |
| [SPARK-24373](https://issues.apache.org/jira/browse/SPARK-24373) | "df.cache() df.count()" no longer eagerly caches data when the analyzed plans are different after re-analyzing the plans |  Blocker | SQL | Wenbo Zhao | Marco Gaido |
| [SPARK-19613](https://issues.apache.org/jira/browse/SPARK-19613) | Flaky test: StateStoreRDDSuite |  Minor | Structured Streaming, Tests | Kay Ousterhout | Dongjoon Hyun |
| [SPARK-24377](https://issues.apache.org/jira/browse/SPARK-24377) | Make --py-files work in non pyspark application |  Minor | Spark Submit | Saisai Shao | Saisai Shao |
| [SPARK-23991](https://issues.apache.org/jira/browse/SPARK-23991) | data loss when allocateBlocksToBatch |  Major | DStreams, Input/Output | kevin fu | Gabor Somogyi |
| [SPARK-23754](https://issues.apache.org/jira/browse/SPARK-23754) | StopIterator exception in Python UDF results in partial result |  Blocker | PySpark | Li Jin | Emilio Dorigatti |
| [SPARK-24384](https://issues.apache.org/jira/browse/SPARK-24384) | spark-submit --py-files with .py files doesn't work in client mode before context initialization |  Major | PySpark, Spark Submit | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24276](https://issues.apache.org/jira/browse/SPARK-24276) | semanticHash() returns different values for semantically the same IS IN |  Minor | SQL | Maxim Gekk | Marco Gaido |
| [SPARK-23649](https://issues.apache.org/jira/browse/SPARK-23649) | CSV schema inferring fails on some UTF-8 chars |  Major | SQL | Maxim Gekk |  |
| [SPARK-24414](https://issues.apache.org/jira/browse/SPARK-24414) | Stages page doesn't show all task attempts when failures |  Critical | Web UI | Thomas Graves | Marcelo Masiero Vanzin |
| [SPARK-24351](https://issues.apache.org/jira/browse/SPARK-24351) | offsetLog/commitLog purge thresholdBatchId should be computed with current committed epoch but not currentBatchId in CP mode |  Major | Structured Streaming | huangtengfei | huangtengfei |
| [SPARK-24369](https://issues.apache.org/jira/browse/SPARK-24369) | A bug when having multiple distinct aggregations |  Major | SQL | Xiao Li | Wenchen Fan |
| [SPARK-23786](https://issues.apache.org/jira/browse/SPARK-23786) | CSV schema validation - column names are not checked |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-21896](https://issues.apache.org/jira/browse/SPARK-21896) | Stack Overflow when window function nested inside aggregate function |  Minor | PySpark, SQL | Luyao Yang | Anton Okolnychyi |
| [SPARK-24300](https://issues.apache.org/jira/browse/SPARK-24300) | generateLDAData in ml.cluster.LDASuite didn't set seed correctly |  Minor | ML | Xiangrui Meng | Lu Wang |
| [SPARK-16451](https://issues.apache.org/jira/browse/SPARK-16451) | Spark-shell / pyspark should finish gracefully when "SaslException: GSS initiate failed" is hit |  Major | . | Yesha Vora | Marcelo Masiero Vanzin |
| [SPARK-24453](https://issues.apache.org/jira/browse/SPARK-24453) | Fix error recovering from the failure in a no-data batch |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-22384](https://issues.apache.org/jira/browse/SPARK-22384) | Refine partition pruning when attribute is wrapped in Cast |  Major | SQL | Jin Xing | Jin Xing |
| [SPARK-17756](https://issues.apache.org/jira/browse/SPARK-17756) | java.lang.ClassCastException when using cartesian with DStream.transform |  Major | DStreams, PySpark | Maciej Szymkiewicz | Hyukjin Kwon |
| [SPARK-24468](https://issues.apache.org/jira/browse/SPARK-24468) | DecimalType \`adjustPrecisionScale\` might fail when scale is negative |  Minor | SQL | Yifei Wu | Marco Gaido |
| [SPARK-24520](https://issues.apache.org/jira/browse/SPARK-24520) | Double braces in link |  Trivial | Documentation | Fokko Driesprong | Fokko Driesprong |
| [SPARK-23732](https://issues.apache.org/jira/browse/SPARK-23732) | Broken link to scala source code in Spark Scala api Scaladoc |  Trivial | Build, Documentation, Project Infra | Yogesh Tewari | Marcelo Masiero Vanzin |
| [SPARK-24416](https://issues.apache.org/jira/browse/SPARK-24416) | Update configuration definition for spark.blacklist.killBlacklistedExecutors |  Minor | Spark Core | Sanket Reddy | Sanket Reddy |
| [SPARK-24216](https://issues.apache.org/jira/browse/SPARK-24216) | Spark TypedAggregateExpression uses getSimpleName that is not safe in scala |  Major | SQL | Fangshi Li | Fangshi Li |
| [SPARK-24506](https://issues.apache.org/jira/browse/SPARK-24506) | Spark.ui.filters not applied to /sqlserver/ url |  Major | Web UI | t oo | Marco Gaido |
| [SPARK-24466](https://issues.apache.org/jira/browse/SPARK-24466) | TextSocketMicroBatchReader no longer works with nc utility |  Major | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-24500](https://issues.apache.org/jira/browse/SPARK-24500) | UnsupportedOperationException when trying to execute Union plan with Stream of children |  Major | SQL | Bogdan Raducanu | Herman van Hövell |
| [SPARK-24531](https://issues.apache.org/jira/browse/SPARK-24531) | HiveExternalCatalogVersionsSuite failing due to missing 2.2.0 version |  Blocker | Tests | Marco Gaido | Marco Gaido |
| [SPARK-24495](https://issues.apache.org/jira/browse/SPARK-24495) | SortMergeJoin with duplicate keys wrong results |  Blocker | SQL | Bogdan Raducanu | Marco Gaido |
| [SPARK-24563](https://issues.apache.org/jira/browse/SPARK-24563) | Allow running PySpark shell without Hive |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-24319](https://issues.apache.org/jira/browse/SPARK-24319) | run-example can not print usage |  Minor | Spark Submit | Bryan Cutler | Gabor Somogyi |
| [SPARK-24452](https://issues.apache.org/jira/browse/SPARK-24452) | long = int\*int or long = int+int may cause overflow. |  Minor | Spark Core, SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-24573](https://issues.apache.org/jira/browse/SPARK-24573) | SBT Java checkstyle affecting the build |  Major | Project Infra | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24526](https://issues.apache.org/jira/browse/SPARK-24526) | Spaces in the build dir causes failures in the build/mvn script |  Minor | Build | Trystan Leftwich | Trystan Leftwich |
| [SPARK-24548](https://issues.apache.org/jira/browse/SPARK-24548) | JavaPairRDD to Dataset\<Row\> in SPARK generates ambiguous results |  Major | Java API, SQL | Jackson | L. C. Hsieh |
| [SPARK-24556](https://issues.apache.org/jira/browse/SPARK-24556) | ReusedExchange should rewrite output partitioning also when child's partitioning is RangePartitioning |  Major | SQL | yucai | yucai |
| [SPARK-24583](https://issues.apache.org/jira/browse/SPARK-24583) | Wrong schema type in InsertIntoDataSourceCommand |  Major | SQL | Wei Xue | Wei Xue |
| [SPARK-23778](https://issues.apache.org/jira/browse/SPARK-23778) | SparkContext.emptyRDD confuses SparkContext.union |  Trivial | Spark Core | Stefano Pettini | Marco Gaido |
| [SPARK-24578](https://issues.apache.org/jira/browse/SPARK-24578) | Reading remote cache block behavior changes and causes timeout issue |  Blocker | Spark Core | Wenbo Zhao | Wenbo Zhao |
| [SPARK-24613](https://issues.apache.org/jira/browse/SPARK-24613) | Cache with UDF could not be matched with subsequent dependent caches |  Minor | SQL | Wei Xue | Wei Xue |
| [SPARK-24589](https://issues.apache.org/jira/browse/SPARK-24589) | OutputCommitCoordinator may allow duplicate commits |  Blocker | Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24588](https://issues.apache.org/jira/browse/SPARK-24588) | StreamingSymmetricHashJoinExec should require HashClusteredPartitioning from children |  Blocker | Structured Streaming | Wenchen Fan | Wenchen Fan |
| [SPARK-24190](https://issues.apache.org/jira/browse/SPARK-24190) | lineSep shouldn't be required in JSON write |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24633](https://issues.apache.org/jira/browse/SPARK-24633) | arrays\_zip function's code generator splits input processing incorrectly |  Minor | SQL | Bruce Robbins | Marco Gaido |
| [SPARK-24648](https://issues.apache.org/jira/browse/SPARK-24648) | SQLMetrics counters are not thread safe |  Minor | Project Infra | Stacy Kerkela | Stacy Kerkela |
| [SPARK-24552](https://issues.apache.org/jira/browse/SPARK-24552) | Task attempt numbers are reused when stages are retried |  Blocker | Spark Core | Ryan Blue | Ryan Blue |
| [SPARK-24659](https://issues.apache.org/jira/browse/SPARK-24659) | GenericArrayData.equals should respect element type differences |  Major | SQL | Kris Mok | Kris Mok |
| [SPARK-24446](https://issues.apache.org/jira/browse/SPARK-24446) | Library path with special characters breaks Spark on YARN |  Minor | Spark Core, YARN | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24660](https://issues.apache.org/jira/browse/SPARK-24660) | SHS is not showing properly errors when downloading logs |  Major | Web UI | Marco Gaido | Marco Gaido |
| [SPARK-24553](https://issues.apache.org/jira/browse/SPARK-24553) | Job UI redirect causing http 302 error |  Minor | Web UI | Steven Kallman | Steven Kallman |
| [SPARK-24645](https://issues.apache.org/jira/browse/SPARK-24645) | Skip parsing when csvColumnPruning enabled and partitions scanned only |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-24603](https://issues.apache.org/jira/browse/SPARK-24603) | Typo in comments |  Trivial | Spark Core | Fokko Driesprong | Fokko Driesprong |
| [SPARK-24715](https://issues.apache.org/jira/browse/SPARK-24715) | sbt build brings a wrong jline versions |  Critical | Build | Dongjoon Hyun | L. C. Hsieh |
| [SPARK-24385](https://issues.apache.org/jira/browse/SPARK-24385) | Trivially-true EqualNullSafe should be handled like EqualTo in Dataset.join |  Major | SQL | Daniel Shields | Marco Gaido |
| [SPARK-23698](https://issues.apache.org/jira/browse/SPARK-23698) | Spark code contains numerous undefined names in Python 3 |  Minor | PySpark | cclauss | cclauss |
| [SPARK-24704](https://issues.apache.org/jira/browse/SPARK-24704) | The order of stages in the DAG graph is incorrect |  Minor | Web UI | StanZhai | StanZhai |
| [SPARK-24698](https://issues.apache.org/jira/browse/SPARK-24698) | In Pyspark's ML, an Identifiable's UID has 20 random characters rather than the 12 mentioned in the documentation. |  Trivial | ML | Thomas Dunne | Thomas Dunne |
| [SPARK-24711](https://issues.apache.org/jira/browse/SPARK-24711) | Integration tests will not work with exclude/include tags |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-24743](https://issues.apache.org/jira/browse/SPARK-24743) | Update the JavaDirectKafkaWordCount example to support the new API of Kafka |  Minor | Examples | luochuan | luochuan |
| [SPARK-24694](https://issues.apache.org/jira/browse/SPARK-24694) | Integration tests pass only one app argument |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-24569](https://issues.apache.org/jira/browse/SPARK-24569) | Spark Aggregator with output type Option[Boolean] creates column of type Row |  Major | SQL | John Conwell | L. C. Hsieh |
| [SPARK-24749](https://issues.apache.org/jira/browse/SPARK-24749) | Cannot filter array\<struct\> with named\_struct |  Major | SQL | pin\_zhang | L. C. Hsieh |
| [SPARK-24739](https://issues.apache.org/jira/browse/SPARK-24739) | PySpark does not work with Python 3.7.0 |  Critical | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24530](https://issues.apache.org/jira/browse/SPARK-24530) | Sphinx doesn't render autodoc\_docstring\_signature correctly (with Python 2?) and pyspark.ml docs are broken |  Critical | ML, PySpark | Xiangrui Meng | Hyukjin Kwon |
| [SPARK-24165](https://issues.apache.org/jira/browse/SPARK-24165) | UDF within when().otherwise() raises NullPointerException |  Major | SQL | Jingxuan Wang | Marek Novotny |
| [SPARK-23461](https://issues.apache.org/jira/browse/SPARK-23461) | vignettes should include model predictions for some ML models |  Major | SparkR | Felix Cheung | Huaxin Gao |
| [SPARK-24610](https://issues.apache.org/jira/browse/SPARK-24610) | wholeTextFiles broken for small files |  Minor | Input/Output | Dhruve Ashar | Dhruve Ashar |
| [SPARK-23007](https://issues.apache.org/jira/browse/SPARK-23007) | Add schema evolution test suite for file-based data sources |  Major | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23486](https://issues.apache.org/jira/browse/SPARK-23486) | LookupFunctions should not check the same function name more than once |  Major | SQL | Cheng Lian | kevin yu |
| [SPARK-24713](https://issues.apache.org/jira/browse/SPARK-24713) | AppMatser of spark streaming kafka OOM if there are hundreds of topics consumed |  Major | Input/Output | Yuanbo Liu | Yuanbo Liu |
| [SPARK-24781](https://issues.apache.org/jira/browse/SPARK-24781) | Using a reference from Dataset in Filter/Sort might not work. |  Blocker | SQL | Takuya Ueshin | L. C. Hsieh |
| [SPARK-24754](https://issues.apache.org/jira/browse/SPARK-24754) | Minhash integer overflow |  Minor | ML | Jiayuan Ma | Sean R. Owen |
| [SPARK-24676](https://issues.apache.org/jira/browse/SPARK-24676) | Project required data from parsed data when csvColumnPruning disabled |  Minor | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-24813](https://issues.apache.org/jira/browse/SPARK-24813) | HiveExternalCatalogVersionsSuite still flaky; fall back to Apache archive |  Major | Tests | Sean R. Owen | Sean R. Owen |
| [SPARK-24734](https://issues.apache.org/jira/browse/SPARK-24734) | Fix containsNull of Concat for array type. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24681](https://issues.apache.org/jira/browse/SPARK-24681) | Cannot create a view from a table when a nested column name contains ':' |  Major | SQL | Adrian Ionescu | Takeshi Yamamuro |
| [SPARK-24804](https://issues.apache.org/jira/browse/SPARK-24804) | There are duplicate words in the title in the DatasetSuite |  Trivial | Spark Core | hantiantian | hantiantian |
| [SPARK-24677](https://issues.apache.org/jira/browse/SPARK-24677) | TaskSetManager not updating successfulTaskDurations for old stage attempts |  Critical | Spark Core | dzcxzl | dzcxzl |
| [SPARK-24717](https://issues.apache.org/jira/browse/SPARK-24717) | Split out min retain version of state for memory in HDFSBackedStateStoreProvider |  Major | Structured Streaming | Jungtaek Lim | Jungtaek Lim |
| [SPARK-22151](https://issues.apache.org/jira/browse/SPARK-22151) | PYTHONPATH not picked up from the spark.yarn.appMasterEnv properly |  Major | Spark Core, YARN | Thomas Graves | Parth Gandhi |
| [SPARK-24755](https://issues.apache.org/jira/browse/SPARK-24755) | Executor loss can cause task to not be resubmitted |  Major | Spark Core | Mridul Muralidharan | Hieu Tri Huynh |
| [SPARK-24846](https://issues.apache.org/jira/browse/SPARK-24846) | Stabilize expression cannonicalization |  Major | SQL | Herman van Hövell |  |
| [SPARK-24195](https://issues.apache.org/jira/browse/SPARK-24195) | sc.addFile for local:/ path is broken |  Minor | Spark Core | Felix Cheung | Yuanjian Li |
| [SPARK-23731](https://issues.apache.org/jira/browse/SPARK-23731) | FileSourceScanExec throws NullPointerException in subexpression elimination |  Major | SQL | Jacek Laskowski | Hyukjin Kwon |
| [SPARK-24880](https://issues.apache.org/jira/browse/SPARK-24880) | Fix the group id for spark-kubernetes-integration-tests |  Major | Build, Kubernetes, Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-24488](https://issues.apache.org/jira/browse/SPARK-24488) | Analyzer throws when generator is aliased multiple times |  Minor | SQL | Brandon Krieger | Brandon Krieger |
| [SPARK-24879](https://issues.apache.org/jira/browse/SPARK-24879) | NPE in Hive partition filter pushdown for \`partCol IN (NULL, ....)\` |  Major | SQL | William Sheu | William Sheu |
| [SPARK-24873](https://issues.apache.org/jira/browse/SPARK-24873) | increase switch to shielding frequent interaction reports with yarn |  Major | Spark Core, Spark Shell, YARN | JieFang.He | Yuming Wang |
| [SPARK-24850](https://issues.apache.org/jira/browse/SPARK-24850) | Query plan string representation grows exponentially on queries with recursive cached datasets |  Major | SQL | Onur Satici | Onur Satici |
| [SPARK-24699](https://issues.apache.org/jira/browse/SPARK-24699) | Watermark / Append mode should work with Trigger.Once |  Major | Structured Streaming | Chris Horn | Tathagata Das |
| [SPARK-24594](https://issues.apache.org/jira/browse/SPARK-24594) | Introduce metrics for YARN executor allocation problems |  Major | Spark Core, YARN | Attila Zsolt Piros | Attila Zsolt Piros |
| [SPARK-24870](https://issues.apache.org/jira/browse/SPARK-24870) | Cache can't work normally if there are case letters in SQL |  Major | SQL | eaton | eaton |
| [SPARK-24812](https://issues.apache.org/jira/browse/SPARK-24812) | Last Access Time in the table description is not valid |  Minor | SQL | Sujith Chacko | Sujith Chacko |
| [SPARK-24895](https://issues.apache.org/jira/browse/SPARK-24895) | Spark 2.4.0 Snapshot artifacts has broken metadata due to mismatched filenames |  Major | Build | Eric Chang | Eric Chang |
| [SPARK-24908](https://issues.apache.org/jira/browse/SPARK-24908) | [R] remove spaces to make lintr happy |  Critical | Build | Shane Knapp | Shane Knapp |
| [SPARK-24891](https://issues.apache.org/jira/browse/SPARK-24891) | Fix HandleNullInputsForUDF rule |  Major | SQL | Wei Xue | Wei Xue |
| [SPARK-24911](https://issues.apache.org/jira/browse/SPARK-24911) | SHOW CREATE TABLE drops escaping of nested column names |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24878](https://issues.apache.org/jira/browse/SPARK-24878) | Fix reverse function for array type of primitive type containing null. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24919](https://issues.apache.org/jira/browse/SPARK-24919) | Scala linter rule for sparkContext.hadoopConfiguration |  Major | Build | Gengliang Wang | Gengliang Wang |
| [SPARK-24829](https://issues.apache.org/jira/browse/SPARK-24829) | In Spark Thrift Server, CAST AS FLOAT inconsistent with spark-shell or spark-sql |  Major | SQL | zuotingbing | zuotingbing |
| [SPARK-24927](https://issues.apache.org/jira/browse/SPARK-24927) | The hadoop-provided profile doesn't play well with Snappy-compressed Parquet files |  Major | Build | Cheng Lian | Cheng Lian |
| [SPARK-24809](https://issues.apache.org/jira/browse/SPARK-24809) | Serializing LongHashedRelation in executor may result in data error |  Critical | SQL | Lijia Liu | Lijia Liu |
| [SPARK-24934](https://issues.apache.org/jira/browse/SPARK-24934) | Complex type and binary type in in-memory partition pruning does not work due to missing upper/lower bounds cases |  Critical | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24957](https://issues.apache.org/jira/browse/SPARK-24957) | Decimal arithmetic can lead to wrong values using codegen |  Major | SQL | David Vogelbacher | Marco Gaido |
| [SPARK-24963](https://issues.apache.org/jira/browse/SPARK-24963) | Integration tests will fail if they run in a namespace not being the default |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos | Matthew Cheah |
| [SPARK-24972](https://issues.apache.org/jira/browse/SPARK-24972) | PivotFirst could not handle pivot columns of complex types |  Minor | SQL | Wei Xue | Wei Xue |
| [SPARK-24536](https://issues.apache.org/jira/browse/SPARK-24536) | Query with nonsensical LIMIT hits AssertionError |  Trivial | SQL | Alexander Behm |  |
| [SPARK-24653](https://issues.apache.org/jira/browse/SPARK-24653) | Flaky test "JoinSuite.test SortMergeJoin (with spill)" |  Minor | Tests | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-24937](https://issues.apache.org/jira/browse/SPARK-24937) | Datasource partition table should load empty static partitions |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-24742](https://issues.apache.org/jira/browse/SPARK-24742) | Field Metadata raises NullPointerException in hashCode method |  Minor | SQL | Kaya Kupferschmidt | Kaya Kupferschmidt |
| [SPARK-24705](https://issues.apache.org/jira/browse/SPARK-24705) | Spark.sql.adaptive.enabled=true is enabled and self-join query |  Minor | SQL | cheng dai | Takeshi Yamamuro |
| [SPARK-24896](https://issues.apache.org/jira/browse/SPARK-24896) | Uuid expression should produce different values in each execution under streaming query |  Major | SQL, Structured Streaming | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24966](https://issues.apache.org/jira/browse/SPARK-24966) | Fix the precedence rule for set operations. |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-24788](https://issues.apache.org/jira/browse/SPARK-24788) | RelationalGroupedDataset.toString throws errors when grouping by UnresolvedAttribute |  Minor | SQL | Chris Horn | Chris Horn |
| [SPARK-24997](https://issues.apache.org/jira/browse/SPARK-24997) | Support MINUS ALL |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25011](https://issues.apache.org/jira/browse/SPARK-25011) | Add PrefixSpan to \_\_all\_\_ in fpm.py |  Minor | ML | yuhao yang | yuhao yang |
| [SPARK-25009](https://issues.apache.org/jira/browse/SPARK-25009) | Standalone Cluster mode application submit is not working |  Critical | Spark Core | Devaraj Kavali | Devaraj Kavali |
| [SPARK-24987](https://issues.apache.org/jira/browse/SPARK-24987) | Kafka Cached Consumer Leaking File Descriptors |  Critical | Structured Streaming | Yuval Itzchakov | Yuval Itzchakov |
| [SPARK-24981](https://issues.apache.org/jira/browse/SPARK-24981) | ShutdownHook timeout causes job to fail when succeeded when SparkContext stop() not called by user program |  Minor | Spark Core | Hieu Tri Huynh | Hieu Tri Huynh |
| [SPARK-25019](https://issues.apache.org/jira/browse/SPARK-25019) | The published spark sql pom does not exclude the normal version of orc-core |  Critical | Build, SQL | Yin Huai | Dongjoon Hyun |
| [SPARK-24948](https://issues.apache.org/jira/browse/SPARK-24948) | SHS filters wrongly some applications due to permission check |  Blocker | Web UI | Marco Gaido | Marco Gaido |
| [SPARK-25010](https://issues.apache.org/jira/browse/SPARK-25010) | Rand/Randn should produce different values for each execution in streaming query |  Major | SQL, Structured Streaming | L. C. Hsieh | L. C. Hsieh |
| [SPARK-24341](https://issues.apache.org/jira/browse/SPARK-24341) | Codegen compile error from predicate subquery |  Minor | SQL | Juliusz Sompolski | Marco Gaido |
| [SPARK-25041](https://issues.apache.org/jira/browse/SPARK-25041) | genjavadoc-plugin\_0.10 is not found with sbt in scala-2.12 |  Major | Build | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-25046](https://issues.apache.org/jira/browse/SPARK-25046) | Alter View  can excute sql  like "ALTER VIEW ... AS INSERT INTO" |  Minor | SQL | SongXun | SongXun |
| [SPARK-25058](https://issues.apache.org/jira/browse/SPARK-25058) | Use Block.isEmpty/nonEmpty to check whether the code is empty or not. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-23415](https://issues.apache.org/jira/browse/SPARK-23415) | BufferHolderSparkSubmitSuite is flaky |  Major | SQL, Tests | Dongjoon Hyun | Kazuaki Ishizaki |
| [SPARK-25076](https://issues.apache.org/jira/browse/SPARK-25076) | SQLConf should not be retrieved from a stopped SparkSession |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24950](https://issues.apache.org/jira/browse/SPARK-24950) | scala DateTimeUtilsSuite daysToMillis and millisToDays fails w/java 8 181-b13 |  Major | Build, Tests | Shane Knapp | Chris Martin |
| [SPARK-25081](https://issues.apache.org/jira/browse/SPARK-25081) | Nested spill in ShuffleExternalSorter may access a released memory page |  Blocker | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25084](https://issues.apache.org/jira/browse/SPARK-25084) | "distribute by" on multiple columns may lead to codegen issue |  Blocker | SQL | yucai | yucai |
| [SPARK-25092](https://issues.apache.org/jira/browse/SPARK-25092) | Add RewriteExceptAll, RewriteIntersectAll and RewriteCorrelatedScalarSubquery in the list of nonExcludableRules |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25090](https://issues.apache.org/jira/browse/SPARK-25090) | java.lang.ClassCastException when using a CrossValidator |  Major | ML | Mark Morrisson | Marco Gaido |
| [SPARK-25033](https://issues.apache.org/jira/browse/SPARK-25033) | Bump Apache commons.{httpclient, httpcore} |  Major | Spark Core | Fokko Driesprong | Fokko Driesprong |
| [SPARK-25096](https://issues.apache.org/jira/browse/SPARK-25096) | Loosen nullability if the cast is force-nullable. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24391](https://issues.apache.org/jira/browse/SPARK-24391) | from\_json should support arrays of primitives, and more generally all JSON |  Major | SQL | Sam Kitajima-Kimbrel | Maxim Gekk |
| [SPARK-22713](https://issues.apache.org/jira/browse/SPARK-22713) | OOM caused by the memory contention and memory leak in TaskMemoryManager |  Critical | Shuffle, Spark Core | Lijie Xu | Eyal Farago |
| [SPARK-25028](https://issues.apache.org/jira/browse/SPARK-25028) | AnalyzePartitionCommand failed with NPE if value is null |  Major | Spark Core | Izek Greenfield | Marco Gaido |
| [SPARK-22974](https://issues.apache.org/jira/browse/SPARK-22974) | CountVectorModel does not attach attributes to output column |  Major | ML | William Zhang | L. C. Hsieh |
| [SPARK-25031](https://issues.apache.org/jira/browse/SPARK-25031) | The schema of MapType can not be printed correctly |  Minor | SQL | Hao Ren | Hao Ren |
| [SPARK-23042](https://issues.apache.org/jira/browse/SPARK-23042) | Use OneHotEncoderModel to encode labels in MultilayerPerceptronClassifier |  Major | ML | L. C. Hsieh | L. C. Hsieh |
| [SPARK-25116](https://issues.apache.org/jira/browse/SPARK-25116) | Fix the "exit code 1" error when terminating Kafka tests |  Major | Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25137](https://issues.apache.org/jira/browse/SPARK-25137) | NumberFormatException\` when starting spark-shell  from Mac terminal |  Trivial | Spark Shell | Vinod KC | Vinod KC |
| [SPARK-25134](https://issues.apache.org/jira/browse/SPARK-25134) | Csv column pruning with checking of headers throws incorrect error |  Major | SQL | koert kuipers | Koert Kuipers |
| [SPARK-25132](https://issues.apache.org/jira/browse/SPARK-25132) | Case-insensitive field resolution when reading from Parquet |  Major | SQL | Chenxiao Mao | Chenxiao Mao |
| [SPARK-25161](https://issues.apache.org/jira/browse/SPARK-25161) | Fix several bugs in failure handling of barrier execution mode |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-25149](https://issues.apache.org/jira/browse/SPARK-25149) | Personalized PageRank raises an error if vertexIDs are \> MaxInt |  Major | GraphX | Bago Amirbekian | Bago Amirbekian |
| [SPARK-25114](https://issues.apache.org/jira/browse/SPARK-25114) | RecordBinaryComparator may return wrong result when subtraction between two words is divisible by Integer.MAX\_VALUE |  Blocker | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-25159](https://issues.apache.org/jira/browse/SPARK-25159) | json schema inference should only trigger one job |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25181](https://issues.apache.org/jira/browse/SPARK-25181) | Block Manager master and slave thread pools are unbounded |  Major | Spark Core | Mukul Murthy | Mukul Murthy |
| [SPARK-25163](https://issues.apache.org/jira/browse/SPARK-25163) | Flaky test: o.a.s.util.collection.ExternalAppendOnlyMapSuite.spilling with compression |  Major | Tests | Shixiong Zhu | L. C. Hsieh |
| [SPARK-25167](https://issues.apache.org/jira/browse/SPARK-25167) | Minor fixes for R sql tests (tests that fail in development environment) |  Minor | SparkR | Dilip Biswal | Dilip Biswal |
| [SPARK-25164](https://issues.apache.org/jira/browse/SPARK-25164) | Parquet reader builds entire list of columns once for each column |  Minor | SQL | Bruce Robbins | Bruce Robbins |
| [SPARK-25126](https://issues.apache.org/jira/browse/SPARK-25126) | avoid creating OrcFile.Reader for all orc files |  Minor | Input/Output | Rao Fu | Rao Fu |
| [SPARK-25204](https://issues.apache.org/jira/browse/SPARK-25204) | rate source test is flaky |  Minor | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-25205](https://issues.apache.org/jira/browse/SPARK-25205) | typo in spark.network.crypto.keyFactoryIteration |  Trivial | Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-23425](https://issues.apache.org/jira/browse/SPARK-23425) | load data for hdfs file path with wild card usage is not working properly |  Major | SQL | Sujith Chacko | Sujith Chacko |
| [SPARK-25174](https://issues.apache.org/jira/browse/SPARK-25174) | ApplicationMaster suspends when unregistering itself from RM with extreme large diagnostic message |  Major | Spark Core, YARN | Kent Yao | Kent Yao |
| [SPARK-25214](https://issues.apache.org/jira/browse/SPARK-25214) | Kafka v2 source may return duplicated records when \`failOnDataLoss\` is \`false\` |  Blocker | Structured Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25124](https://issues.apache.org/jira/browse/SPARK-25124) | VectorSizeHint.size is buggy, breaking streaming pipeline |  Major | ML | Timothy Hunter | Huaxin Gao |
| [SPARK-24721](https://issues.apache.org/jira/browse/SPARK-24721) | Failed to use PythonUDF with literal inputs in filter with data sources |  Major | PySpark, SQL | Xiao Li | Li Jin |
| [SPARK-25218](https://issues.apache.org/jira/browse/SPARK-25218) | Potential resource leaks in TransportServer and SocketAuthHelper |  Minor | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25005](https://issues.apache.org/jira/browse/SPARK-25005) | Structured streaming doesn't support kafka transaction (creating empty offset with abort & markers) |  Major | Structured Streaming | Quentin Ambard | Shixiong Zhu |
| [SPARK-23997](https://issues.apache.org/jira/browse/SPARK-23997) | Configurable max number of buckets |  Major | Input/Output, SQL | Fernando Pereira | Fernando Pereira |
| [SPARK-23679](https://issues.apache.org/jira/browse/SPARK-23679) | uiWebUrl show inproper URL when running on YARN |  Major | Spark Core, Web UI, YARN | Maciej Bryński | Saisai Shao |
| [SPARK-25240](https://issues.apache.org/jira/browse/SPARK-25240) | A deadlock in ALTER TABLE RECOVER PARTITIONS |  Blocker | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25004](https://issues.apache.org/jira/browse/SPARK-25004) | Add spark.executor.pyspark.memory config to set resource.RLIMIT\_AS |  Major | PySpark | Ryan Blue | Ryan Blue |
| [SPARK-22357](https://issues.apache.org/jira/browse/SPARK-22357) | SparkContext.binaryFiles ignore minPartitions parameter |  Major | Spark Core | Weichen Xu | Bo Meng |
| [SPARK-25266](https://issues.apache.org/jira/browse/SPARK-25266) | Fix memory leak in Barrier Execution Mode |  Critical | Scheduler, Spark Core | Kousuke Saruta | Kousuke Saruta |
| [SPARK-24909](https://issues.apache.org/jira/browse/SPARK-24909) | Spark scheduler can hang when fetch failures, executor lost, task running on lost executor, and multiple stage attempts |  Critical | Scheduler, Spark Core | Thomas Graves | Thomas Graves |
| [SPARK-25288](https://issues.apache.org/jira/browse/SPARK-25288) | Kafka transaction tests are flaky |  Major | Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25183](https://issues.apache.org/jira/browse/SPARK-25183) | Spark HiveServer2 registers shutdown hook with JVM, not ShutdownHookManager; race conditions can arise |  Minor | SQL | Steve Loughran | Steve Loughran |
| [SPARK-25283](https://issues.apache.org/jira/browse/SPARK-25283) | A deadlock in UnionRDD |  Major | Spark Core | Maxim Gekk | Maxim Gekk |
| [SPARK-25264](https://issues.apache.org/jira/browse/SPARK-25264) | Fix comma-delineated arguments passed into PythonRunner and RRunner |  Major | Kubernetes, PySpark, Spark Core | Ilan Filonenko |  |
| [SPARK-25289](https://issues.apache.org/jira/browse/SPARK-25289) | ChiSqSelector max on empty collection |  Major | MLlib | Marie Beaulieu | Marco Gaido |
| [SPARK-25308](https://issues.apache.org/jira/browse/SPARK-25308) | ArrayContains function may return a error in the code generation phase. |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25307](https://issues.apache.org/jira/browse/SPARK-25307) | ArraySort function may return a error in the code generation phase. |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25310](https://issues.apache.org/jira/browse/SPARK-25310) | ArraysOverlap may throw a CompileException |  Major | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-25306](https://issues.apache.org/jira/browse/SPARK-25306) | Avoid skewed filter trees to speed up \`createFilter\` in ORC |  Critical | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-24415](https://issues.apache.org/jira/browse/SPARK-24415) | Stage page aggregated executor metrics wrong when failures |  Critical | Web UI | Thomas Graves | Ankur Gupta |
| [SPARK-25231](https://issues.apache.org/jira/browse/SPARK-25231) | Running a Large Job with Speculation On Causes Executor Heartbeats to Time Out on Driver |  Major | Scheduler, Spark Core | Parth Gandhi | Parth Gandhi |
| [SPARK-23243](https://issues.apache.org/jira/browse/SPARK-23243) | Shuffle+Repartition on an RDD could lead to incorrect answers |  Blocker | Spark Core | Xingbo Jiang | Wenchen Fan |
| [SPARK-25176](https://issues.apache.org/jira/browse/SPARK-25176) | Kryo fails to serialize a parametrised type hierarchy |  Major | Spark Core | Mikhail Pryakhin | Yuming Wang |
| [SPARK-25313](https://issues.apache.org/jira/browse/SPARK-25313) | Fix regression in FileFormatWriter output schema |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25317](https://issues.apache.org/jira/browse/SPARK-25317) | MemoryBlock performance regression |  Blocker | SQL | Wenchen Fan | Marco Gaido |
| [SPARK-25268](https://issues.apache.org/jira/browse/SPARK-25268) | runParallelPersonalizedPageRank throws serialization Exception |  Critical | GraphX | Bago Amirbekian | shahid |
| [SPARK-25072](https://issues.apache.org/jira/browse/SPARK-25072) | PySpark custom Row class can be given extra parameters |  Minor | PySpark | Jan-Willem van der Sijp | Yuanjian Li |
| [SPARK-25237](https://issues.apache.org/jira/browse/SPARK-25237) | FileScanRdd's inputMetrics is wrong  when select the datasource table with limit |  Major | SQL | du | Takeshi Yamamuro |
| [SPARK-25021](https://issues.apache.org/jira/browse/SPARK-25021) | Add spark.executor.pyspark.memory support to Kubernetes |  Major | Kubernetes, Spark Core | Ryan Blue | Ilan Filonenko |
| [SPARK-25368](https://issues.apache.org/jira/browse/SPARK-25368) | Incorrect constraint inference returns wrong result |  Blocker | Optimizer, SQL | Lev Katzav | Yuming Wang |
| [SPARK-25175](https://issues.apache.org/jira/browse/SPARK-25175) | Field resolution should fail if there's ambiguity for ORC native reader |  Major | SQL | Chenxiao Mao | Chenxiao Mao |
| [SPARK-25278](https://issues.apache.org/jira/browse/SPARK-25278) | Number of output rows metric of union of views is multiplied by their occurrences |  Major | SQL | Jacek Laskowski | Marco Gaido |
| [SPARK-25036](https://issues.apache.org/jira/browse/SPARK-25036) | Scala 2.12 issues: Compilation error with sbt |  Major | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-25389](https://issues.apache.org/jira/browse/SPARK-25389) | INSERT OVERWRITE DIRECTORY STORED AS should prevent duplicate fields |  Major | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25221](https://issues.apache.org/jira/browse/SPARK-25221) | [DEPLOY] Consistent trailing whitespace treatment of conf values |  Major | Deploy | Gera Shegalov | Gera Shegalov |
| [SPARK-24889](https://issues.apache.org/jira/browse/SPARK-24889) | dataset.unpersist() doesn't update storage memory stats |  Major | Spark Core | Yuri Bogomolov | L. C. Hsieh |
| [SPARK-25398](https://issues.apache.org/jira/browse/SPARK-25398) | Minor bugs from comparing unrelated types |  Minor | Mesos, Spark Core, YARN | Sean R. Owen | Sean R. Owen |
| [SPARK-25399](https://issues.apache.org/jira/browse/SPARK-25399) | Reusing execution threads from continuous processing for microbatch streaming can result in correctness issues |  Critical | Structured Streaming | Mukul Murthy | Mukul Murthy |
| [SPARK-25371](https://issues.apache.org/jira/browse/SPARK-25371) | Vector Assembler with no input columns leads to opaque error |  Trivial | ML, MLlib | Victor Alor | Marco Gaido |
| [SPARK-25352](https://issues.apache.org/jira/browse/SPARK-25352) | Perform ordered global limit when limit number is bigger than topKSortFallbackThreshold |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-25363](https://issues.apache.org/jira/browse/SPARK-25363) | Schema pruning doesn't work if nested column is used in where clause |  Major | SQL | L. C. Hsieh | L. C. Hsieh |
| [SPARK-25387](https://issues.apache.org/jira/browse/SPARK-25387) | Malformed CSV causes NPE |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25357](https://issues.apache.org/jira/browse/SPARK-25357) | Add metadata to SparkPlanInfo to dump more information like file path to event log |  Minor | SQL | Lantao Jin | Lantao Jin |
| [SPARK-25402](https://issues.apache.org/jira/browse/SPARK-25402) | Null handling in BooleanSimplification |  Blocker | SQL | Xiao Li | Xiao Li |
| [SPARK-25295](https://issues.apache.org/jira/browse/SPARK-25295) | Pod names conflicts in client mode, if previous submission was not a clean shutdown. |  Major | Kubernetes, Spark Core | Prashant Sharma | Stavros Kontopoulos |
| [SPARK-25406](https://issues.apache.org/jira/browse/SPARK-25406) | Incorrect usage of withSQLConf method in Parquet schema pruning test suite masks failing tests |  Major | SQL | Michael MacFadden | Michael MacFadden |
| [SPARK-25425](https://issues.apache.org/jira/browse/SPARK-25425) | Extra options must overwrite sessions options |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25438](https://issues.apache.org/jira/browse/SPARK-25438) | Fix FilterPushdownBenchmark to use the same memory assumption |  Major | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25439](https://issues.apache.org/jira/browse/SPARK-25439) | TPCHQuerySuite customer.c\_nationkey should be bigint instead of string |  Minor | SQL, Tests | Nicolas Poggi | Nicolas Poggi |
| [SPARK-25427](https://issues.apache.org/jira/browse/SPARK-25427) | Add BloomFilter creation test cases |  Major | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25431](https://issues.apache.org/jira/browse/SPARK-25431) | Fix function examples and unify the format of the example results. |  Minor | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-25443](https://issues.apache.org/jira/browse/SPARK-25443) | fix issues when building docs with release scripts in docker |  Major | Project Infra | Wenchen Fan | Wenchen Fan |
| [SPARK-24151](https://issues.apache.org/jira/browse/SPARK-24151) | CURRENT\_DATE, CURRENT\_TIMESTAMP incorrectly resolved as column names when caseSensitive is enabled |  Major | SQL | James Thompson | James Thompson |
| [SPARK-25291](https://issues.apache.org/jira/browse/SPARK-25291) | Flakiness of tests in terms of executor memory (SecretsTestSuite) |  Major | Kubernetes, Spark Core | Ilan Filonenko | Ilan Filonenko |
| [SPARK-23200](https://issues.apache.org/jira/browse/SPARK-23200) | Reset configuration when restarting from checkpoints |  Major | Kubernetes, Spark Core | Anirudh Ramanathan |  |
| [SPARK-25471](https://issues.apache.org/jira/browse/SPARK-25471) | Fix tests for Python 3.6 with Pandas 0.23+ |  Major | PySpark, Tests | Bryan Cutler | Bryan Cutler |
| [SPARK-25417](https://issues.apache.org/jira/browse/SPARK-25417) | ArrayContains function may return incorrect result when right expression is implicitly down casted |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25450](https://issues.apache.org/jira/browse/SPARK-25450) | PushProjectThroughUnion rule uses the same exprId for project expressions in each Union child, causing mistakes in constant propagation |  Major | SQL | Wei Xue | Wei Xue |
| [SPARK-25416](https://issues.apache.org/jira/browse/SPARK-25416) | ArrayPosition function may return incorrect result when right expression is implicitly downcasted. |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25502](https://issues.apache.org/jira/browse/SPARK-25502) | [Spark Job History] Empty Page when page number exceeds the reatinedTask size |  Minor | Web UI | ABHISHEK KUMAR GUPTA | shahid |
| [SPARK-25503](https://issues.apache.org/jira/browse/SPARK-25503) | [Spark Job History] Total task message in stage page is ambiguous |  Major | Web UI | ABHISHEK KUMAR GUPTA | shahid |
| [SPARK-25519](https://issues.apache.org/jira/browse/SPARK-25519) | ArrayRemove function may return incorrect result when right expression is implicitly downcasted. |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25495](https://issues.apache.org/jira/browse/SPARK-25495) | FetchedData.reset doesn't reset \_nextOffsetInFetchedData and \_offsetAfterPoll |  Blocker | Structured Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25509](https://issues.apache.org/jira/browse/SPARK-25509) | SHS V2 cannot enabled in Windows, because POSIX permissions is not support. |  Major | Spark Core | Rong Tang | Rong Tang |
| [SPARK-25536](https://issues.apache.org/jira/browse/SPARK-25536) | executorSource.METRIC read wrong record in Executor.scala Line444 |  Major | Spark Core | ZhuoerXu | shahid |
| [SPARK-25522](https://issues.apache.org/jira/browse/SPARK-25522) |  Improve type promotion for input arguments of elementAt function |  Major | SQL | Dilip Biswal | Dilip Biswal |
| [SPARK-25314](https://issues.apache.org/jira/browse/SPARK-25314) | Invalid PythonUDF - requires attributes from more than one child - in "on" join condition |  Major | PySpark, SQL | Sergey Bahchissaraitsev | Yuanjian Li |
| [SPARK-21743](https://issues.apache.org/jira/browse/SPARK-21743) | top-most limit should not cause memory leak |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25546](https://issues.apache.org/jira/browse/SPARK-25546) | RDDInfo uses SparkEnv before it may have been initialized |  Major | Spark Core, Tests | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-25533](https://issues.apache.org/jira/browse/SPARK-25533) | Inconsistent message for Completed Jobs in the  JobUI, when there are failed jobs, compared to spark2.2 |  Major | Web UI | shahid | shahid |
| [SPARK-25505](https://issues.apache.org/jira/browse/SPARK-25505) | The output order of grouping columns in Pivot is different from the input order |  Minor | SQL | Wei Xue | Wei Xue |
| [SPARK-25542](https://issues.apache.org/jira/browse/SPARK-25542) | Flaky test: OpenHashMapSuite |  Major | Spark Core, Tests | Dongjoon Hyun | L. C. Hsieh |
| [SPARK-25570](https://issues.apache.org/jira/browse/SPARK-25570) | Replace 2.3.1 with 2.3.2 in HiveExternalCatalogVersionsSuite |  Minor | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25568](https://issues.apache.org/jira/browse/SPARK-25568) | Continue to update the remaining accumulators when failing to update one accumulator |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25543](https://issues.apache.org/jira/browse/SPARK-25543) | Confusing log messages at DEBUG level, in K8s mode. |  Minor | Kubernetes, Spark Core | Prashant Sharma | Prashant Sharma |
| [SPARK-25578](https://issues.apache.org/jira/browse/SPARK-25578) | Update to Scala 2.12.7 |  Minor | Build, Spark Core, SQL | Sean R. Owen | Sean R. Owen |
| [SPARK-25538](https://issues.apache.org/jira/browse/SPARK-25538) | incorrect row counts after distinct() |  Blocker | SQL | Steven Rand | Marco Gaido |
| [SPARK-25602](https://issues.apache.org/jira/browse/SPARK-25602) | SparkPlan.getByteArrayRdd should not consume the input when not necessary |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25521](https://issues.apache.org/jira/browse/SPARK-25521) | Job id showing null when insert into command Job is finished. |  Minor | Spark Core, SQL | Babulal | Sujith Chacko |
| [SPARK-25644](https://issues.apache.org/jira/browse/SPARK-25644) | Fix java foreachBatch API |  Blocker | Structured Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25646](https://issues.apache.org/jira/browse/SPARK-25646) | docker-image-tool.sh doesn't work on developer build |  Minor | Kubernetes, Spark Core | Marcelo Masiero Vanzin | Marcelo Masiero Vanzin |
| [SPARK-25671](https://issues.apache.org/jira/browse/SPARK-25671) | Build external/spark-ganglia-lgpl in Jenkins Test |  Major | Build | Xiao Li | Xiao Li |
| [SPARK-25591](https://issues.apache.org/jira/browse/SPARK-25591) | PySpark Accumulators with multiple PythonUDFs |  Blocker | PySpark | Abdeali Kothari | L. C. Hsieh |
| [SPARK-25677](https://issues.apache.org/jira/browse/SPARK-25677) | Configuring zstd compression in JDBC throwing IllegalArgumentException Exception |  Major | Spark Core | ABHISHEK KUMAR GUPTA | Shivu Sondur |
| [SPARK-25669](https://issues.apache.org/jira/browse/SPARK-25669) | Check CSV header only when it exists |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25636](https://issues.apache.org/jira/browse/SPARK-25636) | spark-submit swallows the failure reason when there is an error connecting to master |  Minor | Spark Core | Devaraj Kavali | Devaraj Kavali |
| [SPARK-25674](https://issues.apache.org/jira/browse/SPARK-25674) | If the records are incremented by more than 1 at a time,the number of bytes might rarely ever get updated |  Minor | SQL | liuxian | liuxian |
| [SPARK-25708](https://issues.apache.org/jira/browse/SPARK-25708) | HAVING without GROUP BY means global aggregate |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25697](https://issues.apache.org/jira/browse/SPARK-25697) | When zstd compression enabled in progress application is throwing Error in UI |  Major | Spark Core | ABHISHEK KUMAR GUPTA | shahid |
| [SPARK-25660](https://issues.apache.org/jira/browse/SPARK-25660) | Impossible to use the backward slash as the CSV fields delimiter |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-25714](https://issues.apache.org/jira/browse/SPARK-25714) | Null Handling in the Optimizer rule BooleanSimplification |  Blocker | SQL | Xiao Li | Xiao Li |
| [SPARK-25726](https://issues.apache.org/jira/browse/SPARK-25726) | Flaky test: SaveIntoDataSourceCommandSuite.\`simpleString is redacted\` |  Minor | SQL, Tests | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25727](https://issues.apache.org/jira/browse/SPARK-25727) | makeCopy failed in InMemoryRelation |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-25738](https://issues.apache.org/jira/browse/SPARK-25738) | LOAD DATA INPATH doesn't work if hdfs conf includes port |  Blocker | SQL | Imran Rashid | Imran Rashid |
| [SPARK-25579](https://issues.apache.org/jira/browse/SPARK-25579) | Use quoted attribute names if needed in pushed ORC predicates |  Blocker | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25741](https://issues.apache.org/jira/browse/SPARK-25741) | Long URLs are not rendered properly in web UI |  Minor | Web UI | Gengliang Wang | Gengliang Wang |
| [SPARK-21402](https://issues.apache.org/jira/browse/SPARK-21402) | Fix java array of structs deserialization |  Major | SQL | Tom | Vladimir Kuriatkov |
| [SPARK-25768](https://issues.apache.org/jira/browse/SPARK-25768) | Constant argument expecting Hive UDAFs doesn't work |  Major | SQL | Peter Toth | Peter Toth |
| [SPARK-25704](https://issues.apache.org/jira/browse/SPARK-25704) | Replication of \> 2GB block fails due to bad config default |  Major | Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-25795](https://issues.apache.org/jira/browse/SPARK-25795) | Fix CSV SparkR SQL Example |  Minor | Examples, R | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25801](https://issues.apache.org/jira/browse/SPARK-25801) | pandas\_udf grouped\_map fails with input dataframe with more than 255 columns |  Major | PySpark | Frederik |  |
| [SPARK-22809](https://issues.apache.org/jira/browse/SPARK-22809) | pyspark is sensitive to imports with dots |  Major | PySpark | Cricket Temple | Holden Karau |
| [SPARK-25803](https://issues.apache.org/jira/browse/SPARK-25803) | The -n option to docker-image-tool.sh causes other options to be ignored |  Minor | Kubernetes, Spark Core | Steve Larkin | Steve Larkin |
| [SPARK-24787](https://issues.apache.org/jira/browse/SPARK-24787) | Events being dropped at an alarming rate due to hsync being slow for eventLogging |  Minor | Spark Core, Web UI | Sanket Reddy | Devaraj Kavali |
| [SPARK-25832](https://issues.apache.org/jira/browse/SPARK-25832) | remove newly added map related functions |  Blocker | SQL | Wenchen Fan | Xiao Li |
| [SPARK-25793](https://issues.apache.org/jira/browse/SPARK-25793) | Loading model bug in BisectingKMeans |  Major | ML, MLlib | Weichen Xu | Huaxin Gao |
| [SPARK-25840](https://issues.apache.org/jira/browse/SPARK-25840) | \`make-distribution.sh\` should not fail due to missing LICENSE-binary |  Major | Build | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25822](https://issues.apache.org/jira/browse/SPARK-25822) | Fix a race condition when releasing a Python worker |  Major | PySpark | Shixiong Zhu | Shixiong Zhu |
| [SPARK-25835](https://issues.apache.org/jira/browse/SPARK-25835) | Propagate scala 2.12 profile in k8s integration tests |  Minor | Kubernetes, Spark Core | Stavros Kontopoulos | Stavros Kontopoulos |
| [SPARK-25854](https://issues.apache.org/jira/browse/SPARK-25854) | mvn helper script always exits w/1, causing mvn builds to fail |  Critical | Build | Shane Knapp | Shane Knapp |
| [SPARK-25816](https://issues.apache.org/jira/browse/SPARK-25816) | Functions does not resolve Columns correctly |  Critical | SQL | Bowen Zhang | Peter Toth |
| [SPARK-25797](https://issues.apache.org/jira/browse/SPARK-25797) | Views created via 2.1 cannot be read via 2.2+ |  Major | SQL | Chenxiao Mao | Chenxiao Mao |
| [SPARK-25206](https://issues.apache.org/jira/browse/SPARK-25206) | wrong records are returned when Hive metastore schema and parquet schema are in different letter cases |  Blocker | SQL | yucai |  |
| [SPARK-17166](https://issues.apache.org/jira/browse/SPARK-17166) | CTAS lost table properties after conversion to data source tables. |  Major | SQL | Xiao Li | Dongjoon Hyun |
| [SPARK-25799](https://issues.apache.org/jira/browse/SPARK-25799) | DataSourceApiV2 scan reuse does not respect options |  Major | SQL | Max Kießling |  |
| [SPARK-23829](https://issues.apache.org/jira/browse/SPARK-23829) | spark-sql-kafka source in spark 2.3 causes reading stream failure frequently |  Major | Structured Streaming | Norman Bai |  |
| [SPARK-23636](https://issues.apache.org/jira/browse/SPARK-23636) | [SPARK 2.2] \| Kafka Consumer \| KafkaUtils.createRDD throws Exception - java.util.ConcurrentModificationException: KafkaConsumer is not safe for multi-threaded access |  Major | DStreams | Deepak |  |
| [SPARK-26614](https://issues.apache.org/jira/browse/SPARK-26614) | Speculation kill might cause job failure |  Major | Scheduler, Spark Core | liupengcheng |  |
| [SPARK-26612](https://issues.apache.org/jira/browse/SPARK-26612) | Speculation kill causing finished stage recomputed |  Major | Scheduler, Spark Core | liupengcheng |  |
| [SPARK-26802](https://issues.apache.org/jira/browse/SPARK-26802) | CVE-2018-11760: Apache Spark local privilege escalation vulnerability |  Blocker | PySpark, Security | Imran Rashid | Luca Canali |
| [SPARK-28626](https://issues.apache.org/jira/browse/SPARK-28626) | Spark leaves unencrypted data on local disk, even with encryption turned on (CVE-2019-10099) |  Major | Security | Imran Rashid |  |
| [SPARK-25330](https://issues.apache.org/jira/browse/SPARK-25330) | Permission issue after upgrade hadoop version to 2.7.7 |  Major | Build | Yuming Wang | Yuming Wang |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-16139](https://issues.apache.org/jira/browse/SPARK-16139) | Audit tests for leaked threads |  Major | Tests | Imran Rashid | Gabor Somogyi |
| [SPARK-23169](https://issues.apache.org/jira/browse/SPARK-23169) | Run lintr on the changes of lint-r script and .lintr configuration |  Minor | Project Infra | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23392](https://issues.apache.org/jira/browse/SPARK-23392) | Add some test case for images feature |  Trivial | ML, Tests | Bo Xu | Bo Xu |
| [SPARK-22886](https://issues.apache.org/jira/browse/SPARK-22886) | ML test for StructuredStreaming: spark.ml.recommendation |  Major | ML, Tests | Joseph K. Bradley | Gabor Somogyi |
| [SPARK-22882](https://issues.apache.org/jira/browse/SPARK-22882) | ML test for StructuredStreaming: spark.ml.classification |  Major | ML, Tests | Joseph K. Bradley | Weichen Xu |
| [SPARK-22915](https://issues.apache.org/jira/browse/SPARK-22915) | ML test for StructuredStreaming: spark.ml.feature, N-Z |  Major | ML, Tests | Joseph K. Bradley | Attila Zsolt Piros |
| [SPARK-23849](https://issues.apache.org/jira/browse/SPARK-23849) | Tests for the samplingRatio option of json schema inferring |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-23881](https://issues.apache.org/jira/browse/SPARK-23881) | Flaky test: JobCancellationSuite."interruptible iterator of shuffle reader" |  Major | Spark Core | Xingbo Jiang | Xingbo Jiang |
| [SPARK-22883](https://issues.apache.org/jira/browse/SPARK-22883) | ML test for StructuredStreaming: spark.ml.feature, A-M |  Major | ML, Tests | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-24044](https://issues.apache.org/jira/browse/SPARK-24044) | Explicitly print out skipped tests from unittest module |  Major | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-22885](https://issues.apache.org/jira/browse/SPARK-22885) | ML test for StructuredStreaming: spark.ml.tuning |  Major | ML, Tests | Joseph K. Bradley | Weichen Xu |
| [SPARK-22884](https://issues.apache.org/jira/browse/SPARK-22884) | ML test for StructuredStreaming: spark.ml.clustering |  Major | ML, Tests | Joseph K. Bradley | Sandor Murakozi |
| [SPARK-24502](https://issues.apache.org/jira/browse/SPARK-24502) | flaky test: UnsafeRowSerializerSuite |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24521](https://issues.apache.org/jira/browse/SPARK-24521) | Fix ineffective test in CachedTableSuite |  Minor | SQL | Li Jin | Li Jin |
| [SPARK-24564](https://issues.apache.org/jira/browse/SPARK-24564) | Add test suite for RecordBinaryComparator |  Minor | SQL | Xingbo Jiang | Xingbo Jiang |
| [SPARK-24740](https://issues.apache.org/jira/browse/SPARK-24740) | PySpark tests do not pass with NumPy 0.14.x+ |  Minor | ML, PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24562](https://issues.apache.org/jira/browse/SPARK-24562) | Allow running same tests with multiple configs in SQLQueryTestSuite |  Trivial | SQL, Tests | Marco Gaido | Marco Gaido |
| [SPARK-24840](https://issues.apache.org/jira/browse/SPARK-24840) | do not use dummy filter to switch codegen on/off |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-24861](https://issues.apache.org/jira/browse/SPARK-24861) | create corrected temp directories in RateSourceSuite |  Major | Structured Streaming | Wenchen Fan | Wenchen Fan |
| [SPARK-24886](https://issues.apache.org/jira/browse/SPARK-24886) | Increase Jenkins build time |  Major | Project Infra | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-25141](https://issues.apache.org/jira/browse/SPARK-25141) | Modify tests for higher-order functions to check bind method. |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-25184](https://issues.apache.org/jira/browse/SPARK-25184) | Flaky test: FlatMapGroupsWithState "streaming with processing time timeout" |  Minor | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-25249](https://issues.apache.org/jira/browse/SPARK-25249) | Add a unit test for OpenHashMap |  Trivial | Tests | liuxian | liuxian |
| [SPARK-25296](https://issues.apache.org/jira/browse/SPARK-25296) | Create ExplainSuite |  Major | SQL | Xiao Li | Xiao Li |
| [SPARK-25290](https://issues.apache.org/jira/browse/SPARK-25290) | BytesToBytesMapOnHeapSuite randomizedStressTest can cause OutOfMemoryError |  Major | Spark Core | L. C. Hsieh | L. C. Hsieh |
| [SPARK-25267](https://issues.apache.org/jira/browse/SPARK-25267) | Disable ConvertToLocalRelation in the test cases of sql/core and sql/hive |  Major | SQL | Xiao Li | Dilip Biswal |
| [SPARK-25238](https://issues.apache.org/jira/browse/SPARK-25238) | Lint-Python: Upgrading to the current version of pycodestyle fails |  Minor | Tests | cclauss | cclauss |
| [SPARK-25456](https://issues.apache.org/jira/browse/SPARK-25456) | PythonForeachWriterSuite failing |  Blocker | SQL | Imran Rashid | Imran Rashid |
| [SPARK-25422](https://issues.apache.org/jira/browse/SPARK-25422) | flaky test: org.apache.spark.DistributedSuite.caching on disk, replicated (encryption = on) (with replication as stream) |  Major | Spark Core | Wenchen Fan | Imran Rashid |
| [SPARK-25453](https://issues.apache.org/jira/browse/SPARK-25453) | OracleIntegrationSuite IllegalArgumentException: Timestamp format must be yyyy-mm-dd hh:mm:ss[.fffffffff] |  Major | Tests | Yuming Wang | Chenxiao Mao |
| [SPARK-25673](https://issues.apache.org/jira/browse/SPARK-25673) | Remove Travis CI which enables Java lint check |  Minor | Build | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-25736](https://issues.apache.org/jira/browse/SPARK-25736) | add tests to verify the behavior of multi-column count |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-25805](https://issues.apache.org/jira/browse/SPARK-25805) | Flaky test: DataFrameSuite.SPARK-25159 unittest failure |  Minor | SQL | Imran Rashid | Imran Rashid |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-12850](https://issues.apache.org/jira/browse/SPARK-12850) | Support bucket pruning (predicate pushdown for bucketed tables) |  Major | SQL | Reynold Xin | Xiao Li |
| [SPARK-23046](https://issues.apache.org/jira/browse/SPARK-23046) | Have RFormula include VectorSizeHint in pipeline |  Major | ML | Bago Amirbekian | Bago Amirbekian |
| [SPARK-22274](https://issues.apache.org/jira/browse/SPARK-22274) | User-defined aggregation functions with pandas udf |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-23344](https://issues.apache.org/jira/browse/SPARK-23344) | Add KMeans distanceMeasure param to PySpark |  Minor | ML, PySpark | Marco Gaido | Marco Gaido |
| [SPARK-22624](https://issues.apache.org/jira/browse/SPARK-22624) | Expose range partitioning shuffle introduced by SPARK-22614 |  Major | PySpark | Adrian Ionescu | Bo Xu |
| [SPARK-23352](https://issues.apache.org/jira/browse/SPARK-23352) | Explicitly specify supported types in Pandas UDFs |  Major | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23323](https://issues.apache.org/jira/browse/SPARK-23323) | DataSourceV2 should use the output commit coordinator. |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-23362](https://issues.apache.org/jira/browse/SPARK-23362) | Migrate Kafka microbatch source to v2 |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23203](https://issues.apache.org/jira/browse/SPARK-23203) | DataSourceV2 should use immutable trees. |  Blocker | SQL | Ryan Blue | Ryan Blue |
| [SPARK-23418](https://issues.apache.org/jira/browse/SPARK-23418) | DataSourceV2 should not allow userSpecifiedSchema without ReadSupportWithSchema |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-23491](https://issues.apache.org/jira/browse/SPARK-23491) | continuous symptom |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23097](https://issues.apache.org/jira/browse/SPARK-23097) | Migrate text socket source to v2 |  Major | Structured Streaming | Jose Torres | Saisai Shao |
| [SPARK-23585](https://issues.apache.org/jira/browse/SPARK-23585) | Add interpreted execution for UnwrapOption expression |  Major | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23559](https://issues.apache.org/jira/browse/SPARK-23559) | add epoch ID to data writer factory |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23586](https://issues.apache.org/jira/browse/SPARK-23586) | Add interpreted execution for WrapOption expression |  Major | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23594](https://issues.apache.org/jira/browse/SPARK-23594) | Add interpreted execution for GetExternalRowField expression |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-23590](https://issues.apache.org/jira/browse/SPARK-23590) | Add interpreted execution for CreateExternalRow expression |  Major | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23611](https://issues.apache.org/jira/browse/SPARK-23611) | Extend ExpressionEvalHelper harness to also test failures |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-23591](https://issues.apache.org/jira/browse/SPARK-23591) | Add interpreted execution for EncodeUsingSerializer expression |  Major | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23380](https://issues.apache.org/jira/browse/SPARK-23380) | Adds a conf for Arrow fallback in toPandas/createDataFrame with Pandas DataFrame |  Major | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23011](https://issues.apache.org/jira/browse/SPARK-23011) | Support alternative function form with group aggregate pandas UDF |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-23592](https://issues.apache.org/jira/browse/SPARK-23592) | Add interpreted execution for DecodeUsingSerializer expression |  Major | SQL | Herman van Hövell | Marco Gaido |
| [SPARK-23581](https://issues.apache.org/jira/browse/SPARK-23581) | Add an interpreted version of GenerateUnsafeProjection |  Major | SQL | Herman van Hövell | Herman van Hövell |
| [SPARK-23706](https://issues.apache.org/jira/browse/SPARK-23706) | spark.conf.get(value, default=None) should produce None in PySpark |  Minor | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-21898](https://issues.apache.org/jira/browse/SPARK-21898) | Feature parity for KolmogorovSmirnovTest in MLlib |  Minor | ML, MLlib | Weichen Xu | Weichen Xu |
| [SPARK-10884](https://issues.apache.org/jira/browse/SPARK-10884) | Support prediction on single instance for regression and classification related models |  Major | ML | Yanbo Liang | Weichen Xu |
| [SPARK-23577](https://issues.apache.org/jira/browse/SPARK-23577) | Supports line separator for text datasource |  Major | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-11239](https://issues.apache.org/jira/browse/SPARK-11239) | PMML export for ML linear regression |  Major | ML | Holden Karau | Holden Karau |
| [SPARK-23783](https://issues.apache.org/jira/browse/SPARK-23783) | Add new generic export trait for ML pipelines |  Major | ML | Holden Karau | Holden Karau |
| [SPARK-23615](https://issues.apache.org/jira/browse/SPARK-23615) | Add maxDF Parameter to Python CountVectorizer |  Minor | ML, PySpark | Bryan Cutler | Huaxin Gao |
| [SPARK-23096](https://issues.apache.org/jira/browse/SPARK-23096) | Migrate rate source to v2 |  Major | Structured Streaming | Jose Torres | Saisai Shao |
| [SPARK-23765](https://issues.apache.org/jira/browse/SPARK-23765) | Supports line separator for json datasource |  Major | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23727](https://issues.apache.org/jira/browse/SPARK-23727) | Support DATE predict push down in parquet |  Major | SQL | yucai | yucai |
| [SPARK-23713](https://issues.apache.org/jira/browse/SPARK-23713) | Clean-up UnsafeWriter classes |  Major | SQL | Herman van Hövell | Kazuaki Ishizaki |
| [SPARK-23690](https://issues.apache.org/jira/browse/SPARK-23690) | VectorAssembler should have handleInvalid to handle columns with null values |  Major | ML | yogesh garg | yogesh garg |
| [SPARK-23099](https://issues.apache.org/jira/browse/SPARK-23099) | Migrate foreach sink |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23587](https://issues.apache.org/jira/browse/SPARK-23587) | Add interpreted execution for MapObjects expression |  Major | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-23826](https://issues.apache.org/jira/browse/SPARK-23826) | TestHiveSparkSession should set default session |  Major | SQL | Jose Torres | Xiao Li |
| [SPARK-23583](https://issues.apache.org/jira/browse/SPARK-23583) | Add interpreted execution to Invoke expression |  Major | SQL | Herman van Hövell | Kazuaki Ishizaki |
| [SPARK-23593](https://issues.apache.org/jira/browse/SPARK-23593) | Add interpreted execution for InitializeJavaBean expression |  Major | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-23582](https://issues.apache.org/jira/browse/SPARK-23582) | Add interpreted execution to StaticInvoke expression |  Major | SQL | Herman van Hövell | Kazuaki Ishizaki |
| [SPARK-23870](https://issues.apache.org/jira/browse/SPARK-23870) |  Forward RFormula handleInvalid Param to VectorAssembler |  Major | ML | yogesh garg | yogesh garg |
| [SPARK-23859](https://issues.apache.org/jira/browse/SPARK-23859) | Initial PR for Instrumentation improvements: UUID and logging levels |  Major | ML | Joseph K. Bradley | Weichen Xu |
| [SPARK-23847](https://issues.apache.org/jira/browse/SPARK-23847) | Add asc\_nulls\_first, asc\_nulls\_last to PySpark |  Minor | PySpark, SQL | Huaxin Gao | Huaxin Gao |
| [SPARK-23864](https://issues.apache.org/jira/browse/SPARK-23864) | Add Unsafe\* copy methods to UnsafeWriter |  Major | SQL | Herman van Hövell | Herman van Hövell |
| [SPARK-23871](https://issues.apache.org/jira/browse/SPARK-23871) | add python api for VectorAssembler handleInvalid |  Minor | ML, PySpark | yogesh garg | Huaxin Gao |
| [SPARK-23762](https://issues.apache.org/jira/browse/SPARK-23762) | UTF8StringBuilder uses MemoryBlock |  Major | SQL | Kazuaki Ishizaki | Kazuaki Ishizaki |
| [SPARK-23748](https://issues.apache.org/jira/browse/SPARK-23748) | Support select from temp tables |  Major | Structured Streaming | Jose Torres | Saisai Shao |
| [SPARK-23942](https://issues.apache.org/jira/browse/SPARK-23942) | PySpark's collect doesn't trigger QueryExecutionListener |  Major | PySpark, SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23905](https://issues.apache.org/jira/browse/SPARK-23905) | Add UDF weekday |  Major | SQL | Xiao Li | yucai |
| [SPARK-23917](https://issues.apache.org/jira/browse/SPARK-23917) | High-order function: array\_max(x) → x |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-21088](https://issues.apache.org/jira/browse/SPARK-21088) | CrossValidator, TrainValidationSplit should collect all models when fitting: Python API |  Major | ML, PySpark | Joseph K. Bradley | Weichen Xu |
| [SPARK-23918](https://issues.apache.org/jira/browse/SPARK-23918) | High-order function: array\_min(x) → x |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-23747](https://issues.apache.org/jira/browse/SPARK-23747) | Add EpochCoordinator unit tests |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23341](https://issues.apache.org/jira/browse/SPARK-23341) | DataSourceOptions should handle path and table names to avoid confusion. |  Major | SQL | Ryan Blue | Wenchen Fan |
| [SPARK-23926](https://issues.apache.org/jira/browse/SPARK-23926) | High-order function: reverse(x) → array |  Major | SQL | Xiao Li | Marek Novotny |
| [SPARK-23919](https://issues.apache.org/jira/browse/SPARK-23919) | High-order function: array\_position(x, element) → bigint |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-23924](https://issues.apache.org/jira/browse/SPARK-23924) | High-order function: element\_at |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-23584](https://issues.apache.org/jira/browse/SPARK-23584) | Add interpreted execution to NewInstance expression |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-23588](https://issues.apache.org/jira/browse/SPARK-23588) | Add interpreted execution for CatalystToExternalMap expression |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-24026](https://issues.apache.org/jira/browse/SPARK-24026) | spark.ml Scala/Java API for PIC |  Major | ML | Joseph K. Bradley | Miao Wang |
| [SPARK-22362](https://issues.apache.org/jira/browse/SPARK-22362) | Add unit test for Window Aggregate Functions |  Major | SQL | Xingbo Jiang | Attila Zsolt Piros |
| [SPARK-23736](https://issues.apache.org/jira/browse/SPARK-23736) | High-order function: concat(array1, array2, ..., arrayN) → array |  Major | SQL | Marek Novotny | Marek Novotny |
| [SPARK-23595](https://issues.apache.org/jira/browse/SPARK-23595) | Add interpreted execution for ValidateExternalType expression |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-23589](https://issues.apache.org/jira/browse/SPARK-23589) | Add interpreted execution for ExternalMapToCatalyst expression |  Major | SQL | Herman van Hövell | Takeshi Yamamuro |
| [SPARK-24054](https://issues.apache.org/jira/browse/SPARK-24054) | Add array\_position function /  element\_at functions |  Major | SparkR | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23807](https://issues.apache.org/jira/browse/SPARK-23807) | Add Hadoop 3 profile with relevant POM fix ups |  Major | Build | Steve Loughran | Steve Loughran |
| [SPARK-23990](https://issues.apache.org/jira/browse/SPARK-23990) | Instruments logging improvements - ML regression package |  Major | ML | Weichen Xu | Weichen Xu |
| [SPARK-24038](https://issues.apache.org/jira/browse/SPARK-24038) | refactor continuous write exec to its own class |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-23821](https://issues.apache.org/jira/browse/SPARK-23821) | High-order function: flatten(x) → array |  Major | SQL | Marek Novotny | Marek Novotny |
| [SPARK-24069](https://issues.apache.org/jira/browse/SPARK-24069) | Add array\_max / array\_min functions |  Major | SparkR | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23902](https://issues.apache.org/jira/browse/SPARK-23902) | Provide an option in months\_between UDF to disable rounding-off |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-23916](https://issues.apache.org/jira/browse/SPARK-23916) | High-order function: array\_join(x, delimiter, null\_replacement) → varchar |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-23688](https://issues.apache.org/jira/browse/SPARK-23688) | Refactor tests away from rate source |  Major | Structured Streaming | Jose Torres | Jungtaek Lim |
| [SPARK-23723](https://issues.apache.org/jira/browse/SPARK-23723) | New encoding option for json datasource |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-23724](https://issues.apache.org/jira/browse/SPARK-23724) | Custom record separator for jsons in charsets different from UTF-8 |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-23923](https://issues.apache.org/jira/browse/SPARK-23923) | High-order function: cardinality(x) → bigint |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-24039](https://issues.apache.org/jira/browse/SPARK-24039) | remove restarting iterators hack |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-24157](https://issues.apache.org/jira/browse/SPARK-24157) | Enable no-data micro batches for streaming aggregation and deduplication |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24185](https://issues.apache.org/jira/browse/SPARK-24185) | add  flatten function |  Major | SparkR | Huaxin Gao | Huaxin Gao |
| [SPARK-23921](https://issues.apache.org/jira/browse/SPARK-23921) | High-order function: array\_sort(x) → array |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-23930](https://issues.apache.org/jira/browse/SPARK-23930) | High-order function: slice(x, start, length) → array |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-20114](https://issues.apache.org/jira/browse/SPARK-20114) | spark.ml parity for sequential pattern mining - PrefixSpan |  Major | ML | yuhao yang | Weichen Xu |
| [SPARK-24132](https://issues.apache.org/jira/browse/SPARK-24132) | Instrumentation improvement for classification |  Major | ML | Lu Wang | Lu Wang |
| [SPARK-24073](https://issues.apache.org/jira/browse/SPARK-24073) | DataSourceV2: Rename DataReaderFactory to InputPartition. |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-24197](https://issues.apache.org/jira/browse/SPARK-24197) | add array\_sort function |  Major | SparkR | Marek Novotny | Marek Novotny |
| [SPARK-24198](https://issues.apache.org/jira/browse/SPARK-24198) | add slice function |  Major | SparkR | Marek Novotny | Marek Novotny |
| [SPARK-24186](https://issues.apache.org/jira/browse/SPARK-24186) | add array\_reverse and concat |  Major | SparkR | Huaxin Gao | Huaxin Gao |
| [SPARK-24155](https://issues.apache.org/jira/browse/SPARK-24155) | Instrumentation improvement for clustering |  Major | ML | Lu Wang | Lu Wang |
| [SPARK-24040](https://issues.apache.org/jira/browse/SPARK-24040) | support single partition aggregates |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-24158](https://issues.apache.org/jira/browse/SPARK-24158) | Enable no-data micro batches for streaming joins |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23925](https://issues.apache.org/jira/browse/SPARK-23925) | High-order function: repeat(element, count) → array |  Major | SQL | Xiao Li | Florent Pepin |
| [SPARK-23922](https://issues.apache.org/jira/browse/SPARK-23922) | High-order function: arrays\_overlap(x, y) → boolean |  Major | SQL | Xiao Li | Marco Gaido |
| [SPARK-24115](https://issues.apache.org/jira/browse/SPARK-24115) | improve instrumentation for spark.ml.tuning |  Major | ML | yogesh garg | Bago Amirbekian |
| [SPARK-24310](https://issues.apache.org/jira/browse/SPARK-24310) | Instrumentation for frequent pattern mining |  Major | ML | Joseph K. Bradley | Bago Amirbekian |
| [SPARK-24159](https://issues.apache.org/jira/browse/SPARK-24159) | Enable no-data micro batches for streaming mapGroupswithState |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-23503](https://issues.apache.org/jira/browse/SPARK-23503) | continuous execution should sequence committed epochs |  Major | Structured Streaming | Jose Torres | Efim Poberezkin |
| [SPARK-24234](https://issues.apache.org/jira/browse/SPARK-24234) | create the bottom-of-task RDD with row buffer |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-24325](https://issues.apache.org/jira/browse/SPARK-24325) | Tests for Hadoop's LinesReader |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-23711](https://issues.apache.org/jira/browse/SPARK-23711) | Add fallback to interpreted execution logic |  Major | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-24334](https://issues.apache.org/jira/browse/SPARK-24334) | Race condition in ArrowPythonRunner causes unclean shutdown of Arrow memory allocator |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-24331](https://issues.apache.org/jira/browse/SPARK-24331) | Add arrays\_overlap / array\_repeat / map\_entries |  Major | SparkR | Marek Novotny | Marek Novotny |
| [SPARK-24419](https://issues.apache.org/jira/browse/SPARK-24419) | Upgrade SBT to 0.13.17 with Scala 2.10.7 |  Major | Build | DB Tsai | DB Tsai |
| [SPARK-24146](https://issues.apache.org/jira/browse/SPARK-24146) | spark.ml parity for sequential pattern mining - PrefixSpan: Python API |  Major | ML, PySpark | Weichen Xu | Weichen Xu |
| [SPARK-23900](https://issues.apache.org/jira/browse/SPARK-23900) | format\_number udf should take user specifed format as argument |  Major | SQL | Xiao Li | Yuming Wang |
| [SPARK-23920](https://issues.apache.org/jira/browse/SPARK-23920) | High-order function: array\_remove(x, element) → array |  Major | SQL | Xiao Li | Huaxin Gao |
| [SPARK-23903](https://issues.apache.org/jira/browse/SPARK-23903) | Add support for date extract |  Major | SQL | Xiao Li | Yuming Wang |
| [SPARK-24290](https://issues.apache.org/jira/browse/SPARK-24290) | Instrumentation Improvement: add logNamedValue taking Array types |  Major | ML | Lu Wang | Lu Wang |
| [SPARK-24187](https://issues.apache.org/jira/browse/SPARK-24187) | add array\_join |  Major | SparkR | Huaxin Gao | Huaxin Gao |
| [SPARK-24119](https://issues.apache.org/jira/browse/SPARK-24119) | Add interpreted execution to SortPrefix expression |  Minor | SQL | Bruce Robbins | Bruce Robbins |
| [SPARK-19826](https://issues.apache.org/jira/browse/SPARK-19826) | spark.ml Python API for PIC |  Major | ML, PySpark | Felix Cheung | Huaxin Gao |
| [SPARK-23931](https://issues.apache.org/jira/browse/SPARK-23931) | High-order function: array\_zip(array1, array2[, ...]) → array\<row\> |  Major | SQL | Xiao Li | Dylan Guedes |
| [SPARK-23933](https://issues.apache.org/jira/browse/SPARK-23933) | High-order function: map(array\<K\>, array\<V\>) → map\<K,V\> |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-22239](https://issues.apache.org/jira/browse/SPARK-22239) | User-defined window functions with pandas udf (unbounded window) |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-24235](https://issues.apache.org/jira/browse/SPARK-24235) | create the top-of-task RDD sending rows to the remote buffer |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-14376](https://issues.apache.org/jira/browse/SPARK-14376) | spark.ml parity for trees |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-24478](https://issues.apache.org/jira/browse/SPARK-24478) | DataSourceV2 should push filters and projection at physical plan conversion |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-23912](https://issues.apache.org/jira/browse/SPARK-23912) | High-order function: array\_distinct(x) → array |  Major | SQL | Xiao Li | Huaxin Gao |
| [SPARK-23934](https://issues.apache.org/jira/browse/SPARK-23934) | High-order function: map\_from\_entries(array\<row\<K, V\>\>) → map\<K,V\> |  Major | SQL | Xiao Li | Marek Novotny |
| [SPARK-24324](https://issues.apache.org/jira/browse/SPARK-24324) | Pandas Grouped Map UserDefinedFunction mixes column labels |  Major | PySpark | Cristian Consonni | Bryan Cutler |
| [SPARK-24418](https://issues.apache.org/jira/browse/SPARK-24418) | Upgrade to Scala 2.11.12 |  Major | Build | DB Tsai | DB Tsai |
| [SPARK-6237](https://issues.apache.org/jira/browse/SPARK-6237) | Support uploading blocks \> 2GB as a stream |  Major | Shuffle, Spark Core | Reynold Xin | Imran Rashid |
| [SPARK-23927](https://issues.apache.org/jira/browse/SPARK-23927) | High-order function: sequence |  Major | SQL | Xiao Li | Alex Vayda |
| [SPARK-23120](https://issues.apache.org/jira/browse/SPARK-23120) | Add PMML pipeline export support to PySpark |  Major | ML, PySpark | Holden Karau | Holden Karau |
| [SPARK-24439](https://issues.apache.org/jira/browse/SPARK-24439) | Add distanceMeasure to BisectingKMeans in PySpark |  Minor | ML, PySpark | Huaxin Gao | Huaxin Gao |
| [SPARK-24386](https://issues.apache.org/jira/browse/SPARK-24386) | implement continuous processing coalesce(1) |  Major | Structured Streaming | Jose Torres | Jose Torres |
| [SPARK-24638](https://issues.apache.org/jira/browse/SPARK-24638) | StringStartsWith support push down |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-24420](https://issues.apache.org/jira/browse/SPARK-24420) | Upgrade ASM to 6.x to support JDK9+ |  Major | Build | DB Tsai | DB Tsai |
| [SPARK-24716](https://issues.apache.org/jira/browse/SPARK-24716) | Refactor ParquetFilters |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-24535](https://issues.apache.org/jira/browse/SPARK-24535) | Fix java version parsing in SparkR on Windows |  Blocker | SparkR | Shivaram Venkataraman | Felix Cheung |
| [SPARK-23936](https://issues.apache.org/jira/browse/SPARK-23936) | High-order function: map\_concat(map1\<K, V\>, map2\<K, V\>, ..., mapN\<K, V\>) → map\<K,V\> |  Major | SQL | Xiao Li | Bruce Robbins |
| [SPARK-24706](https://issues.apache.org/jira/browse/SPARK-24706) | Support ByteType and ShortType pushdown to parquet |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-23914](https://issues.apache.org/jira/browse/SPARK-23914) | High-order function: array\_union(x, y) → array |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-24537](https://issues.apache.org/jira/browse/SPARK-24537) | Add array\_remove / array\_zip / map\_from\_arrays / array\_distinct |  Major | SparkR | Huaxin Gao | Huaxin Gao |
| [SPARK-17091](https://issues.apache.org/jira/browse/SPARK-17091) | Convert IN predicate to equivalent Parquet filter |  Major | SQL | Andrew Duffy | Yuming Wang |
| [SPARK-24718](https://issues.apache.org/jira/browse/SPARK-24718) | Timestamp support pushdown to parquet data source |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-24776](https://issues.apache.org/jira/browse/SPARK-24776) | AVRO unit test: use SQLTestUtils and Replace deprecated methods |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24800](https://issues.apache.org/jira/browse/SPARK-24800) | Refactor Avro Serializer and Deserializer |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24810](https://issues.apache.org/jira/browse/SPARK-24810) | Fix paths to resource files in AvroSuite |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24805](https://issues.apache.org/jira/browse/SPARK-24805) | Don't ignore files without .avro extension by default |  Major | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24070](https://issues.apache.org/jira/browse/SPARK-24070) | TPC-DS Performance Tests for Parquet 1.10.0 Upgrade |  Major | SQL | Xiao Li | Takeshi Yamamuro |
| [SPARK-24854](https://issues.apache.org/jira/browse/SPARK-24854) | Gather all options into AvroOptions |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-22187](https://issues.apache.org/jira/browse/SPARK-22187) | Update unsaferow format for saved state such that we can set timeouts when state is null |  Major | Structured Streaming | Tathagata Das | Tathagata Das |
| [SPARK-24307](https://issues.apache.org/jira/browse/SPARK-24307) | Support sending messages over 2GB from memory |  Major | Block Manager, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-24811](https://issues.apache.org/jira/browse/SPARK-24811) | Add function \`from\_avro\` and \`to\_avro\` |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24876](https://issues.apache.org/jira/browse/SPARK-24876) | Simplify schema serialization |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24836](https://issues.apache.org/jira/browse/SPARK-24836) | New option - ignoreExtension |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24883](https://issues.apache.org/jira/browse/SPARK-24883) | Remove implicit class AvroDataFrameWriter/AvroDataFrameReader |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24887](https://issues.apache.org/jira/browse/SPARK-24887) | Use SerializableConfiguration in Spark util |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23325](https://issues.apache.org/jira/browse/SPARK-23325) | DataSourceV2 readers should always produce InternalRow. |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-24297](https://issues.apache.org/jira/browse/SPARK-24297) | Change default value for spark.maxRemoteBlockSizeFetchToMem to be \< 2GB |  Major | Block Manager, Shuffle, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-24924](https://issues.apache.org/jira/browse/SPARK-24924) | Add mapping for built-in Avro data source |  Minor | SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-23928](https://issues.apache.org/jira/browse/SPARK-23928) | High-order function: shuffle(x) → array |  Major | SQL | Xiao Li | Huizhi Lu |
| [SPARK-24881](https://issues.apache.org/jira/browse/SPARK-24881) | New options - compression and compressionLevel |  Minor | SQL | Maxim Gekk | Maxim Gekk |
| [SPARK-24624](https://issues.apache.org/jira/browse/SPARK-24624) | Can not mix vectorized and non-vectorized UDFs |  Major | SQL | Xiao Li | Li Jin |
| [SPARK-24967](https://issues.apache.org/jira/browse/SPARK-24967) | Use internal.Logging instead for logging |  Minor | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24771](https://issues.apache.org/jira/browse/SPARK-24771) | Upgrade AVRO version from 1.7.7 to 1.8.2 |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23633](https://issues.apache.org/jira/browse/SPARK-23633) |  Update Pandas UDFs section in sql-programming-guide |  Major | PySpark | Li Jin | Li Jin |
| [SPARK-24976](https://issues.apache.org/jira/browse/SPARK-24976) | Allow None for Decimal type conversion (specific to PyArrow 0.9.0) |  Major | PySpark | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24971](https://issues.apache.org/jira/browse/SPARK-24971) | remove SupportsDeprecatedScanRow |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-23915](https://issues.apache.org/jira/browse/SPARK-23915) | High-order function: array\_except(x, y) → array |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-24990](https://issues.apache.org/jira/browse/SPARK-24990) | merge ReadSupport and ReadSupportWithSchema |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-14540](https://issues.apache.org/jira/browse/SPARK-14540) | Support Scala 2.12 closures and Java 8 lambdas in ClosureCleaner |  Major | Spark Core | Josh Rosen | Stavros Kontopoulos |
| [SPARK-23908](https://issues.apache.org/jira/browse/SPARK-23908) | High-order function: transform(array\<T\>, function\<T, U\>) → array\<U\> |  Major | SQL | Xiao Li | Takuya Ueshin |
| [SPARK-24773](https://issues.apache.org/jira/browse/SPARK-24773) | support reading AVRO logical types - Timestamp with different precisions |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25002](https://issues.apache.org/jira/browse/SPARK-25002) | Avro: revise the output record namespace |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23909](https://issues.apache.org/jira/browse/SPARK-23909) | High-order function: filter(array\<T\>, function\<T, boolean\>) → array\<T\> |  Major | SQL | Xiao Li | Takuya Ueshin |
| [SPARK-23911](https://issues.apache.org/jira/browse/SPARK-23911) | High-order function: aggregate(array\<T\>, initialState S, inputFunction\<S, T, S\>, outputFunction\<S, R\>) → R |  Major | SQL | Xiao Li | Takuya Ueshin |
| [SPARK-24991](https://issues.apache.org/jira/browse/SPARK-24991) | use InternalRow in DataSourceWriter |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-23913](https://issues.apache.org/jira/browse/SPARK-23913) | High-order function: array\_intersect(x, y) → array |  Major | SQL | Xiao Li | Kazuaki Ishizaki |
| [SPARK-24772](https://issues.apache.org/jira/browse/SPARK-24772) | support reading AVRO logical types - Date |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24251](https://issues.apache.org/jira/browse/SPARK-24251) | DataSourceV2: Add AppendData logical operation |  Major | SQL | Ryan Blue | Ryan Blue |
| [SPARK-23596](https://issues.apache.org/jira/browse/SPARK-23596) | Modify Dataset test harness to include interpreted execution |  Major | SQL | Herman van Hövell | L. C. Hsieh |
| [SPARK-25047](https://issues.apache.org/jira/browse/SPARK-25047) | Can't assign SerializedLambda to scala.Function1 in deserialization of BucketedRandomProjectionLSHModel |  Major | ML | Sean R. Owen | Sean R. Owen |
| [SPARK-25068](https://issues.apache.org/jira/browse/SPARK-25068) | High-order function: exists(array\<T\>, function\<T, boolean\>) → boolean |  Major | SQL | Takuya Ueshin | Takuya Ueshin |
| [SPARK-24774](https://issues.apache.org/jira/browse/SPARK-24774) | support reading AVRO logical types - Decimal |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25099](https://issues.apache.org/jira/browse/SPARK-25099) | Generate Avro Binary files in test suite |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25104](https://issues.apache.org/jira/browse/SPARK-25104) | Validate user specified output schema |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-23932](https://issues.apache.org/jira/browse/SPARK-23932) | High-order function: zip\_with(array\<T\>, array\<U\>, function\<T, U, R\>) → array\<R\> |  Major | SQL | Xiao Li | Sandeep Singh |
| [SPARK-23555](https://issues.apache.org/jira/browse/SPARK-23555) | Add BinaryType support for Arrow in PySpark |  Major | PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-25160](https://issues.apache.org/jira/browse/SPARK-25160) | Remove sql configuration spark.sql.avro.outputTimestampType |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-24296](https://issues.apache.org/jira/browse/SPARK-24296) | Support replicating blocks larger than 2 GB |  Major | Block Manager, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-6236](https://issues.apache.org/jira/browse/SPARK-6236) | Support caching blocks larger than 2G |  Major | Shuffle, Spark Core | Reynold Xin |  |
| [SPARK-25127](https://issues.apache.org/jira/browse/SPARK-25127) | DataSourceV2: Remove SupportsPushDownCatalystFilters |  Major | SQL | Ryan Blue | Reynold Xin |
| [SPARK-25133](https://issues.apache.org/jira/browse/SPARK-25133) | Documentaion: AVRO data source guide |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25029](https://issues.apache.org/jira/browse/SPARK-25029) | Scala 2.12 issues: TaskNotSerializable and Janino "Two non-abstract methods ..." errors |  Major | Build | Sean R. Owen | Sean R. Owen |
| [SPARK-23030](https://issues.apache.org/jira/browse/SPARK-23030) | Decrease memory consumption with toPandas() collection using Arrow |  Major | PySpark, SQL | Bryan Cutler | Bryan Cutler |
| [SPARK-25044](https://issues.apache.org/jira/browse/SPARK-25044) | Address translation of LMF closure primitive args to Object in Scala 2.12 |  Major | Spark Core, SQL | Sean R. Owen | Sean R. Owen |
| [SPARK-25256](https://issues.apache.org/jira/browse/SPARK-25256) | Plan mismatch errors in Hive tests in 2.12 |  Major | SQL | Sean R. Owen | Darcy Shen |
| [SPARK-25207](https://issues.apache.org/jira/browse/SPARK-25207) | Case-insensitve field resolution for filter pushdown when reading Parquet |  Major | SQL | yucai | yucai |
| [SPARK-25007](https://issues.apache.org/jira/browse/SPARK-25007) | Add array\_intersect / array\_except /array\_union / array\_shuffle to SparkR |  Major | SparkR | Huaxin Gao | Huaxin Gao |
| [SPARK-25304](https://issues.apache.org/jira/browse/SPARK-25304) | enable HiveSparkSubmitSuite SPARK-8489 test for Scala 2.12 |  Minor | SQL | Darcy Shen | Darcy Shen |
| [SPARK-25298](https://issues.apache.org/jira/browse/SPARK-25298) | spark-tools build failure for Scala 2.12 |  Minor | Build | Darcy Shen | Darcy Shen |
| [SPARK-25337](https://issues.apache.org/jira/browse/SPARK-25337) | HiveExternalCatalogVersionsSuite + Scala 2.12 = NoSuchMethodError: org.apache.spark.sql.execution.datasources.FileFormat.$init$(Lorg/apache/spark/sql/execution/datasources/FileFormat;) |  Major | SQL | Sean R. Owen | Dongjoon Hyun |
| [SPARK-25328](https://issues.apache.org/jira/browse/SPARK-25328) | Add an example for having two columns as the grouping key in group aggregate pandas UDF |  Major | PySpark | Xiao Li | Hyukjin Kwon |
| [SPARK-24549](https://issues.apache.org/jira/browse/SPARK-24549) | Support DecimalType push down to the parquet data sources |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-25460](https://issues.apache.org/jira/browse/SPARK-25460) | DataSourceV2: Structured Streaming does not respect SessionConfigSupport |  Major | SQL, Structured Streaming | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-24777](https://issues.apache.org/jira/browse/SPARK-24777) | Add write benchmark for AVRO |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25321](https://issues.apache.org/jira/browse/SPARK-25321) | ML, Graph 2.4 QA: API: New Scala APIs, docs |  Blocker | Documentation, GraphX, ML, MLlib | Weichen Xu | Weichen Xu |
| [SPARK-25320](https://issues.apache.org/jira/browse/SPARK-25320) | ML, Graph 2.4 QA: API: Binary incompatible changes |  Blocker | Documentation, GraphX, ML, MLlib | Weichen Xu | Weichen Xu |
| [SPARK-25572](https://issues.apache.org/jira/browse/SPARK-25572) | SparkR tests failed on CRAN on Java 10 |  Major | SparkR | Felix Cheung | Felix Cheung |
| [SPARK-23401](https://issues.apache.org/jira/browse/SPARK-23401) | Improve test cases for all supported types and unsupported types |  Minor | PySpark | Hyukjin Kwon | Aleksandr Koriagin |
| [SPARK-25601](https://issues.apache.org/jira/browse/SPARK-25601) | Register Grouped aggregate UDF Vectorized UDFs for SQL Statement |  Major | PySpark, SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-23597](https://issues.apache.org/jira/browse/SPARK-23597) | Audit Spark SQL code base for non-interpreted expressions |  Major | SQL | Herman van Hövell |  |
| [SPARK-25690](https://issues.apache.org/jira/browse/SPARK-25690) | Analyzer rule "HandleNullInputsForUDF" does not stabilize and can be applied infinitely |  Major | Spark Core, SQL | Wei Xue | Wei Xue |
| [SPARK-25718](https://issues.apache.org/jira/browse/SPARK-25718) | Detect recursive reference in Avro schema and throw exception |  Major | SQL | Gengliang Wang | Gengliang Wang |
| [SPARK-25842](https://issues.apache.org/jira/browse/SPARK-25842) | Deprecate APIs introduced in SPARK-21608 |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-25179](https://issues.apache.org/jira/browse/SPARK-25179) | Document the features that require Pyarrow 0.10 |  Major | PySpark | Xiao Li | Hyukjin Kwon |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-23256](https://issues.apache.org/jira/browse/SPARK-23256) | Add columnSchema method to PySpark image reader |  Minor | ML, PySpark | Nicholas Pentreath | Hyukjin Kwon |
| [SPARK-23509](https://issues.apache.org/jira/browse/SPARK-23509) | Upgrade commons-net from 2.2 to 3.1 |  Minor | Spark Core | PandaMonkey | Kazuaki Ishizaki |
| [SPARK-23566](https://issues.apache.org/jira/browse/SPARK-23566) | Arguement name fix |  Minor | Documentation | Anirudh | Anirudh |
| [SPARK-23329](https://issues.apache.org/jira/browse/SPARK-23329) | Update the function descriptions with the arguments and returned values of the trigonometric functions |  Minor | SQL | Xiao Li | Mihaly Toth |
| [SPARK-23642](https://issues.apache.org/jira/browse/SPARK-23642) | isZero scaladoc for LongAccumulator describes wrong method |  Minor | Documentation | Sean | Sean |
| [SPARK-24124](https://issues.apache.org/jira/browse/SPARK-24124) | Spark history server should create spark.history.store.path and set permissions properly |  Major | Spark Core | Thomas Graves | Thomas Graves |
| [SPARK-24378](https://issues.apache.org/jira/browse/SPARK-24378) | Incorrect examples for date\_trunc function in spark 2.3.0 |  Trivial | Documentation | Prakhar Gupta | Yuming Wang |
| [SPARK-24444](https://issues.apache.org/jira/browse/SPARK-24444) | Improve pandas\_udf GROUPED\_MAP docs to explain column assignment |  Major | PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-24224](https://issues.apache.org/jira/browse/SPARK-24224) | Java example code for Power Iteration Clustering in spark.ml |  Trivial | ML | shahid | shahid |
| [SPARK-24191](https://issues.apache.org/jira/browse/SPARK-24191) | Scala example code for Power Iteration Clustering in Spark ML examples |  Trivial | Documentation, Examples, ML | shahid | shahid |
| [SPARK-24134](https://issues.apache.org/jira/browse/SPARK-24134) | A missing full-stop in doc "Tuning Spark" |  Trivial | Documentation | Xiaodong Deng | Xiaodong Deng |
| [SPARK-21607](https://issues.apache.org/jira/browse/SPARK-21607) | Can dropTempView function add a param like dropTempView(viewName: String, dropSelfOnly: Boolean) |  Major | SQL | ant\_nebula | Wei Xue |
| [SPARK-24507](https://issues.apache.org/jira/browse/SPARK-24507) | Description in "Level of Parallelism in Data Receiving" section of Spark Streaming Programming Guide in is not relevan for the recent Kafka direct apprach |  Minor | Documentation, DStreams | Lev Greenberg | Rekha Joshi |
| [SPARK-23254](https://issues.apache.org/jira/browse/SPARK-23254) | Add user guide entry for DataFrame multivariate summary |  Minor | Documentation, ML | Nicholas Pentreath | Weichen Xu |
| [SPARK-24628](https://issues.apache.org/jira/browse/SPARK-24628) | Typos of the example code in docs/mllib-data-types.md |  Minor | MLlib | Weizhe Huang | Weizhe Huang |
| [SPARK-21261](https://issues.apache.org/jira/browse/SPARK-21261) | SparkSQL regexpExpressions example |  Minor | Examples | zhangxin | Sean R. Owen |
| [SPARK-24852](https://issues.apache.org/jira/browse/SPARK-24852) | Have spark.ml training use updated \`Instrumentation\` APIs. |  Major | ML | Bago Amirbekian | Bago Amirbekian |
| [SPARK-23231](https://issues.apache.org/jira/browse/SPARK-23231) | Add doc for string indexer ordering to user guide (also to RFormula guide) |  Minor | Documentation, ML | Nicholas Pentreath | zhengruifeng |
| [SPARK-25082](https://issues.apache.org/jira/browse/SPARK-25082) | Documentation for Spark Function expm1 is incomplete |  Trivial | Spark Core | Alexander Belov | Bo Meng |
| [SPARK-25234](https://issues.apache.org/jira/browse/SPARK-25234) | SparkR:::parallelize doesn't handle integer overflow properly |  Major | SparkR | Xiangrui Meng | Xiangrui Meng |
| [SPARK-23792](https://issues.apache.org/jira/browse/SPARK-23792) | Documentation improvements for datetime functions |  Minor | Documentation, SQL | A Bradbury | A Bradbury |
| [SPARK-24090](https://issues.apache.org/jira/browse/SPARK-24090) | Kubernetes Backend Hotlist for Spark 2.4 |  Major | Kubernetes, Scheduler, Spark Core | Anirudh Ramanathan | Anirudh Ramanathan |
| [SPARK-25273](https://issues.apache.org/jira/browse/SPARK-25273) | How to install testthat v1.0.2 |  Major | Documentation | Maxim Gekk | Maxim Gekk |
| [SPARK-20395](https://issues.apache.org/jira/browse/SPARK-20395) | Update Scala to 2.11.11 and zinc to 0.3.15 |  Minor | Build, Spark Core | Jeremy Smith | DB Tsai |
| [SPARK-25248](https://issues.apache.org/jira/browse/SPARK-25248) | Audit barrier APIs for Spark 2.4 |  Major | Spark Core | Xiangrui Meng | Xiangrui Meng |
| [SPARK-25258](https://issues.apache.org/jira/browse/SPARK-25258) | Upgrade kryo package to version 4.0.2 |  Major | Spark Core | liupengcheng | Yuming Wang |
| [SPARK-23131](https://issues.apache.org/jira/browse/SPARK-23131) | Kryo raises StackOverflow during serializing GLR model |  Minor | ML | Peigen | Yuming Wang |
| [SPARK-14220](https://issues.apache.org/jira/browse/SPARK-14220) | Build and test Spark against Scala 2.12 |  Blocker | Build, Project Infra | Josh Rosen | Sean R. Owen |
| [SPARK-25345](https://issues.apache.org/jira/browse/SPARK-25345) | Deprecate readImages APIs from ImageSchema |  Major | ML | Xiangrui Meng | Weichen Xu |
| [SPARK-23899](https://issues.apache.org/jira/browse/SPARK-23899) | Built-in SQL Function Improvement |  Major | SQL | Xiao Li |  |
| [SPARK-25419](https://issues.apache.org/jira/browse/SPARK-25419) | Parquet predicate pushdown improvement |  Major | SQL | Yuming Wang | Yuming Wang |
| [SPARK-25583](https://issues.apache.org/jira/browse/SPARK-25583) | Add newly added History server related configurations in the documentation |  Minor | Spark Core | shahid | shahid |
| [SPARK-25656](https://issues.apache.org/jira/browse/SPARK-25656) | Add an example section about how to use Parquet/ORC library options |  Major | Documentation, Examples, SQL | Dongjoon Hyun | Dongjoon Hyun |
| [SPARK-25347](https://issues.apache.org/jira/browse/SPARK-25347) | Document image data source in doc site |  Major | Documentation, ML | Xiangrui Meng | Weichen Xu |
| [SPARK-6235](https://issues.apache.org/jira/browse/SPARK-6235) | Address various 2G limits |  Major | Shuffle, Spark Core | Reynold Xin |  |
| [SPARK-23092](https://issues.apache.org/jira/browse/SPARK-23092) | Migrate MemoryStream to DataSource V2 |  Major | Structured Streaming | Burak Yavuz | Tathagata Das |
| [SPARK-23501](https://issues.apache.org/jira/browse/SPARK-23501) | Refactor AllStagesPage in order to avoid redundant code |  Trivial | Web UI | Marco Gaido | Marco Gaido |
| [SPARK-23601](https://issues.apache.org/jira/browse/SPARK-23601) | Remove .md5 files from release |  Minor | Build | Sean R. Owen | Sean R. Owen |
| [SPARK-23533](https://issues.apache.org/jira/browse/SPARK-23533) | Add support for changing ContinuousDataReader's startOffset |  Major | Structured Streaming | Yuanjian Li | Yuanjian Li |
| [SPARK-24392](https://issues.apache.org/jira/browse/SPARK-24392) | Mark pandas\_udf as Experimental |  Blocker | PySpark | Bryan Cutler | Bryan Cutler |
| [SPARK-24533](https://issues.apache.org/jira/browse/SPARK-24533) | typesafe has rebranded to lightbend. change the build/mvn endpoint from downloads.typesafe.com to downloads.lightbend.com |  Trivial | Spark Core | Sanket Reddy | Sanket Reddy |
| [SPARK-24654](https://issues.apache.org/jira/browse/SPARK-24654) | Update, fix LICENSE and NOTICE, and specialize for source vs binary |  Major | Build | Sean R. Owen | Sean R. Owen |
| [SPARK-20220](https://issues.apache.org/jira/browse/SPARK-20220) | Add thrift scheduling pool config in scheduling docs |  Trivial | Documentation | Miklos Christine | Miklos Christine |
| [SPARK-23451](https://issues.apache.org/jira/browse/SPARK-23451) | Deprecate KMeans computeCost |  Trivial | ML | Marco Gaido | Marco Gaido |
| [SPARK-25063](https://issues.apache.org/jira/browse/SPARK-25063) | Rename class KnowNotNull to KnownNotNull |  Trivial | SQL | Wei Xue | Wei Xue |
| [SPARK-25095](https://issues.apache.org/jira/browse/SPARK-25095) | Python support for BarrierTaskContext |  Major | PySpark | Xingbo Jiang | Xingbo Jiang |
| [SPARK-25213](https://issues.apache.org/jira/browse/SPARK-25213) | DataSourceV2 doesn't seem to produce unsafe rows |  Major | SQL | Li Jin | Li Jin |
| [SPARK-25336](https://issues.apache.org/jira/browse/SPARK-25336) | Revert SPARK-24863 and SPARK-24748 |  Major | Structured Streaming | Shixiong Zhu | Shixiong Zhu |


