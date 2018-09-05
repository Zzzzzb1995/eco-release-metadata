
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

## Release 1.4.1 - 2015-07-15

### INCOMPATIBLE CHANGES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8446](https://issues.apache.org/jira/browse/SPARK-8446) | Add helper functions for testing physical SparkPlan operators |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-7547](https://issues.apache.org/jira/browse/SPARK-7547) | Example code for ElasticNet |  Major | ML | Joseph K. Bradley | DB Tsai |
| [SPARK-7387](https://issues.apache.org/jira/browse/SPARK-7387) | CrossValidator example code in Python |  Minor | ML, PySpark | Xiangrui Meng | Ram Sriharsha |
| [SPARK-6820](https://issues.apache.org/jira/browse/SPARK-6820) | Convert NAs to null type in SparkR DataFrames |  Critical | SparkR | Shivaram Venkataraman | Qian Huang |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8787](https://issues.apache.org/jira/browse/SPARK-8787) | Change the parameter  order of @deprecated in package object sql |  Trivial | SQL | Vinod KC | Vinod KC |
| [SPARK-8776](https://issues.apache.org/jira/browse/SPARK-8776) | Increase the default MaxPermSize |  Major | Spark Core | Yin Huai | Yin Huai |
| [SPARK-8630](https://issues.apache.org/jira/browse/SPARK-8630) | Prevent from checkpointing QueueInputDStream |  Major | Streaming | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8511](https://issues.apache.org/jira/browse/SPARK-8511) | Modify ML Python tests to remove saved models |  Major | PySpark | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8475](https://issues.apache.org/jira/browse/SPARK-8475) | SparkSubmit with Ivy jars is very slow to load with no internet access |  Minor | Spark Submit | Nathan McCarthy | Burak Yavuz |
| [SPARK-8395](https://issues.apache.org/jira/browse/SPARK-8395) | spark-submit documentation is incorrect |  Minor | Documentation | Dev Lakhani | Sean Owen |
| [SPARK-8392](https://issues.apache.org/jira/browse/SPARK-8392) | RDDOperationGraph: getting cached nodes is slow |  Minor | Spark Core | meiyoula | meiyoula |
| [SPARK-8343](https://issues.apache.org/jira/browse/SPARK-8343) | Improve the Spark Streaming Guides |  Minor | Documentation, Streaming | Mike Dusenberry | Mike Dusenberry |
| [SPARK-8282](https://issues.apache.org/jira/browse/SPARK-8282) | Make number of threads used in RBackend configurable |  Major | SparkR | Hossein Falaki | Hossein Falaki |
| [SPARK-8141](https://issues.apache.org/jira/browse/SPARK-8141) | Precompute datatypes for partition columns and reuse it |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-8126](https://issues.apache.org/jira/browse/SPARK-8126) | Use temp directory under build dir for unit tests |  Minor | Build | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-8084](https://issues.apache.org/jira/browse/SPARK-8084) | SparkR install script should fail with error if any packages required are not found |  Major | Build, SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8054](https://issues.apache.org/jira/browse/SPARK-8054) | Java compatibility fixes for MLlib 1.4 |  Major | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8001](https://issues.apache.org/jira/browse/SPARK-8001) | Make AsynchronousListenerBus.waitUntilEmpty throw TimeoutException if timeout |  Minor | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-7969](https://issues.apache.org/jira/browse/SPARK-7969) | Drop method on Dataframes should handle Column |  Minor | PySpark, SQL | Olivier Girardot | Mike Dusenberry |
| [SPARK-7916](https://issues.apache.org/jira/browse/SPARK-7916) | MLlib Python doc parity check for classification and regression. |  Major | Documentation, MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-7810](https://issues.apache.org/jira/browse/SPARK-7810) | rdd.py "\_load\_from\_socket" cannot load data from jvm socket if ipv6 is used |  Major | PySpark | Ai He | Ai He |
| [SPARK-7705](https://issues.apache.org/jira/browse/SPARK-7705) | Cleanup of .sparkStaging directory fails if application is killed |  Minor | YARN | Wilfred Spiegelenburg | Weizhong |
| [SPARK-7284](https://issues.apache.org/jira/browse/SPARK-7284) | Update streaming documentation for Spark 1.4.0 release |  Critical | Documentation, Streaming | Tathagata Das | Tathagata Das |
| [SPARK-5768](https://issues.apache.org/jira/browse/SPARK-5768) | Spark UI Shows incorrect memory under Yarn |  Trivial | Web UI | Al M | Rekha Joshi |
| [SPARK-3444](https://issues.apache.org/jira/browse/SPARK-3444) | Provide a way to easily change the log level in the Spark shell while running |  Minor | Spark Shell | holdenk | Holden Karau |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-10508](https://issues.apache.org/jira/browse/SPARK-10508) | incorrect evaluation of searched case expression |  Major | SQL | N Campbell | Josh Rosen |
| [SPARK-9087](https://issues.apache.org/jira/browse/SPARK-9087) | Broken SQL on where condition involving timestamp and time string. |  Critical | SQL | Paul Wu | Michael Armbrust |
| [SPARK-9032](https://issues.apache.org/jira/browse/SPARK-9032) | scala.MatchError in DataFrameReader.json(String path) |  Major | Java API, SQL | Philipp Poetter | Josh Rosen |
| [SPARK-8909](https://issues.apache.org/jira/browse/SPARK-8909) | Nice to have all the examples in scala, java,python, R to be same in sql-programming-guide |  Trivial | Documentation | Alok Singh | Alok Singh |
| [SPARK-8903](https://issues.apache.org/jira/browse/SPARK-8903) | Fix NPE when cross tab elements contain nulls (branch 1.4) |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8902](https://issues.apache.org/jira/browse/SPARK-8902) | Hostname missing in spark-ec2 error message |  Trivial | EC2 | Daniel Darabos | Daniel Darabos |
| [SPARK-8900](https://issues.apache.org/jira/browse/SPARK-8900) | sparkPackages flag name is wrong in the documentation |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8894](https://issues.apache.org/jira/browse/SPARK-8894) | Example code errors in SparkR documentation |  Major | Documentation, SparkR | Sun Rui | Sun Rui |
| [SPARK-8868](https://issues.apache.org/jira/browse/SPARK-8868) | SqlSerializer2 can go into infinite loop when row consists only of NullType columns |  Minor | SQL | Josh Rosen | Yin Huai |
| [SPARK-8821](https://issues.apache.org/jira/browse/SPARK-8821) | The ec2 script doesn't run on python 3 with an utf8 env |  Major | EC2 | Simon Hafner | Simon Hafner |
| [SPARK-8819](https://issues.apache.org/jira/browse/SPARK-8819) | Spark doesn't compile with maven 3.3.x |  Blocker | Build | Andrew Or | Andrew Or |
| [SPARK-8804](https://issues.apache.org/jira/browse/SPARK-8804) |  order of UTF8String is wrong if there is any non-ascii character in it |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-8803](https://issues.apache.org/jira/browse/SPARK-8803) | Crosstab element's can't contain null's and back ticks |  Major | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8781](https://issues.apache.org/jira/browse/SPARK-8781) | Published POMs are no longer effective POMs |  Blocker | Build | Konstantin Shaposhnikov | Andrew Or |
| [SPARK-8754](https://issues.apache.org/jira/browse/SPARK-8754) | YarnClientSchedulerBackend doesn't stop gracefully in failure conditions |  Minor | YARN | Devaraj K | Devaraj K |
| [SPARK-8746](https://issues.apache.org/jira/browse/SPARK-8746) | Need to update download link for Hive 0.13.1 jars (HiveComparisonTest) |  Trivial | SQL | Christian Kadner | Christian Kadner |
| [SPARK-8736](https://issues.apache.org/jira/browse/SPARK-8736) | GBTRegressionModel thresholds prediction but should not |  Critical | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8720](https://issues.apache.org/jira/browse/SPARK-8720) | PR #7036 breaks branch-1.4 because of a malformed comment |  Critical | Spark Core | Cheng Lian | Andrew Or |
| [SPARK-8710](https://issues.apache.org/jira/browse/SPARK-8710) | ScalaReflection.mirror should be a def |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8687](https://issues.apache.org/jira/browse/SPARK-8687) | Spark on yarn-client mode can't send `spark.yarn.credentials.file` to executor. |  Major | YARN | SaintBacchus | SaintBacchus |
| [SPARK-8678](https://issues.apache.org/jira/browse/SPARK-8678) | Default values in Pipeline API should be immutable |  Major | ML, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8662](https://issues.apache.org/jira/browse/SPARK-8662) | [SparkR] SparkSQL tests fail in R 3.2 |  Major | R | Chris Freeman | Chris Freeman |
| [SPARK-8657](https://issues.apache.org/jira/browse/SPARK-8657) | Fail to upload conf archive to viewfs |  Minor | YARN | Tao Li | Tao Li |
| [SPARK-8637](https://issues.apache.org/jira/browse/SPARK-8637) | Packages argument is wrong in sparkR.init |  Blocker | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8628](https://issues.apache.org/jira/browse/SPARK-8628) | Race condition in AbstractSparkSQLParser.parse |  Critical | SQL | Santiago M. Mola | Vinod KC |
| [SPARK-8619](https://issues.apache.org/jira/browse/SPARK-8619) | Can't find the keytab file when recovering the streaming application. |  Major | Streaming | SaintBacchus | SaintBacchus |
| [SPARK-8607](https://issues.apache.org/jira/browse/SPARK-8607) | SparkR - Third party jars are not being added to classpath in SparkRBackend |  Critical | R | Chris Freeman | Chris Freeman |
| [SPARK-8606](https://issues.apache.org/jira/browse/SPARK-8606) | Exceptions in RDD.getPreferredLocations() and getPartitions() should not be able to crash DAGScheduler |  Critical | Scheduler | Josh Rosen | Josh Rosen |
| [SPARK-8604](https://issues.apache.org/jira/browse/SPARK-8604) | Parquet data source doesn't write summary file while doing appending |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8578](https://issues.apache.org/jira/browse/SPARK-8578) | Should ignore user defined output committer when appending data |  Major | SQL | Cheng Lian | Yin Huai |
| [SPARK-8574](https://issues.apache.org/jira/browse/SPARK-8574) | org/apache/spark/unsafe doesn't honor the java source/target versions |  Major | Build | Thomas Graves | Thomas Graves |
| [SPARK-8567](https://issues.apache.org/jira/browse/SPARK-8567) | Flaky test: o.a.s.sql.hive.HiveSparkSubmitSuite --jars |  Blocker | SQL, Tests | Yin Huai | Yin Huai |
| [SPARK-8563](https://issues.apache.org/jira/browse/SPARK-8563) | Bug that IndexedRowMatrix.computeSVD() yields the U with wrong numCols |  Major | MLlib | 19 Lee | 19 Lee |
| [SPARK-8535](https://issues.apache.org/jira/browse/SPARK-8535) | PySpark : Can't create DataFrame from Pandas dataframe with no explicit column name |  Major | PySpark | Christophe Bourguignat | Yuri Saito |
| [SPARK-8532](https://issues.apache.org/jira/browse/SPARK-8532) | In Python's DataFrameWriter, save/saveAsTable/json/parquet/jdbc always override mode |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-8525](https://issues.apache.org/jira/browse/SPARK-8525) | Bug in Streaming k-means documentation |  Minor | Documentation, MLlib | Oleksiy Dyagilev | Oleksiy Dyagilev |
| [SPARK-8506](https://issues.apache.org/jira/browse/SPARK-8506) | SparkR does not provide an easy way to depend on Spark Packages when performing init from inside of R |  Minor | SparkR | holdenk | holdenk |
| [SPARK-8489](https://issues.apache.org/jira/browse/SPARK-8489) | Add regression tests for SPARK-8470 |  Critical | SQL, Tests | Andrew Or | Andrew Or |
| [SPARK-8483](https://issues.apache.org/jira/browse/SPARK-8483) | Remove commons-lang3 depedency from flume-sink |  Major | Streaming | Hari Shreedharan | Hari Shreedharan |
| [SPARK-8468](https://issues.apache.org/jira/browse/SPARK-8468) | Cross-validation with RegressionEvaluator prefers higher RMSE |  Blocker | ML | Chelsea Zhang | Liang-Chi Hsieh |
| [SPARK-8463](https://issues.apache.org/jira/browse/SPARK-8463) | No suitable driver found for write.jdbc |  Major | SQL | Matthew Jones | Liang-Chi Hsieh |
| [SPARK-8452](https://issues.apache.org/jira/browse/SPARK-8452) | expose jobGroup API in SparkR |  Major | SparkR | Hossein Falaki | Hossein Falaki |
| [SPARK-8451](https://issues.apache.org/jira/browse/SPARK-8451) | SparkSubmitSuite never checks for process exit code |  Major | Spark Submit, Tests | Andrew Or | Andrew Or |
| [SPARK-8437](https://issues.apache.org/jira/browse/SPARK-8437) | Using directory path without wildcard for filename slow for large number of files with wholeTextFiles and binaryFiles |  Minor | Input/Output | Ewan Leith | Sean Owen |
| [SPARK-8420](https://issues.apache.org/jira/browse/SPARK-8420) | Inconsistent behavior with Dataframe Timestamp between 1.3.1 and 1.4.0 |  Blocker | SQL | Justin Yip | Michael Armbrust |
| [SPARK-8410](https://issues.apache.org/jira/browse/SPARK-8410) | Hive VersionsSuite RuntimeException |  Minor | SQL | Josiah Samuel Sathiadass | Burak Yavuz |
| [SPARK-8408](https://issues.apache.org/jira/browse/SPARK-8408) | Python OR operator is not considered while creating a column of boolean type |  Minor | PySpark | Felix Maximilian Möller | Davies Liu |
| [SPARK-8406](https://issues.apache.org/jira/browse/SPARK-8406) | Race condition when writing Parquet files |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8399](https://issues.apache.org/jira/browse/SPARK-8399) | Overlap between histograms and axis' name in Spark Streaming UI |  Minor | Streaming, Web UI | Benjamin Fradet | Benjamin Fradet |
| [SPARK-8379](https://issues.apache.org/jira/browse/SPARK-8379) | LeaseExpiredException when using dynamic partition with speculative execution |  Major | SQL | jeanlyn | jeanlyn |
| [SPARK-8376](https://issues.apache.org/jira/browse/SPARK-8376) | Commons Lang 3 is one of the required JAR of Spark Flume Sink but is missing in the docs |  Minor | Documentation | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8373](https://issues.apache.org/jira/browse/SPARK-8373) | When an RDD has no partition, Python sum will throw "Can not reduce() empty RDD" |  Minor | PySpark | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8372](https://issues.apache.org/jira/browse/SPARK-8372) | History server shows incorrect information for application not started |  Minor | Deploy, Web UI | Carson Wang | Marcelo Vanzin |
| [SPARK-8368](https://issues.apache.org/jira/browse/SPARK-8368) | ClassNotFoundException in closure for map |  Blocker | SQL | CHEN Zhiwei | Yin Huai |
| [SPARK-8367](https://issues.apache.org/jira/browse/SPARK-8367) | ReliableKafka will loss data when `spark.streaming.blockInterval` was 0 |  Major | Streaming | SaintBacchus | SaintBacchus |
| [SPARK-8358](https://issues.apache.org/jira/browse/SPARK-8358) | DataFrame explode with alias and \* fails |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8354](https://issues.apache.org/jira/browse/SPARK-8354) | Fix off-by-factor-of-8 error when allocating scratch space in UnsafeFixedWidthAggregationMap |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8339](https://issues.apache.org/jira/browse/SPARK-8339) | Itertools islice requires an integer for the stop argument. |  Minor | PySpark | Kevin Conor | Kevin Conor |
| [SPARK-8336](https://issues.apache.org/jira/browse/SPARK-8336) | Fix NullPointerException with functions.rand() |  Major | SQL | Ted Yu | Ted Yu |
| [SPARK-8329](https://issues.apache.org/jira/browse/SPARK-8329) | DataSource options parser no longer accepts '\_' |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8322](https://issues.apache.org/jira/browse/SPARK-8322) | EC2 script not fully updated for 1.4.0 release |  Major | EC2 | Mark Smith | Mark Smith |
| [SPARK-8310](https://issues.apache.org/jira/browse/SPARK-8310) | Spark EC2 branch in 1.4 is wrong |  Critical | EC2 | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8309](https://issues.apache.org/jira/browse/SPARK-8309) | OpenHashMap doesn't work with more than 12M items |  Critical | Spark Core | Vyacheslav Baranov | Vyacheslav Baranov |
| [SPARK-8306](https://issues.apache.org/jira/browse/SPARK-8306) | AddJar command needs to set the new class loader to the HiveConf inside executionHive.state. |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8289](https://issues.apache.org/jira/browse/SPARK-8289) | Provide a specific stack size with all Java implementations to prevent stack overflows with certain tests |  Major | Tests | Adam Roberts | Adam Roberts |
| [SPARK-8285](https://issues.apache.org/jira/browse/SPARK-8285) | CombineSum should be calculated as unlimited decimal first |  Trivial | SQL | Navis | Navis |
| [SPARK-8202](https://issues.apache.org/jira/browse/SPARK-8202) | PySpark: infinite loop during external sort |  Critical | PySpark | Davies Liu | Davies Liu |
| [SPARK-8200](https://issues.apache.org/jira/browse/SPARK-8200) | Exception in StreamingLinearAlgorithm on Stream with Empty RDD. |  Minor | MLlib, Streaming | Paavo Parkkinen | Paavo Parkkinen |
| [SPARK-8162](https://issues.apache.org/jira/browse/SPARK-8162) | Run spark-shell cause NullPointerException |  Blocker | Build, Spark Shell | Weizhong | Andrew Or |
| [SPARK-8161](https://issues.apache.org/jira/browse/SPARK-8161) | externalBlockStoreInitialized is never set to be true |  Major | Block Manager | shimingfei | shimingfei |
| [SPARK-8151](https://issues.apache.org/jira/browse/SPARK-8151) | Pipeline components should correctly implement copy |  Blocker | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8150](https://issues.apache.org/jira/browse/SPARK-8150) | IDFModel must implement copy |  Major | ML | Joseph K. Bradley | Xiangrui Meng |
| [SPARK-8123](https://issues.apache.org/jira/browse/SPARK-8123) | Bucketizer must implement copy |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8121](https://issues.apache.org/jira/browse/SPARK-8121) | When using with Hadoop 1.x, "spark.sql.parquet.output.committer.class" is overriden by "spark.sql.sources.outputCommitterClass" |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8116](https://issues.apache.org/jira/browse/SPARK-8116) | sc.range() doesn't match python range() |  Minor | PySpark | Ted Blackman | Ted Blackman |
| [SPARK-8112](https://issues.apache.org/jira/browse/SPARK-8112) | Received block event count through the StreamingListener can be negative |  Minor | Streaming | Tathagata Das | Shixiong Zhu |
| [SPARK-8098](https://issues.apache.org/jira/browse/SPARK-8098) | Show correct length of bytes on log page |  Minor | Web UI | Carson Wang | Carson Wang |
| [SPARK-8095](https://issues.apache.org/jira/browse/SPARK-8095) | Spark package dependencies not resolved when package is in local-ivy-cache |  Major | Spark Submit | Eron Wright | Burak Yavuz |
| [SPARK-8093](https://issues.apache.org/jira/browse/SPARK-8093) | Spark 1.4 branch's new JSON schema inference has changed the behavior of handling inner empty JSON object. |  Critical | SQL | Harish Butani | Nathan Howell |
| [SPARK-8091](https://issues.apache.org/jira/browse/SPARK-8091) | SerializationDebugger does not handle classes with writeObject method |  Major | Spark Core | Tathagata Das | Tathagata Das |
| [SPARK-8090](https://issues.apache.org/jira/browse/SPARK-8090) | SerializationDebugger does not handle classes with writeReplace correctly |  Major | Spark Core | Tathagata Das | Tathagata Das |
| [SPARK-8088](https://issues.apache.org/jira/browse/SPARK-8088) | ExecutionAllocationManager spamming INFO logs about "Lowering target number of executors" |  Major | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-8087](https://issues.apache.org/jira/browse/SPARK-8087) | PipelineModel.copy didn't copy the stages |  Blocker | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8085](https://issues.apache.org/jira/browse/SPARK-8085) | Pass in user-specified schema in read.df |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8083](https://issues.apache.org/jira/browse/SPARK-8083) | Fix return to drivers link in Mesos driver page |  Major | Mesos, Web UI | Timothy Chen | Timothy Chen |
| [SPARK-8080](https://issues.apache.org/jira/browse/SPARK-8080) | Custom Receiver.store with Iterator type do not give correct count at Spark UI |  Minor | Streaming, Web UI | Dibyendu Bhattacharya | Dibyendu Bhattacharya |
| [SPARK-8079](https://issues.apache.org/jira/browse/SPARK-8079) | NPE when HadoopFsRelation.prepareForWriteJob throws exception |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8063](https://issues.apache.org/jira/browse/SPARK-8063) | Spark master URL conflict between MASTER env variable and --master command line option |  Major | SparkR | Sun Rui | Sun Rui |
| [SPARK-8051](https://issues.apache.org/jira/browse/SPARK-8051) | StringIndexerModel (and other models) shouldn't complain if the input column is missing. |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8049](https://issues.apache.org/jira/browse/SPARK-8049) | OneVsRest's output includes a temp column |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8043](https://issues.apache.org/jira/browse/SPARK-8043) | update NaiveBayes and SVM examples in doc |  Minor | MLlib | yuhao yang | yuhao yang |
| [SPARK-8032](https://issues.apache.org/jira/browse/SPARK-8032) | Make NumPy version checking in mllib/\_\_init\_\_.py |  Major | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8004](https://issues.apache.org/jira/browse/SPARK-8004) | Spark does not enclose column names when fetchting from jdbc sources |  Major | SQL | Rene Treffer | Liang-Chi Hsieh |
| [SPARK-7989](https://issues.apache.org/jira/browse/SPARK-7989) | Fix flaky tests in ExternalShuffleServiceSuite and SparkListenerWithClusterSuite |  Critical | Spark Core, Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-7955](https://issues.apache.org/jira/browse/SPARK-7955) | Dynamic allocation: longer timeout for executors with cached blocks |  Major | Spark Core | Hari Shreedharan | Hari Shreedharan |
| [SPARK-7859](https://issues.apache.org/jira/browse/SPARK-7859) | Collect\_SET behaves different under different version of JDK |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-7820](https://issues.apache.org/jira/browse/SPARK-7820) | Java8-tests suite compile error under SBT |  Critical | Build, Streaming | Saisai Shao | Saisai Shao |
| [SPARK-7781](https://issues.apache.org/jira/browse/SPARK-7781) | GradientBoostedTrees is missing maxBins parameter in pyspark |  Major | MLlib | Don Drake | holdenk |
| [SPARK-7515](https://issues.apache.org/jira/browse/SPARK-7515) | Update documentation for PySpark on YARN with cluster mode |  Minor | Documentation | Kousuke Saruta | Kousuke Saruta |
| [SPARK-7287](https://issues.apache.org/jira/browse/SPARK-7287) | Flaky test: o.a.s.deploy.SparkSubmitSuite --packages |  Critical | Tests | Andrew Or | Yin Huai |
| [SPARK-7180](https://issues.apache.org/jira/browse/SPARK-7180) | SerializationDebugger fails with ArrayOutOfBoundsException |  Major | Spark Core | Andrew Or | Tathagata Das |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8715](https://issues.apache.org/jira/browse/SPARK-8715) | ArrayOutOfBoundsException for DataFrameStatSuite.crosstab |  Major | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8634](https://issues.apache.org/jira/browse/SPARK-8634) | Fix flaky test StreamingListenerSuite "receiver info reporting" |  Critical | Streaming, Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8541](https://issues.apache.org/jira/browse/SPARK-8541) | sumApprox and meanApprox doctests are incorrect |  Minor | PySpark | Scott Taylor | Scott Taylor |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8766](https://issues.apache.org/jira/browse/SPARK-8766) | DataFrame Python API should work with column which has non-ascii character in it |  Major | PySpark | Davies Liu | Davies Liu |
| [SPARK-8681](https://issues.apache.org/jira/browse/SPARK-8681) | crosstab column names in wrong order |  Critical | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8621](https://issues.apache.org/jira/browse/SPARK-8621) | crosstab exception when one of the value is empty |  Critical | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8568](https://issues.apache.org/jira/browse/SPARK-8568) | Prevent accidental use of "and" and "or" to build invalid expressions in Python |  Critical | SQL | Reynold Xin | Davies Liu |
| [SPARK-8548](https://issues.apache.org/jira/browse/SPARK-8548) | Remove the trailing whitespaces from the SparkR files |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8355](https://issues.apache.org/jira/browse/SPARK-8355) | Python DataFrameReader/Writer should mirror scala |  Critical | SQL | Michael Armbrust | Cheolsoo Park |
| [SPARK-8353](https://issues.apache.org/jira/browse/SPARK-8353) | Show anchor links when hovering over documentation headers |  Major | Documentation | Josh Rosen | Josh Rosen |
| [SPARK-8330](https://issues.apache.org/jira/browse/SPARK-8330) | DAG visualization: trim whitespace from input |  Major | Web UI | Andrew Or | Andrew Or |
| [SPARK-8146](https://issues.apache.org/jira/browse/SPARK-8146) | DataFrame Python API: Alias replace in DataFrameNaFunctions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8074](https://issues.apache.org/jira/browse/SPARK-8074) | Parquet should throw AnalysisException during setup for data type/name related failures |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8060](https://issues.apache.org/jira/browse/SPARK-8060) | Improve Python reader/writer interface doc and testing |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7991](https://issues.apache.org/jira/browse/SPARK-7991) | Python DataFrame: support passing a list into describe |  Major | SQL | Reynold Xin | Amey Chaugule |
| [SPARK-7980](https://issues.apache.org/jira/browse/SPARK-7980) | Support SQLContext.range(end) |  Major | SQL | Reynold Xin | Animesh Baranawal |
| [SPARK-7715](https://issues.apache.org/jira/browse/SPARK-7715) | Update MLlib Programming Guide for 1.4 |  Major | Documentation, ML, MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-7558](https://issues.apache.org/jira/browse/SPARK-7558) | Log test name when starting and finishing each test |  Major | Tests | Patrick Wendell | Andrew Or |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8769](https://issues.apache.org/jira/browse/SPARK-8769) | toLocalIterator should mention it results in many jobs |  Trivial | Documentation | holdenk | holdenk |
| [SPARK-8639](https://issues.apache.org/jira/browse/SPARK-8639) | Instructions for executing jekyll in docs/README.md could be slightly more clear, typo in docs/api.md |  Trivial | Documentation | Rosstin Murphy | Rosstin Murphy |
| [SPARK-8462](https://issues.apache.org/jira/browse/SPARK-8462) | Documentation fixes for Spark SQL |  Minor | Documentation | Lars Francke | Lars Francke |
| [SPARK-8274](https://issues.apache.org/jira/browse/SPARK-8274) | Fix wrong URLs in MLlib Frequent Pattern Mining Documentation |  Trivial | Documentation, MLlib | Favio Vázquez | Favio Vázquez |
| [SPARK-8145](https://issues.apache.org/jira/browse/SPARK-8145) | Trigger a double click on the span to show full job description |  Major | Web UI | q79969786 | q79969786 |
| [SPARK-7666](https://issues.apache.org/jira/browse/SPARK-7666) | MLlib Python doc parity check |  Major | MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-3629](https://issues.apache.org/jira/browse/SPARK-3629) | Improvements to YARN doc |  Minor | Documentation, YARN | Matei Zaharia | Neelesh Srinivas Salian |


