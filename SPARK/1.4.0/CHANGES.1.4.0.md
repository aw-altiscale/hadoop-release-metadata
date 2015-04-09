
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
# Changelog

## Release 1.4.0 - Unreleased

### INCOMPATIBLE CHANGES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-6651](https://issues.apache.org/jira/browse/SPARK-6651) | Delegate dense vector arithmetics to the underly numpy array |  Major | MLlib, PySpark | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6600](https://issues.apache.org/jira/browse/SPARK-6600) | Open ports in ec2/spark\_ec2.py to allow HDFS NFS gateway |  Minor | EC2 | Florian Verhein | Florian Verhein |
| [SPARK-6576](https://issues.apache.org/jira/browse/SPARK-6576) | DenseMatrix in PySpark should support indexing |  Minor | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-6542](https://issues.apache.org/jira/browse/SPARK-6542) | Add CreateStruct as an Expression |  Major | SQL | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6309](https://issues.apache.org/jira/browse/SPARK-6309) | Add MatrixUDT to support dense/sparse matrices in DataFrames |  Major | MLlib, SQL | Xiangrui Meng | Manoj Kumar |
| [SPARK-6268](https://issues.apache.org/jira/browse/SPARK-6268) | KMeans parameter getter methods |  Minor | MLlib | Joseph K. Bradley | yuhao yang |
| [SPARK-6186](https://issues.apache.org/jira/browse/SPARK-6186) | make tachyon version configurable in the ec2 script |  Minor | EC2 | cheng chang | cheng chang |
| [SPARK-6025](https://issues.apache.org/jira/browse/SPARK-6025) | Helper method for GradientBoostedTrees to compute validation error |  Minor | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-5955](https://issues.apache.org/jira/browse/SPARK-5955) | Add checkpointInterval to ALS |  Major | ML, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-5954](https://issues.apache.org/jira/browse/SPARK-5954) | Add topByKey to pair RDDs |  Major | Spark Core | Xiangrui Meng | Shuo Xiang |
| [SPARK-5843](https://issues.apache.org/jira/browse/SPARK-5843) | Expose all parameters in JavaPairRDD.combineByKey() |  Minor | Spark Core | Matt Cheah | Matthew Cheah |
| [SPARK-5654](https://issues.apache.org/jira/browse/SPARK-5654) | Integrate SparkR into Apache Spark |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-5566](https://issues.apache.org/jira/browse/SPARK-5566) | Tokenizer for mllib package |  Major | ML, MLlib | Joseph K. Bradley | Augustin Borsu |
| [SPARK-5495](https://issues.apache.org/jira/browse/SPARK-5495) | Offer user the ability to kill application in master web UI for standalone mode |  Major | Web UI | Saisai Shao | Saisai Shao |
| [SPARK-4985](https://issues.apache.org/jira/browse/SPARK-4985) | Parquet support for date type |  Major | SQL | Adrian Wang | Adrian Wang |
| [SPARK-4894](https://issues.apache.org/jira/browse/SPARK-4894) | Add Bernoulli-variant of Naive Bayes |  Major | MLlib | RJ Nowling | Leah McGuire |
| [SPARK-3562](https://issues.apache.org/jira/browse/SPARK-3562) | Periodic cleanup event logs |  Major | Spark Core | xukun | xukun |
| [SPARK-911](https://issues.apache.org/jira/browse/SPARK-911) | Support map pruning on sorted (K, V) RDD's |  Major | Spark Core | Patrick Wendell |  |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-6754](https://issues.apache.org/jira/browse/SPARK-6754) | TaskContextHelper is not necessary |  Minor | Spark Core | Kay Ousterhout | Kay Ousterhout |
| [SPARK-6750](https://issues.apache.org/jira/browse/SPARK-6750) | Upgrade ScalaStyle to 0.7 |  Major | Project Infra | Reynold Xin | Reynold Xin |
| [SPARK-6736](https://issues.apache.org/jira/browse/SPARK-6736) | [GraphX]Example of Graph#aggregateMessages has error |  Minor | Documentation, GraphX | Sasaki Toru |  |
| [SPARK-6733](https://issues.apache.org/jira/browse/SPARK-6733) | Suppression of usage of Scala existential code should be done |  Trivial | Scheduler | Raymond Tay | Vinod KC |
| [SPARK-6720](https://issues.apache.org/jira/browse/SPARK-6720) | PySpark MultivariateStatisticalSummary unit test for normL1 and normL2 |  Minor | MLlib, PySpark | Kai Sasaki | Kai Sasaki |
| [SPARK-6713](https://issues.apache.org/jira/browse/SPARK-6713) | Iterators in columnSimilarities to allow flatMap spill |  Major | MLlib | Reza Zadeh | Reza Zadeh |
| [SPARK-6705](https://issues.apache.org/jira/browse/SPARK-6705) | MLLIB ML Pipeline's Logistic Regression has no intercept term |  Major | ML, MLlib | Omede Firouz | Omede Firouz |
| [SPARK-6704](https://issues.apache.org/jira/browse/SPARK-6704) | integrate SparkR docs build tool into Spark doc build |  Blocker | SparkR | Davies Liu | Shivaram Venkataraman |
| [SPARK-6663](https://issues.apache.org/jira/browse/SPARK-6663) | Use Literal.create instead of constructor |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-6627](https://issues.apache.org/jira/browse/SPARK-6627) | Clean up of shuffle code and interfaces |  Critical | Shuffle, Spark Core | Patrick Wendell | Patrick Wendell |
| [SPARK-6618](https://issues.apache.org/jira/browse/SPARK-6618) | HiveMetastoreCatalog.lookupRelation should use fine-grained lock |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-6597](https://issues.apache.org/jira/browse/SPARK-6597) | Replace `input:checkbox` with `input[type="checkbox"] in additional-metrics.js |  Trivial | Web UI | Kousuke Saruta | Kousuke Saruta |
| [SPARK-6580](https://issues.apache.org/jira/browse/SPARK-6580) | Optimize LogisticRegressionModel.predictPoint |  Minor | MLlib | Joseph K. Bradley | Yanbo Liang |
| [SPARK-6569](https://issues.apache.org/jira/browse/SPARK-6569) | Kafka directInputStream logs what appear to be incorrect warnings |  Trivial | Streaming | Platon Potapov | Platon Potapov |
| [SPARK-6553](https://issues.apache.org/jira/browse/SPARK-6553) | Support for functools.partial as UserDefinedFunction |  Major | PySpark | Kalle Jepsen | Kalle Jepsen |
| [SPARK-6552](https://issues.apache.org/jira/browse/SPARK-6552) | expose start-slave.sh to user and update outdated doc |  Minor | Deploy, Documentation | Tao Wang | Tao Wang |
| [SPARK-6536](https://issues.apache.org/jira/browse/SPARK-6536) | Add IN to python Column |  Major | SQL | Michael Armbrust | Davies Liu |
| [SPARK-6515](https://issues.apache.org/jira/browse/SPARK-6515) | Use while(true) in OpenHashSet.getPos |  Minor | Spark Core | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6512](https://issues.apache.org/jira/browse/SPARK-6512) | Add contains to OpenHashMap |  Minor | Spark Core | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6510](https://issues.apache.org/jira/browse/SPARK-6510) | Add Graph#minus method to act as Set#difference |  Major | GraphX | Brennon York | Brennon York |
| [SPARK-6483](https://issues.apache.org/jira/browse/SPARK-6483) | Spark SQL udf(ScalaUdf) is very slow |  Major | SQL | Zhichao  Zhang | Zhichao  Zhang |
| [SPARK-6477](https://issues.apache.org/jira/browse/SPARK-6477) | Run MIMA tests before the Spark test suite |  Minor | Build | Brennon York | Brennon York |
| [SPARK-6475](https://issues.apache.org/jira/browse/SPARK-6475) | DataFrame should support array types when creating DFs from JavaBeans. |  Major | SQL | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6471](https://issues.apache.org/jira/browse/SPARK-6471) | Metastore schema should only be a subset of parquet schema to support dropping of columns using replace columns |  Blocker | SQL | Yash Datta | Yash Datta |
| [SPARK-6459](https://issues.apache.org/jira/browse/SPARK-6459) | Warn when Column API is constructing trivially true equality |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6453](https://issues.apache.org/jira/browse/SPARK-6453) | Some Mesos*Suite have a different package with their classes |  Trivial | Mesos | Jongyoul Lee | Jongyoul Lee |
| [SPARK-6448](https://issues.apache.org/jira/browse/SPARK-6448) | History server doesn't log exception when failing to replay log file |  Trivial | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-6433](https://issues.apache.org/jira/browse/SPARK-6433) | hive tests to import spark-sql test JAR for QueryTest access |  Minor | Build, SQL | Steve Loughran | Steve Loughran |
| [SPARK-6428](https://issues.apache.org/jira/browse/SPARK-6428) | Add to style checker "public method must have explicit type defined" |  Major | Build | Reynold Xin | Reynold Xin |
| [SPARK-6426](https://issues.apache.org/jira/browse/SPARK-6426) | User could also point the yarn cluster config directory via YARN\_CONF\_DIR |  Trivial | Documentation | Tao Wang | Tao Wang |
| [SPARK-6423](https://issues.apache.org/jira/browse/SPARK-6423) | MemoryUtils should use memoryOverhead if it's set |  Minor | Mesos | Jongyoul Lee | Jongyoul Lee |
| [SPARK-6406](https://issues.apache.org/jira/browse/SPARK-6406) | Launcher backward compatibility issues |  Minor | Deploy | Nishkam Ravi | Nishkam Ravi |
| [SPARK-6405](https://issues.apache.org/jira/browse/SPARK-6405) | Spark Kryo buffer should be forced to be max. 2GB |  Major | Spark Core | Matt Cheah | Matthew Cheah |
| [SPARK-6397](https://issues.apache.org/jira/browse/SPARK-6397) | Exclude virtual columns from QueryPlan.missingInput |  Minor | SQL | Yadong Qi | Yadong Qi |
| [SPARK-6394](https://issues.apache.org/jira/browse/SPARK-6394) | cleanup BlockManager companion object and improve the getCacheLocs method in DAGScheduler |  Minor | Spark Core | Wenchen Fan | Wenchen Fan |
| [SPARK-6374](https://issues.apache.org/jira/browse/SPARK-6374) | Add getter for GeneralizedLinearAlgorithm |  Minor | MLlib | yuhao yang | yuhao yang |
| [SPARK-6361](https://issues.apache.org/jira/browse/SPARK-6361) | Support adding a column with metadata in DataFrames |  Major | SQL | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6343](https://issues.apache.org/jira/browse/SPARK-6343) | Make doc more explicit regarding network connectivity requirements |  Minor | Documentation | Peter Parente | Peter Parente |
| [SPARK-6341](https://issues.apache.org/jira/browse/SPARK-6341) | Upgrade breeze from 0.11.1 to 0.11.2 or later |  Minor | ML, MLlib | Yu Ishikawa | Yu Ishikawa |
| [SPARK-6338](https://issues.apache.org/jira/browse/SPARK-6338) | Use standard temp dir mechanisms in tests to avoid orphaned temp files |  Minor | Tests | Sean Owen | Sean Owen |
| [SPARK-6326](https://issues.apache.org/jira/browse/SPARK-6326) | Improve castStruct to be faster |  Minor | SQL | Liang-Chi Hsieh |  |
| [SPARK-6291](https://issues.apache.org/jira/browse/SPARK-6291) | GLM toString should not output full weight vector |  Minor | MLlib | Joseph K. Bradley | Yanbo Liang |
| [SPARK-6274](https://issues.apache.org/jira/browse/SPARK-6274) | Add streaming examples showing integration with DataFrames and SQL |  Major | Examples, Streaming | Tathagata Das | Tathagata Das |
| [SPARK-6271](https://issues.apache.org/jira/browse/SPARK-6271) | Sort these tokens in alphabetic order to avoid further duplicate in HiveQl |  Minor | SQL | Zhongshuai Pei |  |
| [SPARK-6269](https://issues.apache.org/jira/browse/SPARK-6269) | Using a different implementation of java array reflection for size estimation |  Major | Spark Core | Matt Cheah | Matthew Cheah |
| [SPARK-6252](https://issues.apache.org/jira/browse/SPARK-6252) | Scala NaiveBayes should expose getLambda |  Trivial | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-6225](https://issues.apache.org/jira/browse/SPARK-6225) | Resolve most build warnings, 1.3.0 edition |  Minor | MLlib, Spark Core, SQL, Streaming | Sean Owen | Sean Owen |
| [SPARK-6219](https://issues.apache.org/jira/browse/SPARK-6219) | Expand Python lint checks to check for  compilation errors |  Minor | Build | Nicholas Chammas | Nicholas Chammas |
| [SPARK-6202](https://issues.apache.org/jira/browse/SPARK-6202) | Test framework should support variable substitution |  Minor | SQL, Tests | Adrian Wang |  |
| [SPARK-6195](https://issues.apache.org/jira/browse/SPARK-6195) | Specialized in-memory column type for fixed-precision decimal |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6193](https://issues.apache.org/jira/browse/SPARK-6193) | Speed up how spark-ec2 searches for clusters |  Minor | EC2 | Nicholas Chammas | Nicholas Chammas |
| [SPARK-6191](https://issues.apache.org/jira/browse/SPARK-6191) | Generalize spark-ec2's ability to download libraries from PyPI |  Minor | EC2 | Nicholas Chammas | Nicholas Chammas |
| [SPARK-6178](https://issues.apache.org/jira/browse/SPARK-6178) | Remove unused imports from java classes |  Trivial | Shuffle | Vinod KC | Vinod KC |
| [SPARK-6177](https://issues.apache.org/jira/browse/SPARK-6177) | Add note in LDA example to remind possible coalesce |  Trivial | Examples, MLlib | yuhao yang | yuhao yang |
| [SPARK-6153](https://issues.apache.org/jira/browse/SPARK-6153) | intellij import from maven cannot debug sparksqlclidriver |  Minor | Deploy, SQL | Adrian Wang | Adrian Wang |
| [SPARK-6146](https://issues.apache.org/jira/browse/SPARK-6146) | Support more datatype in SqlParser |  Critical | SQL | Yin Huai |  |
| [SPARK-6138](https://issues.apache.org/jira/browse/SPARK-6138) | Enhance the `toArray` method in `SizeTrackingVector` |  Minor | Spark Core | Wenchen Fan | Wenchen Fan |
| [SPARK-6124](https://issues.apache.org/jira/browse/SPARK-6124) | Support jdbc connection properties in OPTIONS part of the query |  Minor | SQL | Volodymyr Lyubinets | Volodymyr Lyubinets |
| [SPARK-6118](https://issues.apache.org/jira/browse/SPARK-6118) | making package name of deploy.worker.CommandUtils and deploy.CommandUtilsSuite consistent |  Minor | Tests | Nan Zhu | Nan Zhu |
| [SPARK-6103](https://issues.apache.org/jira/browse/SPARK-6103) | remove unused class to import in EdgeRDDImpl |  Trivial | GraphX | Lianhui Wang | Lianhui Wang |
| [SPARK-6087](https://issues.apache.org/jira/browse/SPARK-6087) | Provide actionable exception if Kryo buffer is not large enough |  Major | Spark Core | Patrick Wendell | Lev Khomich |
| [SPARK-6085](https://issues.apache.org/jira/browse/SPARK-6085) | Increase default value for memory overhead |  Minor | Spark Core | Ted Yu | Ted Yu |
| [SPARK-6079](https://issues.apache.org/jira/browse/SPARK-6079) | Use index to speed up StatusTracker.getJobIdsForGroup() |  Minor | Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-6004](https://issues.apache.org/jira/browse/SPARK-6004) | Pick the best model when training GradientBoostedTrees with validation |  Minor | MLlib | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-5983](https://issues.apache.org/jira/browse/SPARK-5983) | Don't respond to HTTP TRACE in HTTP-based UIs |  Minor | Web UI | Sean Owen | Sean Owen |
| [SPARK-5922](https://issues.apache.org/jira/browse/SPARK-5922) | Add diff(other: RDD[VertexId, VD]) in VertexRDD |  Trivial | GraphX | Takeshi Yamamuro | Brennon York |
| [SPARK-5911](https://issues.apache.org/jira/browse/SPARK-5911) | Make Column.cast(to: String) support fixed precision and scale decimal type |  Major | SQL | Yin Huai |  |
| [SPARK-5836](https://issues.apache.org/jira/browse/SPARK-5836) | Highlight in Spark documentation that by default Spark does not delete its temporary files |  Minor | Documentation | Tomasz Dudziak | Ilya Ganelin |
| [SPARK-5831](https://issues.apache.org/jira/browse/SPARK-5831) | When checkpoint file size is bigger than 10, then delete them |  Trivial | Streaming | meiyoula | meiyoula |
| [SPARK-5790](https://issues.apache.org/jira/browse/SPARK-5790) | Add tests for: VertexRDD's won't zip properly for `diff` capability |  Minor | GraphX, Tests | Brennon York | Brennon York |
| [SPARK-5750](https://issues.apache.org/jira/browse/SPARK-5750) | Document that ordering of elements in shuffled partitions is not deterministic across runs |  Minor | Documentation | Josh Rosen | Ilya Ganelin |
| [SPARK-5708](https://issues.apache.org/jira/browse/SPARK-5708) | Add Slf4jSink to Spark Metrics Sink |  Minor | Spark Core | Judy Nash | Judy Nash |
| [SPARK-5668](https://issues.apache.org/jira/browse/SPARK-5668) | spark\_ec2.py region parameter could be either mandatory or its value displayed |  Minor | EC2 | Miguel Peralvo | Miguel Peralvo |
| [SPARK-5666](https://issues.apache.org/jira/browse/SPARK-5666) | Improvements in Mqtt Spark Streaming |  Minor | Streaming | Prabeesh K | Prabeesh K |
| [SPARK-5644](https://issues.apache.org/jira/browse/SPARK-5644) | Delete tmp dir when sc is stop |  Minor | Spark Core | Weizhong | Weizhong |
| [SPARK-5641](https://issues.apache.org/jira/browse/SPARK-5641) | Allow spark\_ec2.py to copy arbitrary files to cluster |  Minor | EC2 | Florian Verhein | Florian Verhein |
| [SPARK-5628](https://issues.apache.org/jira/browse/SPARK-5628) | Add option to return spark-ec2 version |  Minor | EC2 | Nicholas Chammas | Nicholas Chammas |
| [SPARK-5611](https://issues.apache.org/jira/browse/SPARK-5611) | Allow spark-ec2 repo to be specified in CLI of spark\_ec2.py |  Minor | EC2 | Florian Verhein | Florian Verhein |
| [SPARK-5559](https://issues.apache.org/jira/browse/SPARK-5559) | Flaky test: o.a.s.streaming.flume.FlumeStreamSuite |  Major | Streaming, Tests | Kousuke Saruta | Kousuke Saruta |
| [SPARK-5522](https://issues.apache.org/jira/browse/SPARK-5522) | Accelerate the History Server start |  Major | Spark Core, Web UI | Liangliang Gu | Liangliang Gu |
| [SPARK-5436](https://issues.apache.org/jira/browse/SPARK-5436) | Validate GradientBoostedTrees during training |  Major | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-5366](https://issues.apache.org/jira/browse/SPARK-5366) | check for mode of private key file |  Minor | EC2 | liu chang | liu chang |
| [SPARK-5313](https://issues.apache.org/jira/browse/SPARK-5313) | Create simple framework for highlighting changes introduced in a PR |  Minor | Project Infra | Nicholas Chammas | Brennon York |
| [SPARK-5157](https://issues.apache.org/jira/browse/SPARK-5157) | Configure more JVM options properly when we use ConcMarkSweepGC for AM. |  Trivial | YARN | Kousuke Saruta | Kousuke Saruta |
| [SPARK-5134](https://issues.apache.org/jira/browse/SPARK-5134) | Bump default Hadoop version to 2+ |  Minor | Build | Ryan Williams | Ryan Williams |
| [SPARK-4924](https://issues.apache.org/jira/browse/SPARK-4924) | Factor out code to launch Spark applications into a separate library |  Major | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-4820](https://issues.apache.org/jira/browse/SPARK-4820) | Spark build encounters "File name too long" on some encrypted filesystems |  Minor | Documentation | Patrick Wendell | Theodore Vasiloudis |
| [SPARK-4600](https://issues.apache.org/jira/browse/SPARK-4600) | org.apache.spark.graphx.VertexRDD.diff does not work |  Minor | Documentation, GraphX | Teppei Tosa | Brennon York |
| [SPARK-4423](https://issues.apache.org/jira/browse/SPARK-4423) | Improve foreach() documentation to avoid confusion between local- and cluster-mode behavior |  Minor | Documentation | Josh Rosen | Ilya Ganelin |
| [SPARK-4346](https://issues.apache.org/jira/browse/SPARK-4346) | YarnClientSchedulerBack.asyncMonitorApplication should be common with Client.monitorApplication |  Major | Scheduler, YARN | Thomas Graves | Weizhong |
| [SPARK-4123](https://issues.apache.org/jira/browse/SPARK-4123) | Show dependency changes in pull requests |  Critical | Project Infra | Patrick Wendell | Brennon York |
| [SPARK-4011](https://issues.apache.org/jira/browse/SPARK-4011) | tighten the visibility of the members in Master/Worker class |  Minor | Spark Core | Nan Zhu | Nan Zhu |
| [SPARK-3642](https://issues.apache.org/jira/browse/SPARK-3642) | Better document the nuances of shared variables |  Minor | Documentation | Sandy Ryza | Sandy Ryza |
| [SPARK-3596](https://issues.apache.org/jira/browse/SPARK-3596) | Support changing the yarn client monitor interval |  Major | YARN | Thomas Graves | Weizhong |
| [SPARK-3591](https://issues.apache.org/jira/browse/SPARK-3591) | Provide "fire and forget" option for YARN cluster mode |  Major | YARN | Andrew Or | Tao Wang |
| [SPARK-3381](https://issues.apache.org/jira/browse/SPARK-3381) | DecisionTree: eliminate bins for unordered features |  Trivial | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-3357](https://issues.apache.org/jira/browse/SPARK-3357) | Internal log messages should be set at DEBUG level instead of INFO |  Minor | Spark Core | Xiangrui Meng | Sean Owen |
| [SPARK-3355](https://issues.apache.org/jira/browse/SPARK-3355) | Allow running maven tests in run-tests |  Major | Project Infra | Patrick Wendell | Brennon York |
| [SPARK-2149](https://issues.apache.org/jira/browse/SPARK-2149) | [MLLIB] Univariate kernel density estimation |  Major | MLlib | Sandy Ryza | Sandy Ryza |
| [SPARK-2087](https://issues.apache.org/jira/browse/SPARK-2087) | Clean Multi-user semantics for thrift JDBC/ODBC server. |  Minor | SQL | Michael Armbrust | Cheng Hao |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-6781](https://issues.apache.org/jira/browse/SPARK-6781) | sqlCtx -\> sqlContext in pyspark shell |  Critical | SQL | Michael Armbrust | Davies Liu |
| [SPARK-6767](https://issues.apache.org/jira/browse/SPARK-6767) | Documentation error in Spark SQL Readme file |  Trivial | Documentation, SQL | Tijo Thomas | Tijo Thomas |
| [SPARK-6753](https://issues.apache.org/jira/browse/SPARK-6753) | Unit test for SPARK-3426 (in ShuffleSuite) doesn't correctly clone the SparkConf |  Minor | Tests | Kay Ousterhout | Kay Ousterhout |
| [SPARK-6748](https://issues.apache.org/jira/browse/SPARK-6748) | QueryPlan.schema should be a lazy val to avoid creating excessive duplicate StructType objects |  Major | . | Cheng Lian |  |
| [SPARK-6737](https://issues.apache.org/jira/browse/SPARK-6737) | OutputCommitCoordinator.authorizedCommittersByStage map out of memory |  Critical | Scheduler, Spark Core, Streaming | Tao Li | Josh Rosen |
| [SPARK-6729](https://issues.apache.org/jira/browse/SPARK-6729) | DriverQuirks get can get OutOfBounds exception is some cases |  Minor | SQL | Volodymyr Lyubinets | Volodymyr Lyubinets |
| [SPARK-6716](https://issues.apache.org/jira/browse/SPARK-6716) | Change SparkContext.DRIVER\_IDENTIFIER from '\<driver\>' to 'driver' |  Major | Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-6696](https://issues.apache.org/jira/browse/SPARK-6696) | HiveContext.refreshTable is missing in PySpark |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6688](https://issues.apache.org/jira/browse/SPARK-6688) | EventLoggingListener should always operate on resolved URIs |  Minor | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6686](https://issues.apache.org/jira/browse/SPARK-6686) | toDF column rename does not work when columns contain '.' |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6673](https://issues.apache.org/jira/browse/SPARK-6673) | spark-shell.cmd can't start even when spark was built in Windows |  Blocker | Windows | Masayoshi TSUZUKI | Masayoshi TSUZUKI |
| [SPARK-6672](https://issues.apache.org/jira/browse/SPARK-6672) | createDataFrame from RDD[Row] with UDTs cannot be saved |  Major | MLlib, SQL | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6670](https://issues.apache.org/jira/browse/SPARK-6670) | HiveContext.analyze should throw UnsupportedOperationException instead of NotImplementedError |  Major | SQL | Yin Huai | Michael Armbrust |
| [SPARK-6669](https://issues.apache.org/jira/browse/SPARK-6669) | Lock metastore client in analyzeTable |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-6667](https://issues.apache.org/jira/browse/SPARK-6667) | hang while collect in PySpark |  Blocker | PySpark | Davies Liu | Davies Liu |
| [SPARK-6660](https://issues.apache.org/jira/browse/SPARK-6660) | MLLibPythonAPI.pythonToJava doesn't recognize object arrays |  Critical | MLlib, PySpark | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6655](https://issues.apache.org/jira/browse/SPARK-6655) | We need to read the schema of a data source table stored in spark.sql.sources.schema property |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-6650](https://issues.apache.org/jira/browse/SPARK-6650) | ExecutorAllocationManager never stops |  Major | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6647](https://issues.apache.org/jira/browse/SPARK-6647) | Make trait StringComparison as BinaryPredicate and throw error when Predicate can't translate to data source Filter |  Major | SQL | Liang-Chi Hsieh |  |
| [SPARK-6642](https://issues.apache.org/jira/browse/SPARK-6642) | Change the lambda weight to number of explicit ratings in implicit ALS |  Major | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6640](https://issues.apache.org/jira/browse/SPARK-6640) | Executor may connect to HeartbeartReceiver before it's setup in the driver side |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6636](https://issues.apache.org/jira/browse/SPARK-6636) | Use public DNS hostname everywhere in spark\_ec2.py |  Minor | EC2 | Matt Aasted | Matt Aasted |
| [SPARK-6633](https://issues.apache.org/jira/browse/SPARK-6633) | Should be "Contains" instead of "EndsWith" when constructing sources.StringContains |  Critical | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-6621](https://issues.apache.org/jira/browse/SPARK-6621) | Calling EventLoop.stop in EventLoop.onReceive and EventLoop.onError should call onStop |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6614](https://issues.apache.org/jira/browse/SPARK-6614) | OutputCommitCoordinator should clear authorized committers only after authorized committer fails, not after any failure |  Major | Scheduler | Josh Rosen | Josh Rosen |
| [SPARK-6607](https://issues.apache.org/jira/browse/SPARK-6607) | Aggregation attribute name including special chars '(' and ')' should be replaced before generating Parquet schema |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-6596](https://issues.apache.org/jira/browse/SPARK-6596) | fix the instruction on building scaladoc |  Trivial | Documentation | Nan Zhu | Nan Zhu |
| [SPARK-6592](https://issues.apache.org/jira/browse/SPARK-6592) | API of Row trait should be presented in Scala doc |  Critical | Documentation, SQL | Nan Zhu | Nan Zhu |
| [SPARK-6585](https://issues.apache.org/jira/browse/SPARK-6585) | FileServerSuite.test ("HttpFileServer should not work with SSL when the server is untrusted") failed is some evn. |  Minor | Tests | June | June |
| [SPARK-6578](https://issues.apache.org/jira/browse/SPARK-6578) | Outbound channel in network library is not thread-safe, can lead to fetch failures |  Blocker | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6575](https://issues.apache.org/jira/browse/SPARK-6575) | Converted Parquet Metastore tables no longer cache metadata |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6574](https://issues.apache.org/jira/browse/SPARK-6574) | Python Example sql.py not working in version 1.3 |  Blocker | PySpark, SQL | Davies Liu | Davies Liu |
| [SPARK-6571](https://issues.apache.org/jira/browse/SPARK-6571) | MatrixFactorizationModel created by load fails on predictAll |  Major | MLlib, PySpark | Charles Hayden | Xiangrui Meng |
| [SPARK-6560](https://issues.apache.org/jira/browse/SPARK-6560) | PairRDDFunctions suppresses exceptions in writeFile |  Minor | Spark Core | Stephen Haberman | Stephen Haberman |
| [SPARK-6558](https://issues.apache.org/jira/browse/SPARK-6558) | Utils.getCurrentUserName returns the full principal name instead of login name |  Critical | Spark Core | Thomas Graves | Thomas Graves |
| [SPARK-6556](https://issues.apache.org/jira/browse/SPARK-6556) | Fix wrong parsing logic of executorTimeoutMs and checkTimeoutIntervalMs in HeartbeatReceiver |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6555](https://issues.apache.org/jira/browse/SPARK-6555) | Override equals and hashCode in MetastoreRelation |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6550](https://issues.apache.org/jira/browse/SPARK-6550) | Add PreAnalyzer to keep logical plan consistent across DataFrame |  Major | SQL | Liang-Chi Hsieh |  |
| [SPARK-6546](https://issues.apache.org/jira/browse/SPARK-6546) | Build failure caused by PR #5029 together with #4289 |  Major | SQL | Zhongshuai Pei | Zhongshuai Pei |
| [SPARK-6544](https://issues.apache.org/jira/browse/SPARK-6544) | Problem with Avro and Kryo Serialization |  Major | Spark Core | Dean Chen |  |
| [SPARK-6538](https://issues.apache.org/jira/browse/SPARK-6538) | Add missing nullable Metastore fields when merging a Parquet schema |  Major | SQL | Adam Budde |  |
| [SPARK-6537](https://issues.apache.org/jira/browse/SPARK-6537) | UIWorkloadGenerator: The main thread should not stop SparkContext until all jobs finish |  Minor | Web UI | Kousuke Saruta | Kousuke Saruta |
| [SPARK-6532](https://issues.apache.org/jira/browse/SPARK-6532) | LDAModel.scala fails scalastyle on Windows |  Minor | Build, Windows | Brian O'Keefe | Sean Owen |
| [SPARK-6506](https://issues.apache.org/jira/browse/SPARK-6506) | python support yarn cluster mode requires SPARK\_HOME to be set |  Major | YARN | Thomas Graves | Marcelo Vanzin |
| [SPARK-6496](https://issues.apache.org/jira/browse/SPARK-6496) | Multinomial Logistic Regression failed when initialWeights is not null |  Major | MLlib | Yanbo Liang | Yanbo Liang |
| [SPARK-6492](https://issues.apache.org/jira/browse/SPARK-6492) | SparkContext.stop() can deadlock when DAGSchedulerEventProcessLoop dies |  Critical | Spark Core | Josh Rosen | Ilya Ganelin |
| [SPARK-6480](https://issues.apache.org/jira/browse/SPARK-6480) | histogram() bucket function is wrong in some simple edge cases |  Major | Spark Core | Sean Owen | Sean Owen |
| [SPARK-6473](https://issues.apache.org/jira/browse/SPARK-6473) | Launcher lib shouldn't try to figure out Scala version when not in dev mode |  Minor | Spark Submit | Marcelo Vanzin |  |
| [SPARK-6468](https://issues.apache.org/jira/browse/SPARK-6468) | Fix the race condition of subDirs in DiskBlockManager |  Minor | Block Manager | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6465](https://issues.apache.org/jira/browse/SPARK-6465) | GenericRowWithSchema: KryoException: Class cannot be created (missing no-arg constructor): |  Critical | SQL | Earthson Lu | Michael Armbrust |
| [SPARK-6463](https://issues.apache.org/jira/browse/SPARK-6463) | AttributeSet.equal should compare size |  Critical | SQL | June | June |
| [SPARK-6458](https://issues.apache.org/jira/browse/SPARK-6458) | Bad error message for invalid data sources |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6457](https://issues.apache.org/jira/browse/SPARK-6457) | Error when calling Pyspark RandomForestModel.load |  Minor | MLlib, PySpark | Joseph K. Bradley |  |
| [SPARK-6454](https://issues.apache.org/jira/browse/SPARK-6454) | Fix several broken links in PySpark docs |  Minor | Documentation, PySpark | Sean Owen | Kamil Smuga |
| [SPARK-6452](https://issues.apache.org/jira/browse/SPARK-6452) | CheckAnalysis should throw when the Aggregate node contains missing input attribute(s) |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6451](https://issues.apache.org/jira/browse/SPARK-6451) | Support CombineSum in Code Gen |  Blocker | SQL | Yin Huai | Venkata Ramana G |
| [SPARK-6450](https://issues.apache.org/jira/browse/SPARK-6450) | Metastore Parquet table conversion fails when a single metastore Parquet table appears multiple times in the query |  Blocker | SQL | Anand Mohan Tumuluri | Cheng Lian |
| [SPARK-6437](https://issues.apache.org/jira/browse/SPARK-6437) | SQL ExternalSort should use CompletionIterator to clean up temp files |  Critical | SQL | Yin Huai | Michael Armbrust |
| [SPARK-6421](https://issues.apache.org/jira/browse/SPARK-6421) | \_regression\_train\_wrapper does not test initialWeights correctly |  Major | MLlib, PySpark | Joseph K. Bradley | Kai Sasaki |
| [SPARK-6414](https://issues.apache.org/jira/browse/SPARK-6414) | Spark driver failed with NPE on job cancelation |  Critical | Scheduler | Yuri Makhno | Hung Lin |
| [SPARK-6409](https://issues.apache.org/jira/browse/SPARK-6409) | It is not necessary that avoid old inteface of hive, because this will make some UDAF can not work. |  Major | SQL | Zhongshuai Pei | Zhongshuai Pei |
| [SPARK-6408](https://issues.apache.org/jira/browse/SPARK-6408) | JDBCRDD fails on where clause with string literal |  Blocker | SQL | Pei-Lun Lee |  |
| [SPARK-6389](https://issues.apache.org/jira/browse/SPARK-6389) | YARN app diagnostics report doesn't report NPEs |  Trivial | YARN | Steve Loughran | Steve Loughran |
| [SPARK-6383](https://issues.apache.org/jira/browse/SPARK-6383) | Few examples on Dataframe operation give compiler errors |  Trivial | SQL | Tijo Thomas | Tijo Thomas |
| [SPARK-6376](https://issues.apache.org/jira/browse/SPARK-6376) | Subqueries are thrown away too early in dataframes |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6375](https://issues.apache.org/jira/browse/SPARK-6375) | Bad formatting in analysis errors |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6372](https://issues.apache.org/jira/browse/SPARK-6372) | "spark-submit --conf" is not being propagated to child processes |  Blocker | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6369](https://issues.apache.org/jira/browse/SPARK-6369) | InsertIntoHiveTable and Parquet Relation should use logic from SparkHadoopWriter |  Blocker | SQL | Michael Armbrust | Cheng Lian |
| [SPARK-6345](https://issues.apache.org/jira/browse/SPARK-6345) | Model update propagation during prediction in Streaming Regression |  Major | MLlib, Streaming | Jeremy Freeman | Jeremy Freeman |
| [SPARK-6337](https://issues.apache.org/jira/browse/SPARK-6337) | Spark 1.3 doc fixes |  Trivial | Documentation, SQL | Joseph K. Bradley | Vinod KC |
| [SPARK-6330](https://issues.apache.org/jira/browse/SPARK-6330) | newParquetRelation gets incorrect FileSystem |  Blocker | SQL | Volodymyr Lyubinets | Volodymyr Lyubinets |
| [SPARK-6329](https://issues.apache.org/jira/browse/SPARK-6329) | Minor doc changes for Mesos and TOC |  Trivial | Documentation | Brennon York | Brennon York |
| [SPARK-6327](https://issues.apache.org/jira/browse/SPARK-6327) | Run PySpark with python directly is broken |  Critical | PySpark | Davies Liu | Davies Liu |
| [SPARK-6325](https://issues.apache.org/jira/browse/SPARK-6325) | YarnAllocator crash with dynamic allocation on |  Critical | Spark Core, YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6317](https://issues.apache.org/jira/browse/SPARK-6317) | Interactive HIVE scala console is not starting |  Major | SQL | Vinod KC | Vinod KC |
| [SPARK-6315](https://issues.apache.org/jira/browse/SPARK-6315) | SparkSQL 1.3.0 (RC3) fails to read parquet file generated by 1.1.1 |  Blocker | SQL | Michael Armbrust | Cheng Lian |
| [SPARK-6313](https://issues.apache.org/jira/browse/SPARK-6313) | Fetch File Lock file creation doesnt work when Spark working dir is on a NFS mount |  Critical | Spark Core | Nathan McCarthy | Nathan McCarthy |
| [SPARK-6308](https://issues.apache.org/jira/browse/SPARK-6308) | VectorUDT is displayed as `vecto` in dtypes |  Major | MLlib, SQL | Xiangrui Meng | Manoj Kumar |
| [SPARK-6306](https://issues.apache.org/jira/browse/SPARK-6306) | Readme points to dead link |  Trivial | Documentation | Theodore Vasiloudis |  |
| [SPARK-6300](https://issues.apache.org/jira/browse/SPARK-6300) | sc.addFile(path) does not support the relative path. |  Critical | Spark Core | Zhongshuai Pei | Zhongshuai Pei |
| [SPARK-6299](https://issues.apache.org/jira/browse/SPARK-6299) | ClassNotFoundException in standalone mode when running groupByKey with class defined in REPL. |  Major | Spark Shell | Kevin (Sangwoo) Kim | Kevin (Sangwoo) Kim |
| [SPARK-6286](https://issues.apache.org/jira/browse/SPARK-6286) | Handle TASK\_ERROR in TaskState |  Minor | Spark Core | Iulian Dragos | Iulian Dragos |
| [SPARK-6285](https://issues.apache.org/jira/browse/SPARK-6285) | Duplicated code leads to errors |  Major | SQL | Iulian Dragos | Cheng Lian |
| [SPARK-6279](https://issues.apache.org/jira/browse/SPARK-6279) | Miss expressions flag "s" at logging string |  Trivial | Streaming | Zhichao  Zhang | Zhichao  Zhang |
| [SPARK-6250](https://issues.apache.org/jira/browse/SPARK-6250) | Types are now reserved words in DDL parser. |  Blocker | SQL | Michael Armbrust | Yin Huai |
| [SPARK-6245](https://issues.apache.org/jira/browse/SPARK-6245) | jsonRDD() of empty RDD results in exception |  Minor | SQL | Matthew Farrellee | Sean Owen |
| [SPARK-6243](https://issues.apache.org/jira/browse/SPARK-6243) | The Operation of match did not conside the scenarios that order.dataType does not match NativeType |  Major | SQL | Zhongshuai Pei |  |
| [SPARK-6222](https://issues.apache.org/jira/browse/SPARK-6222) | [STREAMING] All data may not be recovered from WAL when driver is killed |  Blocker | Streaming | Hari Shreedharan |  |
| [SPARK-6205](https://issues.apache.org/jira/browse/SPARK-6205) | UISeleniumSuite fails for Hadoop 2.x test with NoClassDefFoundError |  Minor | Tests | Sean Owen | Sean Owen |
| [SPARK-6197](https://issues.apache.org/jira/browse/SPARK-6197) | handle json parse exception for eventlog file not finished writing |  Minor | Web UI | Zhang, Liye | Zhang, Liye |
| [SPARK-6194](https://issues.apache.org/jira/browse/SPARK-6194) | collect() in PySpark will cause memory leak in JVM |  Critical | PySpark | Davies Liu | Davies Liu |
| [SPARK-6188](https://issues.apache.org/jira/browse/SPARK-6188) | Instance types can be mislabeled when re-starting cluster with default arguments |  Minor | EC2 | Theodore Vasiloudis | Theodore Vasiloudis |
| [SPARK-6145](https://issues.apache.org/jira/browse/SPARK-6145) | ORDER BY fails to resolve nested fields |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-6133](https://issues.apache.org/jira/browse/SPARK-6133) | SparkContext#stop is not idempotent |  Major | Spark Core | Andrew Or | Andrew Or |
| [SPARK-6132](https://issues.apache.org/jira/browse/SPARK-6132) | Context cleaner race condition across SparkContexts |  Major | Spark Core | Andrew Or | Andrew Or |
| [SPARK-6107](https://issues.apache.org/jira/browse/SPARK-6107) | event log file ends with .inprogress should be able to display on webUI for standalone mode |  Major | Web UI | Zhang, Liye | Zhang, Liye |
| [SPARK-6088](https://issues.apache.org/jira/browse/SPARK-6088) | UI is malformed when tasks fetch remote results |  Major | Web UI | Kay Ousterhout | Kay Ousterhout |
| [SPARK-6077](https://issues.apache.org/jira/browse/SPARK-6077) | Multiple spark streaming tabs on UI when reuse the same sparkcontext |  Minor | Streaming, Web UI | zhichao-li |  |
| [SPARK-6075](https://issues.apache.org/jira/browse/SPARK-6075) | After SPARK-3885, some tasks' accumulator updates may be lost |  Blocker | Spark Core, Tests | Josh Rosen | Josh Rosen |
| [SPARK-6063](https://issues.apache.org/jira/browse/SPARK-6063) | MLlib doesn't pass mvn scalastyle check due to UTF chars in LDAModel.scala |  Minor | Build, Windows | Michael Griffiths | Michael Griffiths |
| [SPARK-6059](https://issues.apache.org/jira/browse/SPARK-6059) | Add volatile to ApplicationMaster.reporterThread and ApplicationMaster.allocator |  Minor | YARN | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6054](https://issues.apache.org/jira/browse/SPARK-6054) | SQL UDF returning object of case class; regression from 1.2.0 |  Blocker | SQL | Spiro Michaylov | Michael Armbrust |
| [SPARK-6045](https://issues.apache.org/jira/browse/SPARK-6045) | RecordWriter should be checked against null in PairRDDFunctions#saveAsNewAPIHadoopDataset |  Trivial | Input/Output | Ted Yu | Ted Yu |
| [SPARK-6044](https://issues.apache.org/jira/browse/SPARK-6044) | RDD.aggregate() should not use the closure serializer on the zero value |  Major | Spark Core | Matt Cheah | Sean Owen |
| [SPARK-6036](https://issues.apache.org/jira/browse/SPARK-6036) | EventLog process logic has race condition with Akka actor system |  Major | Spark Core, Web UI | Zhang, Liye | Zhang, Liye |
| [SPARK-5970](https://issues.apache.org/jira/browse/SPARK-5970) | Temporary directories are not removed (but their content is) |  Minor | Spark Core | Milan Straka | Milan Straka |
| [SPARK-5949](https://issues.apache.org/jira/browse/SPARK-5949) | Driver program has to register roaring bitmap classes used by spark with Kryo when number of partitions is greater than 2000 |  Major | Spark Core | Peter Torok | Imran Rashid |
| [SPARK-5914](https://issues.apache.org/jira/browse/SPARK-5914) | Enable spark-submit to run requiring only user permission on windows |  Minor | Spark Submit, Windows | Judy Nash | Judy Nash |
| [SPARK-5908](https://issues.apache.org/jira/browse/SPARK-5908) | Hive udtf with single alias should be resolved correctly |  Major | SQL | Liang-Chi Hsieh |  |
| [SPARK-5860](https://issues.apache.org/jira/browse/SPARK-5860) | JdbcRDD: overflow on large range with high number of partitions |  Minor | Spark Core | Jeroen Warmerdam | Jeroen Warmerdam |
| [SPARK-5845](https://issues.apache.org/jira/browse/SPARK-5845) | Time to cleanup spilled shuffle files not included in shuffle write time |  Minor | Shuffle | Kay Ousterhout | Ilya Ganelin |
| [SPARK-5821](https://issues.apache.org/jira/browse/SPARK-5821) | JSONRelation and ParquetRelation2 should check if delete is successful for the overwrite operation. |  Major | SQL | Yanbo Liang | Yanbo Liang |
| [SPARK-5815](https://issues.apache.org/jira/browse/SPARK-5815) | Deprecate SVDPlusPlus APIs that expose DoubleMatrix from JBLAS |  Major | GraphX | Xiangrui Meng | Sean Owen |
| [SPARK-5801](https://issues.apache.org/jira/browse/SPARK-5801) | Shuffle creates too many nested directories |  Minor | Shuffle, Spark Core | Kay Ousterhout | Marcelo Vanzin |
| [SPARK-5776](https://issues.apache.org/jira/browse/SPARK-5776) | JIRA version not of form x.y.z breaks merge\_spark\_pr.py |  Minor | Project Infra | Sean Owen | Sean Owen |
| [SPARK-5771](https://issues.apache.org/jira/browse/SPARK-5771) | Number of Cores in Completed Applications of Standalone Master Web Page always be 0 if sc.stop() is called |  Minor | Web UI | Liangliang Gu | Liangliang Gu |
| [SPARK-5744](https://issues.apache.org/jira/browse/SPARK-5744) | RDD.isEmpty / take fails for (empty) RDD of Nothing |  Minor | Spark Core | Tobias Bertelsen | Sean Owen |
| [SPARK-5724](https://issues.apache.org/jira/browse/SPARK-5724) | misconfiguration in Akka system |  Minor | Spark Core | Nan Zhu | Nan Zhu |
| [SPARK-5712](https://issues.apache.org/jira/browse/SPARK-5712) | Semicolon at end of a comment line |  Minor | SQL | Adrian Wang |  |
| [SPARK-5680](https://issues.apache.org/jira/browse/SPARK-5680) | Sum function on all null values, should return zero |  Minor | SQL | Venkata Ramana G |  |
| [SPARK-5656](https://issues.apache.org/jira/browse/SPARK-5656) | NegativeArraySizeException in EigenValueDecomposition.symmetricEigs for large n and/or large k |  Minor | MLlib | Mark Bittmann | Mark Bittmann |
| [SPARK-5651](https://issues.apache.org/jira/browse/SPARK-5651) | Support 'create db.table' in HiveContext |  Major | SQL | Yadong Qi |  |
| [SPARK-5529](https://issues.apache.org/jira/browse/SPARK-5529) | BlockManager heartbeat expiration does not kill executor |  Major | Spark Core, YARN | Hong Shen | Hong Shen |
| [SPARK-5498](https://issues.apache.org/jira/browse/SPARK-5498) | [SPARK-SQL]when the partition schema does not match table schema,it throws java.lang.ClassCastException and so on |  Major | SQL | jeanlyn |  |
| [SPARK-5470](https://issues.apache.org/jira/browse/SPARK-5470) | use defaultClassLoader of Serializer to load classes of classesToRegister in KryoSerializer |  Major | Spark Core | Lianhui Wang | Lianhui Wang |
| [SPARK-5416](https://issues.apache.org/jira/browse/SPARK-5416) | Initialize Executor.threadPool before ExecutorSource |  Minor | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-5408](https://issues.apache.org/jira/browse/SPARK-5408) | MaxPermSize is ignored by ExecutorRunner and DriverRunner |  Minor | Spark Core | Jacek Lewandowski | Jacek Lewandowski |
| [SPARK-5404](https://issues.apache.org/jira/browse/SPARK-5404) | Statistic of Logical Plan is too aggresive |  Major | SQL | Cheng Hao |  |
| [SPARK-5380](https://issues.apache.org/jira/browse/SPARK-5380) | There will be an ArrayIndexOutOfBoundsException if the format of the source file is wrong |  Minor | GraphX | Leo\_lh | Leo\_lh |
| [SPARK-5371](https://issues.apache.org/jira/browse/SPARK-5371) | Failure to analyze query with UNION ALL and double aggregation |  Critical | SQL | David Ross | Michael Armbrust |
| [SPARK-5363](https://issues.apache.org/jira/browse/SPARK-5363) | Spark 1.2 freeze without error notification |  Blocker | PySpark | Tassilo Klein | Davies Liu |
| [SPARK-5320](https://issues.apache.org/jira/browse/SPARK-5320) | Joins on simple table created using select gives error |  Major | SQL | Kuldeep | Yuri Saito |
| [SPARK-5242](https://issues.apache.org/jira/browse/SPARK-5242) | "ec2/spark\_ec2.py lauch" does not work with VPC if no public DNS or IP is available |  Major | EC2 | Vladimir Grigor | Michelangelo D'Agostino |
| [SPARK-5203](https://issues.apache.org/jira/browse/SPARK-5203) | union with different decimal type report error |  Major | SQL | guowei |  |
| [SPARK-4949](https://issues.apache.org/jira/browse/SPARK-4949) | shutdownCallback in SparkDeploySchedulerBackend should be enclosed by synchronized block. |  Minor | Scheduler | Kousuke Saruta | Kousuke Saruta |
| [SPARK-4777](https://issues.apache.org/jira/browse/SPARK-4777) | Some block memory after unrollSafely not count into used memory(memoryStore.entrys or unrollMemory) |  Major | Spark Core | SuYan | SuYan |
| [SPARK-4704](https://issues.apache.org/jira/browse/SPARK-4704) | SparkSubmitDriverBootstrap doesn't flush output |  Major | Spark Core | Stephen Haberman | Sean Owen |
| [SPARK-4687](https://issues.apache.org/jira/browse/SPARK-4687) | SparkContext#addFile doesn't keep file folder information |  Major | Spark Core | Jimmy Xiang | Sandy Ryza |
| [SPARK-4300](https://issues.apache.org/jira/browse/SPARK-4300) | Race condition during SparkWorker shutdown |  Minor | Spark Shell | Alex Liu | Sean Owen |
| [SPARK-4012](https://issues.apache.org/jira/browse/SPARK-4012) | Uncaught OOM in ContextCleaner |  Major | Spark Core | Nan Zhu | Nan Zhu |
| [SPARK-3885](https://issues.apache.org/jira/browse/SPARK-3885) | Provide mechanism to remove accumulators once they are no longer used |  Major | Spark Core | Josh Rosen | Ilya Ganelin |
| [SPARK-3884](https://issues.apache.org/jira/browse/SPARK-3884) | If deploy mode is cluster, --driver-memory shouldn't apply to client JVM |  Major | Spark Submit | Sandy Ryza | Marcelo Vanzin |
| [SPARK-3570](https://issues.apache.org/jira/browse/SPARK-3570) | Shuffle write time does not include time to open shuffle files |  Major | Spark Core | Kay Ousterhout | Kay Ousterhout |
| [SPARK-3266](https://issues.apache.org/jira/browse/SPARK-3266) | JavaDoubleRDD doesn't contain max() |  Major | Java API | Amey Chaugule | Sean Owen |
| [SPARK-1965](https://issues.apache.org/jira/browse/SPARK-1965) | Spark UI throws NPE on trying to load the app page for non-existent app |  Minor | Web UI | Kay Ousterhout | Sean Owen |
| [SPARK-1805](https://issues.apache.org/jira/browse/SPARK-1805) | Error launching cluster when master and slave machines are of different virtualization types |  Minor | EC2 | Han JU | Nicholas Chammas |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-6625](https://issues.apache.org/jira/browse/SPARK-6625) | Add common string filters to data sources |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6623](https://issues.apache.org/jira/browse/SPARK-6623) | Alias DataFrame.na.fill/drop in Python |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6608](https://issues.apache.org/jira/browse/SPARK-6608) | Make DataFrame.rdd a lazy val |  Minor | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6603](https://issues.apache.org/jira/browse/SPARK-6603) | SQLContext.registerFunction -\> SQLContext.udf.register |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-6564](https://issues.apache.org/jira/browse/SPARK-6564) | SQLContext.emptyDataFrame should contain 0 rows, not 1 row |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6563](https://issues.apache.org/jira/browse/SPARK-6563) | DataFrame.fillna |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6554](https://issues.apache.org/jira/browse/SPARK-6554) | Cannot use partition columns in where clause when Parquet filter push-down is enabled |  Critical | SQL | Jon Chase | Cheng Lian |
| [SPARK-6526](https://issues.apache.org/jira/browse/SPARK-6526) | Add Normalizer transformer |  Major | ML | Xusen Yin | Xusen Yin |
| [SPARK-6262](https://issues.apache.org/jira/browse/SPARK-6262) | Python MLlib API missing items: Statistics |  Major | MLlib, PySpark | Joseph K. Bradley | Kai Sasaki |
| [SPARK-6256](https://issues.apache.org/jira/browse/SPARK-6256) | Python MLlib API missing items: Regression |  Major | MLlib, PySpark | Joseph K. Bradley | Yanbo Liang |
| [SPARK-6255](https://issues.apache.org/jira/browse/SPARK-6255) | Python MLlib API missing items: Classification |  Major | MLlib, PySpark | Joseph K. Bradley | Yanbo Liang |
| [SPARK-6228](https://issues.apache.org/jira/browse/SPARK-6228) | Move SASL support into network/common module |  Minor | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-6226](https://issues.apache.org/jira/browse/SPARK-6226) | Support model save/load in Python's KMeans |  Major | MLlib, PySpark | Joseph K. Bradley | Xusen Yin |
| [SPARK-6119](https://issues.apache.org/jira/browse/SPARK-6119) | DataFrame.dropna support |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6117](https://issues.apache.org/jira/browse/SPARK-6117) | describe function for summary statistics |  Major | SQL | Reynold Xin |  |
| [SPARK-6096](https://issues.apache.org/jira/browse/SPARK-6096) | Support model save/load in Python's naive Bayes |  Major | MLlib, PySpark | Xiangrui Meng | Xusen Yin |
| [SPARK-6095](https://issues.apache.org/jira/browse/SPARK-6095) | Support model save/load in Python's linear models |  Major | MLlib, PySpark | Xiangrui Meng | Yanbo Liang |
| [SPARK-6090](https://issues.apache.org/jira/browse/SPARK-6090) | Add BinaryClassificationMetrics in PySpark/MLlib |  Major | MLlib, PySpark | Xiangrui Meng | Xiangrui Meng |
| [SPARK-5987](https://issues.apache.org/jira/browse/SPARK-5987) | Model import/export for GaussianMixtureModel |  Major | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-5986](https://issues.apache.org/jira/browse/SPARK-5986) | Model import/export for KMeansModel |  Major | MLlib | Joseph K. Bradley | Xusen Yin |
| [SPARK-5692](https://issues.apache.org/jira/browse/SPARK-5692) | Model import/export for Word2Vec |  Major | MLlib | Xiangrui Meng | Manoj Kumar |
| [SPARK-5124](https://issues.apache.org/jira/browse/SPARK-5124) | Standardize internal RPC interface |  Major | Spark Core | Reynold Xin | Shixiong Zhu |
| [SPARK-4655](https://issues.apache.org/jira/browse/SPARK-4655) | Split Stage into ShuffleMapStage and ResultStage subclasses |  Major | Spark Core | Josh Rosen | Ilya Ganelin |
| [SPARK-4588](https://issues.apache.org/jira/browse/SPARK-4588) | Add API for feature attributes |  Critical | ML, MLlib | Xiangrui Meng | Sean Owen |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-6626](https://issues.apache.org/jira/browse/SPARK-6626) | TwitterUtils.createStream documentation error |  Trivial | Documentation | Jayson Sunshine | Jayson Sunshine |
| [SPARK-6469](https://issues.apache.org/jira/browse/SPARK-6469) | Improving documentation on YARN local directories usage |  Minor | Documentation, YARN | Christophe Préaud | Christophe Préaud |
| [SPARK-6455](https://issues.apache.org/jira/browse/SPARK-6455) | Correct some mistakes and typos |  Trivial | GraphX | Hangchen Yu | Hangchen Yu |
| [SPARK-6402](https://issues.apache.org/jira/browse/SPARK-6402) | EC2 script and job scheduling documentation still refer to Shark |  Trivial | Documentation, EC2 | Pierre Borckmans | Pierre Borckmans |
| [SPARK-6370](https://issues.apache.org/jira/browse/SPARK-6370) | Improve documentation of RDD.sample() fraction's effect |  Minor | Spark Core | Marko Bonaci | Marko Bonaci |
| [SPARK-6336](https://issues.apache.org/jira/browse/SPARK-6336) | LBFGS should document what convergenceTol means |  Trivial | Documentation, MLlib | Joseph K. Bradley | Kai Sasaki |
| [SPARK-6278](https://issues.apache.org/jira/browse/SPARK-6278) | Mention the change of step size in the migration guide |  Major | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6275](https://issues.apache.org/jira/browse/SPARK-6275) | Miss toDF() function in docs/sql-programming-guide.md |  Trivial | Documentation | Zhichao  Zhang | Zhichao  Zhang |
| [SPARK-5814](https://issues.apache.org/jira/browse/SPARK-5814) | Remove JBLAS from runtime dependencies |  Major | GraphX, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-6615](https://issues.apache.org/jira/browse/SPARK-6615) | Add missing methods to Word2Vec's Python API |  Minor | MLlib, PySpark | Kai Sasaki | Kai Sasaki |
| [SPARK-6598](https://issues.apache.org/jira/browse/SPARK-6598) | Python API for IDFModel |  Minor | MLlib | Kai Sasaki | Kai Sasaki |
| [SPARK-6371](https://issues.apache.org/jira/browse/SPARK-6371) | Update version to 1.4.0-SNAPSHOT |  Critical | Build | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-5909](https://issues.apache.org/jira/browse/SPARK-5909) | Add a clearCache command to Spark SQL's cache manager |  Major | SQL | Yin Huai |  |
| [SPARK-5727](https://issues.apache.org/jira/browse/SPARK-5727) | Deprecate, remove Debian packaging |  Minor | Build, Deploy | Sean Owen | Sean Owen |

