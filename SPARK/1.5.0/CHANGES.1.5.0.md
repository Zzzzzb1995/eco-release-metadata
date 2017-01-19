
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

## Release 1.5.0 - 2015-09-09



### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-10578](https://issues.apache.org/jira/browse/SPARK-10578) | pyspark.ml.classification.RandomForestClassifer does not return \`rawPrediction\` column |  Major | ML | Karen Yin-Yee Ng | Joseph K. Bradley |
| [SPARK-6936](https://issues.apache.org/jira/browse/SPARK-6936) | SQLContext.sql() caused deadlock in multi-thread env |  Major | SQL | Paul Wu | Michael Armbrust |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-7387](https://issues.apache.org/jira/browse/SPARK-7387) | CrossValidator example code in Python |  Minor | ML, PySpark | Xiangrui Meng | Ram Sriharsha |
| [SPARK-7547](https://issues.apache.org/jira/browse/SPARK-7547) | Example code for ElasticNet |  Major | ML | Joseph K. Bradley | DB Tsai |
| [SPARK-7440](https://issues.apache.org/jira/browse/SPARK-7440) | Remove physical Distinct operator in favor of Aggregate |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6964](https://issues.apache.org/jira/browse/SPARK-6964) | Support Cancellation in the Thrift Server |  Critical | SQL | Michael Armbrust | Dong Wang |
| [SPARK-7639](https://issues.apache.org/jira/browse/SPARK-7639) | Add Python API for Statistics.kernelDensity |  Major | MLlib, PySpark | Yanbo Liang | Manoj Kumar |
| [SPARK-6820](https://issues.apache.org/jira/browse/SPARK-6820) | Convert NAs to null type in SparkR DataFrames |  Critical | SparkR | Shivaram Venkataraman | Qian Huang |
| [SPARK-8129](https://issues.apache.org/jira/browse/SPARK-8129) | Securely pass auth secrets to executors in standalone cluster mode |  Minor | Deploy, Spark Core | Kan Zhang | Kan Zhang |
| [SPARK-6390](https://issues.apache.org/jira/browse/SPARK-6390) | Add MatrixUDT in PySpark |  Major | MLlib, PySpark | Xiangrui Meng | Manoj Kumar |
| [SPARK-7605](https://issues.apache.org/jira/browse/SPARK-7605) | Python API for ElementwiseProduct |  Major | MLlib, PySpark | Yanbo Liang | Manoj Kumar |
| [SPARK-8446](https://issues.apache.org/jira/browse/SPARK-8446) | Add helper functions for testing physical SparkPlan operators |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8348](https://issues.apache.org/jira/browse/SPARK-8348) | Add in operator to DataFrame Column |  Major | SparkR, SQL | Xiangrui Meng | Yu Ishikawa |
| [SPARK-7604](https://issues.apache.org/jira/browse/SPARK-7604) | Python API for PCA and PCAModel |  Major | MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8431](https://issues.apache.org/jira/browse/SPARK-8431) | Add in operator to DataFrame Column in SparkR |  Major | SparkR, SQL | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8344](https://issues.apache.org/jira/browse/SPARK-8344) | Add internal metrics / logging for DAGScheduler to detect long pauses / blocking |  Major | Scheduler, Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-8302](https://issues.apache.org/jira/browse/SPARK-8302) | Support heterogeneous cluster nodes on YARN |  Major | YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-5962](https://issues.apache.org/jira/browse/SPARK-5962) | [MLLIB] Python support for Power Iteration Clustering |  Major | MLlib | Stephen Boesch | Yanbo Liang |
| [SPARK-8579](https://issues.apache.org/jira/browse/SPARK-8579) | Support arbitrary object in UnsafeRow |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8019](https://issues.apache.org/jira/browse/SPARK-8019) | [SparkR] Create worker R processes with a command other then Rscript |  Major | SparkR | Michael Sannella | Michael Sannella |
| [SPARK-8456](https://issues.apache.org/jira/browse/SPARK-8456) | Python API for N-Gram Feature Transformer |  Trivial | ML | Feynman Liang | Feynman Liang |
| [SPARK-8551](https://issues.apache.org/jira/browse/SPARK-8551) | Python example code for elastic net |  Minor | PySpark | Shuo Xiang | Shuo Xiang |
| [SPARK-7988](https://issues.apache.org/jira/browse/SPARK-7988) | Mechanism to control receiver scheduling |  Critical | DStreams | Nishkam Ravi | Nishkam Ravi |
| [SPARK-6833](https://issues.apache.org/jira/browse/SPARK-6833) | Extend \`addPackage\` so that any given R file can be sourced in the worker before functions are run. |  Minor | SparkR | Shivaram Venkataraman | Sun Rui |
| [SPARK-8479](https://issues.apache.org/jira/browse/SPARK-8479) | Add numNonzeros and numActives to linalg.Matrices |  Minor | MLlib | Manoj Kumar | Manoj Kumar |
| [SPARK-8782](https://issues.apache.org/jira/browse/SPARK-8782) | GenerateOrdering fails for NullType (i.e. ORDER BY NULL crashes) |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8777](https://issues.apache.org/jira/browse/SPARK-8777) | Add random data generation test utilities to Spark SQL |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8124](https://issues.apache.org/jira/browse/SPARK-8124) | Created more examples on SparkR DataFrames |  Minor | Examples, SparkR | Daniel Emaasit | Daniel Emaasit |
| [SPARK-8711](https://issues.apache.org/jira/browse/SPARK-8711) | Add additional methods to JavaModel wrappers in trees |  Major | ML, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8704](https://issues.apache.org/jira/browse/SPARK-8704) | Add missing methods in StandardScaler (ML and PySpark) |  Major | ML, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8538](https://issues.apache.org/jira/browse/SPARK-8538) | LinearRegressionResults class for storing LR results on data |  Major | ML | Joseph K. Bradley | Feynman Liang |
| [SPARK-8539](https://issues.apache.org/jira/browse/SPARK-8539) | LinearRegressionSummary class for storing LR training stats |  Major | ML | Joseph K. Bradley | Feynman Liang |
| [SPARK-8598](https://issues.apache.org/jira/browse/SPARK-8598) | Implementation of 1-sample, two-sided, Kolmogorov Smirnov Test for RDDs |  Minor | MLlib | Jose Cambronero | Jose Cambronero |
| [SPARK-6487](https://issues.apache.org/jira/browse/SPARK-6487) | Add sequential pattern mining algorithm PrefixSpan to Spark MLlib |  Critical | MLlib | Zhang JiaJin | Zhang JiaJin |
| [SPARK-8706](https://issues.apache.org/jira/browse/SPARK-8706) | Implement Pylint / Prospector checks for PySpark |  Major | Project Infra, PySpark | Josh Rosen | Manoj Kumar |
| [SPARK-8774](https://issues.apache.org/jira/browse/SPARK-8774) | Add R model formula with basic support as a transformer |  Critical | ML, SparkR | Xiangrui Meng | Eric Liang |
| [SPARK-8807](https://issues.apache.org/jira/browse/SPARK-8807) | Add between operator in SparkR |  Major | SparkR | Yu Ishikawa | Liang-Chi Hsieh |
| [SPARK-9022](https://issues.apache.org/jira/browse/SPARK-9022) | UnsafeProject |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8600](https://issues.apache.org/jira/browse/SPARK-8600) | Naive Bayes API for spark.ml Pipelines |  Major | ML | Xiangrui Meng | Yanbo Liang |
| [SPARK-7879](https://issues.apache.org/jira/browse/SPARK-7879) | KMeans API for spark.ml Pipelines |  Critical | ML | Joseph K. Bradley | Yu Ishikawa |
| [SPARK-9143](https://issues.apache.org/jira/browse/SPARK-9143) | Add planner rule for automatically inserting Unsafe \<-\> Safe row format converters |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9115](https://issues.apache.org/jira/browse/SPARK-9115) | date/time function: dayInYear |  Major | SQL | Tarek Auel | Tarek Auel |
| [SPARK-9023](https://issues.apache.org/jira/browse/SPARK-9023) | UnsafeExchange |  Major | SQL | Reynold Xin | Josh Rosen |
| [SPARK-7422](https://issues.apache.org/jira/browse/SPARK-7422) | Add argmax to Vector, SparseVector |  Minor | MLlib | Joseph K. Bradley | George Dittmar |
| [SPARK-8996](https://issues.apache.org/jira/browse/SPARK-8996) | Add Python API for Kolmogorov-Smirnov Test |  Major | MLlib, PySpark | Xiangrui Meng | Manoj Kumar |
| [SPARK-9178](https://issues.apache.org/jira/browse/SPARK-9178) | UTF8String empty string method |  Trivial | SQL | Tarek Auel | Tarek Auel |
| [SPARK-9201](https://issues.apache.org/jira/browse/SPARK-9201) | Integrate MLlib with SparkR using RFormula |  Major | ML, SparkR | Eric Liang | Eric Liang |
| [SPARK-9024](https://issues.apache.org/jira/browse/SPARK-9024) | Unsafe HashJoin |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8484](https://issues.apache.org/jira/browse/SPARK-8484) | Add TrainValidationSplit to ml.tuning |  Critical | ML | Xiangrui Meng | Martin Zapletal |
| [SPARK-8364](https://issues.apache.org/jira/browse/SPARK-8364) | Add crosstab to SparkR DataFrames |  Major | SparkR | Xiangrui Meng | Xiangrui Meng |
| [SPARK-7254](https://issues.apache.org/jira/browse/SPARK-7254) | Extend PIC to handle Graphs directly |  Major | GraphX, MLlib | Joseph K. Bradley | Liang-Chi Hsieh |
| [SPARK-8867](https://issues.apache.org/jira/browse/SPARK-8867) | Show the UDF usage for user. |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-4176](https://issues.apache.org/jira/browse/SPARK-4176) | Support decimals with precision \> 18 in Parquet |  Major | SQL | Matei Zaharia | Rene Treffer |
| [SPARK-9230](https://issues.apache.org/jira/browse/SPARK-9230) | SparkR RFormula should support StringType features |  Major | ML, SparkR | Eric Liang | Eric Liang |
| [SPARK-8882](https://issues.apache.org/jira/browse/SPARK-8882) | A New Receiver Scheduling Mechanism to solve unbalanced receivers |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9391](https://issues.apache.org/jira/browse/SPARK-9391) | Support minus, dot, and intercept operators in SparkR RFormula |  Major | ML, SparkR | Eric Liang | Eric Liang |
| [SPARK-6129](https://issues.apache.org/jira/browse/SPARK-6129) | Create MLlib metrics user guide with algorithm definitions and complete code examples. |  Major | Documentation, MLlib | Xiangrui Meng | Seth Hendrickson |
| [SPARK-9440](https://issues.apache.org/jira/browse/SPARK-9440) | LocalLDAModel should save docConcentration, topicConcentration, and gammaShape |  Critical | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-7368](https://issues.apache.org/jira/browse/SPARK-7368) | add QR decomposition for RowMatrix |  Major | MLlib | yuhao yang | yuhao yang |
| [SPARK-8671](https://issues.apache.org/jira/browse/SPARK-8671) | Add isotonic regression to the pipeline API |  Major | ML | Xiangrui Meng | Martin Zapletal |
| [SPARK-7690](https://issues.apache.org/jira/browse/SPARK-7690) | MulticlassClassificationEvaluator for tuning Multiclass Classifiers |  Major | ML | Ram Sriharsha | Ram Sriharsha |
| [SPARK-9471](https://issues.apache.org/jira/browse/SPARK-9471) | Multilayer perceptron classifier |  Major | ML | Alexander Ulanov | Alexander Ulanov |
| [SPARK-9231](https://issues.apache.org/jira/browse/SPARK-9231) | DistributedLDAModel method for top topics per document |  Minor | MLlib | Joseph K. Bradley | yuhao yang |
| [SPARK-8564](https://issues.apache.org/jira/browse/SPARK-8564) | Add the Python API for Kinesis |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9246](https://issues.apache.org/jira/browse/SPARK-9246) | DistributedLDAModel predict top docs per topic |  Major | MLlib | Joseph K. Bradley | Meihua Wu |
| [SPARK-8936](https://issues.apache.org/jira/browse/SPARK-8936) | Hyperparameter estimation in LDA |  Major | ML | Feynman Liang | Feynman Liang |
| [SPARK-9464](https://issues.apache.org/jira/browse/SPARK-9464) | Add property-based tests for UTF8String |  Critical | SQL | Josh Rosen | Yijie Shen |
| [SPARK-8169](https://issues.apache.org/jira/browse/SPARK-8169) | Add StopWordsRemover as a transformer |  Major | ML | Xiangrui Meng | yuhao yang |
| [SPARK-4751](https://issues.apache.org/jira/browse/SPARK-4751) | Support dynamic allocation for standalone mode |  Critical | Spark Core | Andrew Or | Andrew Or |
| [SPARK-1855](https://issues.apache.org/jira/browse/SPARK-1855) | Provide memory-and-local-disk RDD checkpointing |  Major | MLlib, Spark Core | Xiangrui Meng | Andrew Or |
| [SPARK-5133](https://issues.apache.org/jira/browse/SPARK-5133) | Feature Importance for Random Forests |  Major | ML, MLlib | Peter Prettenhofer | Joseph K. Bradley |
| [SPARK-9544](https://issues.apache.org/jira/browse/SPARK-9544) | RFormula in Python |  Major | ML, PySpark | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8874](https://issues.apache.org/jira/browse/SPARK-8874) | Add missing methods in Word2Vec ML |  Major | ML | Manoj Kumar | Manoj Kumar |
| [SPARK-9263](https://issues.apache.org/jira/browse/SPARK-9263) | Add Spark Submit flag to exclude dependencies when using --packages |  Major | Spark Submit | Burak Yavuz | Burak Yavuz |
| [SPARK-8313](https://issues.apache.org/jira/browse/SPARK-8313) | Support Spark Packages containing R code with --packages |  Major | Spark Submit, SparkR | Burak Yavuz | Burak Yavuz |
| [SPARK-8522](https://issues.apache.org/jira/browse/SPARK-8522) | Disable feature scaling in Linear and Logistic Regression |  Major | ML | DB Tsai | DB Tsai |
| [SPARK-9381](https://issues.apache.org/jira/browse/SPARK-9381) | Migrate JSON data source to the new partitioning data source |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-9657](https://issues.apache.org/jira/browse/SPARK-9657) | PrefixSpan getMaxPatternLength should return an Int |  Trivial | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9112](https://issues.apache.org/jira/browse/SPARK-9112) | Implement LogisticRegressionSummary similar to LinearRegressionSummary |  Minor | ML | Manoj Kumar | Manoj Kumar |
| [SPARK-7083](https://issues.apache.org/jira/browse/SPARK-7083) | Binary processing dimensional join |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-5155](https://issues.apache.org/jira/browse/SPARK-5155) | Python API for MQTT streaming |  Major | DStreams, PySpark | Davies Liu | Prabeesh K |
| [SPARK-7293](https://issues.apache.org/jira/browse/SPARK-7293) | Report memory used in aggregations and joins |  Critical | Spark Core | Patrick Wendell | Andrew Or |
| [SPARK-8798](https://issues.apache.org/jira/browse/SPARK-8798) | Allow additional uris to be fetched with mesos |  Major | Mesos | Timothy Chen | Timothy Chen |
| [SPARK-8967](https://issues.apache.org/jira/browse/SPARK-8967) | Implement @since as an annotation |  Major | Documentation, Spark Core | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9028](https://issues.apache.org/jira/browse/SPARK-9028) | Add CountVectorizer as an estimator to generate CountVectorizerModel |  Major | ML | yuhao yang | yuhao yang |
| [SPARK-6813](https://issues.apache.org/jira/browse/SPARK-6813) | SparkR style guide |  Major | SparkR | Shivaram Venkataraman | Yu Ishikawa |
| [SPARK-10106](https://issues.apache.org/jira/browse/SPARK-10106) | Add \`ifelse\` Column function to SparkR |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9245](https://issues.apache.org/jira/browse/SPARK-9245) | DistributedLDAModel predict top topic per doc-term instance |  Major | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-4752](https://issues.apache.org/jira/browse/SPARK-4752) | Classifier based on artificial neural network |  Major | MLlib | Alexander Ulanov | Alexander Ulanov |
| [SPARK-3617](https://issues.apache.org/jira/browse/SPARK-3617) | Configurable case sensitivity |  Major | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-5109](https://issues.apache.org/jira/browse/SPARK-5109) | Loading multiple parquet files into a single SchemaRDD |  Major | SQL | Sam Steingold | Michael Armbrust |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-7357](https://issues.apache.org/jira/browse/SPARK-7357) | Improving HBaseTest example |  Minor | Examples | Jihong MA | Jihong MA |
| [SPARK-6470](https://issues.apache.org/jira/browse/SPARK-6470) | Allow Spark apps to put YARN node labels in their requests |  Major | YARN | Sandy Ryza | Sandy Ryza |
| [SPARK-7663](https://issues.apache.org/jira/browse/SPARK-7663) | [MLLIB] feature.Word2Vec throws empty iterator error when the vocabulary size is zero |  Minor | ML, MLlib | Xusen Yin | Xusen Yin |
| [SPARK-7533](https://issues.apache.org/jira/browse/SPARK-7533) | Decrease spacing between AM-RM heartbeats. |  Major | YARN | Sandy Ryza | Zoltán Zvara |
| [SPARK-7389](https://issues.apache.org/jira/browse/SPARK-7389) | Tachyon integration improvement |  Major | Block Manager | shimingfei | shimingfei |
| [SPARK-7657](https://issues.apache.org/jira/browse/SPARK-7657) | [YARN] Show driver link in Spark UI |  Minor | YARN | Hari Shreedharan | Hari Shreedharan |
| [SPARK-7795](https://issues.apache.org/jira/browse/SPARK-7795) | Speed up task serialization in standalone mode |  Major | Spark Core | Akshat Aranya | Akshat Aranya |
| [SPARK-5090](https://issues.apache.org/jira/browse/SPARK-5090) | The improvement of python converter for hbase |  Major | Examples | Gen TANG | Gen TANG |
| [SPARK-7637](https://issues.apache.org/jira/browse/SPARK-7637) | StructType.merge slow with large nenormalised tables O(N2) |  Minor | SQL | Rowan Chattaway | Rowan Chattaway |
| [SPARK-7887](https://issues.apache.org/jira/browse/SPARK-7887) | Remove EvaluatedType from SQL Expression |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7878](https://issues.apache.org/jira/browse/SPARK-7878) | Rename Stage.jobId to Stage.earliestJobId |  Minor | Scheduler | Kay Ousterhout | Kay Ousterhout |
| [SPARK-7826](https://issues.apache.org/jira/browse/SPARK-7826) | Suppress extra calling getCacheLocs. |  Major | Scheduler, Spark Core | Takuya Ueshin | Takuya Ueshin |
| [SPARK-7524](https://issues.apache.org/jira/browse/SPARK-7524) | add configs for keytab and principal, move originals to internal |  Major | YARN | Tao Wang | Tao Wang |
| [SPARK-7910](https://issues.apache.org/jira/browse/SPARK-7910) | Expose partitioner information in JavaRDD |  Minor | Java API | holdenk | holdenk |
| [SPARK-7945](https://issues.apache.org/jira/browse/SPARK-7945) | Do trim to values of properties |  Minor | Spark Core | Tao Wang | Tao Wang |
| [SPARK-7855](https://issues.apache.org/jira/browse/SPARK-7855) | Move hash-style shuffle code out of ExternalSorter and into own file |  Major | Shuffle | Josh Rosen | Josh Rosen |
| [SPARK-7691](https://issues.apache.org/jira/browse/SPARK-7691) | Use type-specific row accessor functions in CatalystTypeConverters' toScala functions |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-7983](https://issues.apache.org/jira/browse/SPARK-7983) | Add require for one-based indices in loadLibSVMFile |  Minor | MLlib | yuhao yang | yuhao yang |
| [SPARK-7801](https://issues.apache.org/jira/browse/SPARK-7801) | Upgrade master versions to Spark 1.5.0 |  Major | Build | Patrick Wendell | Patrick Wendell |
| [SPARK-7161](https://issues.apache.org/jira/browse/SPARK-7161) | Provide REST api to download event logs from History Server |  Minor | Spark Core | Hari Shreedharan | Hari Shreedharan |
| [SPARK-8054](https://issues.apache.org/jira/browse/SPARK-8054) | Java compatibility fixes for MLlib 1.4 |  Major | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8059](https://issues.apache.org/jira/browse/SPARK-8059) | Reduce latency between executor requests and RM heartbeat |  Minor | YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-8001](https://issues.apache.org/jira/browse/SPARK-8001) | Make AsynchronousListenerBus.waitUntilEmpty throw TimeoutException if timeout |  Minor | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-6164](https://issues.apache.org/jira/browse/SPARK-6164) | CrossValidatorModel should keep stats from fitting |  Minor | ML | Joseph K. Bradley | Leah McGuire |
| [SPARK-8084](https://issues.apache.org/jira/browse/SPARK-8084) | SparkR install script should fail with error if any packages required are not found |  Major | Build, SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-7969](https://issues.apache.org/jira/browse/SPARK-7969) | Drop method on Dataframes should handle Column |  Minor | PySpark, SQL | Olivier Girardot | Mike Dusenberry |
| [SPARK-8106](https://issues.apache.org/jira/browse/SPARK-8106) | Set derby.system.durability=test in order to speed up Hive compatibility tests |  Major | Build, SQL, Tests | Josh Rosen | Josh Rosen |
| [SPARK-6324](https://issues.apache.org/jira/browse/SPARK-6324) | Clean up usage code in command-line scripts |  Minor | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-7699](https://issues.apache.org/jira/browse/SPARK-7699) | Dynamic allocation: initial executors may be canceled before first job |  Major | Spark Core | meiyoula | Saisai Shao |
| [SPARK-7169](https://issues.apache.org/jira/browse/SPARK-7169) | Allow to specify metrics configuration more flexibly |  Minor | Spark Core | Jacek Lewandowski | Marcelo Vanzin |
| [SPARK-8141](https://issues.apache.org/jira/browse/SPARK-8141) | Precompute datatypes for partition columns and reuse it |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-7042](https://issues.apache.org/jira/browse/SPARK-7042) | Spark version of akka-actor\_2.11 is not compatible with the official akka-actor\_2.11 2.3.x |  Minor | Spark Core | Konstantin Shaposhnikov | Konstantin Shaposhnikov |
| [SPARK-8117](https://issues.apache.org/jira/browse/SPARK-8117) | Push codegen into Expression |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8149](https://issues.apache.org/jira/browse/SPARK-8149) | Break ExpressionEvaluationSuite down to multiple files |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8154](https://issues.apache.org/jira/browse/SPARK-8154) | Remove Term/Code type aliases in code generation |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7705](https://issues.apache.org/jira/browse/SPARK-7705) | Cleanup of .sparkStaging directory fails if application is killed |  Minor | YARN | Wilfred Spiegelenburg | Weizhong |
| [SPARK-8140](https://issues.apache.org/jira/browse/SPARK-8140) | Remove empty model check in StreamingLinearAlgorithm |  Trivial | DStreams, MLlib | Manoj Kumar | Manoj Kumar |
| [SPARK-8158](https://issues.apache.org/jira/browse/SPARK-8158) | HiveShim improvement |  Major | SQL | Adrian Wang | Adrian Wang |
| [SPARK-8168](https://issues.apache.org/jira/browse/SPARK-8168) | Add Python friendly constructor to PipelineModel |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8101](https://issues.apache.org/jira/browse/SPARK-8101) | Upgrade netty to avoid memory leak accord to netty #3837 issues |  Minor | Spark Core | SuYan | Sean Owen |
| [SPARK-7886](https://issues.apache.org/jira/browse/SPARK-7886) | Add built-in expressions to FunctionRegistry |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7261](https://issues.apache.org/jira/browse/SPARK-7261) | Change default log level to WARN in the REPL |  Blocker | Spark Shell | Patrick Wendell | Shixiong Zhu |
| [SPARK-8282](https://issues.apache.org/jira/browse/SPARK-8282) | Make number of threads used in RBackend configurable |  Major | SparkR | Hossein Falaki | Hossein Falaki |
| [SPARK-2774](https://issues.apache.org/jira/browse/SPARK-2774) | Set preferred locations for reduce tasks |  Major | Spark Core | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8189](https://issues.apache.org/jira/browse/SPARK-8189) | Use 100ns precision for TimestampType |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8126](https://issues.apache.org/jira/browse/SPARK-8126) | Use temp directory under build dir for unit tests |  Minor | Build | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-8164](https://issues.apache.org/jira/browse/SPARK-8164) | transformExpressions should support nested expression sequence |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7444](https://issues.apache.org/jira/browse/SPARK-7444) | Eliminate noisy css warn/error logs for UISeleniumSuite |  Minor | Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8286](https://issues.apache.org/jira/browse/SPARK-8286) | Rewrite UTF8String in Java and move it into unsafe package. |  Minor | Spark Core, SQL | Reynold Xin | Reynold Xin |
| [SPARK-7824](https://issues.apache.org/jira/browse/SPARK-7824) | Collapsing operator reordering and constant folding into a single batch to push down the single side. |  Major | SQL | Zhongshuai Pei | Zhongshuai Pei |
| [SPARK-8317](https://issues.apache.org/jira/browse/SPARK-8317) | Do not push sort into shuffle in Exchange operator |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-6566](https://issues.apache.org/jira/browse/SPARK-6566) | Update Spark to use the latest version of Parquet libraries |  Major | SQL | Konstantin Shaposhnikov | Yash Datta |
| [SPARK-8314](https://issues.apache.org/jira/browse/SPARK-8314) | improvement in performance of MLUtils.appendBias |  Major | MLlib | Roger Menezes | Roger Menezes |
| [SPARK-8346](https://issues.apache.org/jira/browse/SPARK-8346) | Use InternalRow instread of catalyst.InternalRow |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8319](https://issues.apache.org/jira/browse/SPARK-8319) | Update logic related to key ordering in shuffle dependencies |  Major | Shuffle, SQL | Josh Rosen | Josh Rosen |
| [SPARK-8349](https://issues.apache.org/jira/browse/SPARK-8349) | Use expression constructors (rather than apply) in FunctionRegistry |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8343](https://issues.apache.org/jira/browse/SPARK-8343) | Improve the Spark Streaming Guides |  Minor | Documentation, DStreams | Mike Dusenberry | Mike Dusenberry |
| [SPARK-8316](https://issues.apache.org/jira/browse/SPARK-8316) | Upgrade Maven to 3.3.3 |  Minor | Build | Nicholas Chammas | Nicholas Chammas |
| [SPARK-6583](https://issues.apache.org/jira/browse/SPARK-6583) | Support aggregated function in order by |  Major | SQL | Yadong Qi | Yadong Qi |
| [SPARK-7184](https://issues.apache.org/jira/browse/SPARK-7184) | Investigate turning codegen on by default |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8387](https://issues.apache.org/jira/browse/SPARK-8387) | [SPARK][Web-UI] Only show 4096 bytes content for executor log instead all |  Minor | Web UI, YARN | SuYan | SuYan |
| [SPARK-7916](https://issues.apache.org/jira/browse/SPARK-7916) | MLlib Python doc parity check for classification and regression. |  Major | Documentation, MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-7020](https://issues.apache.org/jira/browse/SPARK-7020) | Restrict module testing based on commit contents |  Critical | Build, Project Infra | Brennon York | Brennon York |
| [SPARK-8077](https://issues.apache.org/jira/browse/SPARK-8077) | Optimisation of TreeNode for large number of children |  Minor | SQL | Mick Davies | Mick Davies |
| [SPARK-8395](https://issues.apache.org/jira/browse/SPARK-8395) | spark-submit documentation is incorrect |  Minor | Documentation | Dev Lakhani | Sean Owen |
| [SPARK-6782](https://issues.apache.org/jira/browse/SPARK-6782) | add sbt-revolver plugin to sbt build |  Minor | Build | Imran Rashid | Imran Rashid |
| [SPARK-7913](https://issues.apache.org/jira/browse/SPARK-7913) | Increase the maximum capacity of PartitionedPairBuffer, PartitionedSerializedPairBuffer and AppendOnlyMap |  Minor | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8397](https://issues.apache.org/jira/browse/SPARK-8397) | Allow custom configuration for TestHive |  Minor | SQL | Punya Biswal | Punya Biswal |
| [SPARK-8392](https://issues.apache.org/jira/browse/SPARK-8392) | RDDOperationGraph: getting cached nodes is slow |  Minor | Spark Core | meiyoula | meiyoula |
| [SPARK-8381](https://issues.apache.org/jira/browse/SPARK-8381) | reuse typeConvert when convert Seq[Row] to catalyst type |  Major | SQL | Lianhui Wang | Lianhui Wang |
| [SPARK-7961](https://issues.apache.org/jira/browse/SPARK-7961) | Redesign SQLConf for better error message reporting |  Critical | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-8135](https://issues.apache.org/jira/browse/SPARK-8135) | Don't load defaults when reconstituting Hadoop Configurations |  Major | Spark Core | Sandy Ryza | Sandy Ryza |
| [SPARK-8301](https://issues.apache.org/jira/browse/SPARK-8301) | Improve UTF8String substring/startsWith/endsWith/contains performance |  Critical | SQL | Reynold Xin | Tarek Auel |
| [SPARK-7426](https://issues.apache.org/jira/browse/SPARK-7426) | spark.ml AttributeFactory.fromStructField should allow other NumericTypes |  Minor | ML | Joseph K. Bradley | Mike Dusenberry |
| [SPARK-8429](https://issues.apache.org/jira/browse/SPARK-8429) | Add ability to set additional tags |  Minor | EC2 | Stefano Parmesan | Stefano Parmesan |
| [SPARK-8482](https://issues.apache.org/jira/browse/SPARK-8482) | Add M4 instances support |  Trivial | EC2 | Pradeep Chhetri | Pradeep Chhetri |
| [SPARK-8511](https://issues.apache.org/jira/browse/SPARK-8511) | Modify ML Python tests to remove saved models |  Major | PySpark | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8307](https://issues.apache.org/jira/browse/SPARK-8307) | Improve timestamp from parquet |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-7235](https://issues.apache.org/jira/browse/SPARK-7235) | Refactor the GroupingSet implementation |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-8139](https://issues.apache.org/jira/browse/SPARK-8139) | Documents data sources and Parquet output committer related options |  Minor | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6749](https://issues.apache.org/jira/browse/SPARK-6749) | Make metastore client robust to underlying socket connection loss |  Critical | SQL | Yin Huai | Eric Liang |
| [SPARK-8138](https://issues.apache.org/jira/browse/SPARK-8138) | Error message for discovered conflicting partition columns is not intuitive |  Minor | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8576](https://issues.apache.org/jira/browse/SPARK-8576) | Add spark-ec2 options to assign launched instances into IAM roles and to set instance-initiated shutdown behavior |  Minor | EC2 | Nicholas Chammas | Nicholas Chammas |
| [SPARK-8127](https://issues.apache.org/jira/browse/SPARK-8127) | KafkaRDD optimize count() take() isEmpty() |  Minor | DStreams | Cody Koeninger | Cody Koeninger |
| [SPARK-7289](https://issues.apache.org/jira/browse/SPARK-7289) | Combine Limit and Sort to avoid total ordering |  Major | SQL | Fei Wang | Wenchen Fan |
| [SPARK-7884](https://issues.apache.org/jira/browse/SPARK-7884) | Move block deserialization from BlockStoreShuffleFetcher to ShuffleReader |  Major | Spark Core | Matt Massie | Matt Massie |
| [SPARK-5768](https://issues.apache.org/jira/browse/SPARK-5768) | Spark UI Shows incorrect memory under Yarn |  Trivial | Web UI | Al M | Rekha Joshi |
| [SPARK-8635](https://issues.apache.org/jira/browse/SPARK-8635) | improve performance of CatalystTypeConverters |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8620](https://issues.apache.org/jira/browse/SPARK-8620) | cleanup CodeGenContext |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-5482](https://issues.apache.org/jira/browse/SPARK-5482) | Allow individual test suites in python/run-tests |  Minor | PySpark | Katsunori Kanda | Josh Rosen |
| [SPARK-8610](https://issues.apache.org/jira/browse/SPARK-8610) | Separate Row and InternalRow (part 2) |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8686](https://issues.apache.org/jira/browse/SPARK-8686) | DataFrame should support \`where\` with expression represented by String |  Minor | SQL | Kousuke Saruta | Kousuke Saruta |
| [SPARK-7845](https://issues.apache.org/jira/browse/SPARK-7845) | Bump "Hadoop 1" tests to version 1.2.1 |  Critical | Tests | Patrick Wendell | Cheng Lian |
| [SPARK-8575](https://issues.apache.org/jira/browse/SPARK-8575) | Deprecate callUDF in favor of udf |  Minor | SQL | Benjamin Fradet | Benjamin Fradet |
| [SPARK-8692](https://issues.apache.org/jira/browse/SPARK-8692) | re-order the case statements that handling catalyst data types |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8528](https://issues.apache.org/jira/browse/SPARK-8528) | Add applicationId to SparkContext object in pyspark |  Minor | PySpark | Vladimir Vladimirov | Vladimir Vladimirov |
| [SPARK-8070](https://issues.apache.org/jira/browse/SPARK-8070) | Improve createDataFrame in Python |  Major | PySpark | Davies Liu | Davies Liu |
| [SPARK-7810](https://issues.apache.org/jira/browse/SPARK-7810) | rdd.py "\_load\_from\_socket" cannot load data from jvm socket if ipv6 is used |  Major | PySpark | Ai He | Ai He |
| [SPARK-8660](https://issues.apache.org/jira/browse/SPARK-8660) | Update comments that contain R statements in ml.logisticRegressionSuite |  Trivial | ML | Xiangrui Meng | somil deshmukh |
| [SPARK-8478](https://issues.apache.org/jira/browse/SPARK-8478) | Harmonize UDF-related code to use uniformly UDF instead of Udf |  Minor | SQL | Benjamin Fradet | Benjamin Fradet |
| [SPARK-8661](https://issues.apache.org/jira/browse/SPARK-8661) | Update comments that contain R statements in ml.LinearRegressionSuite |  Major | ML | Xiangrui Meng | somil deshmukh |
| [SPARK-8589](https://issues.apache.org/jira/browse/SPARK-8589) | cleanup DateTimeUtils |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8475](https://issues.apache.org/jira/browse/SPARK-8475) | SparkSubmit with Ivy jars is very slow to load with no internet access |  Minor | Spark Submit | Nathan McCarthy | Burak Yavuz |
| [SPARK-5161](https://issues.apache.org/jira/browse/SPARK-5161) | Parallelize Python test execution |  Major | Project Infra | Nicholas Chammas | Josh Rosen |
| [SPARK-8590](https://issues.apache.org/jira/browse/SPARK-8590) | add code gen for ExtractValue |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8723](https://issues.apache.org/jira/browse/SPARK-8723) | improve code gen for divide and remainder |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8713](https://issues.apache.org/jira/browse/SPARK-8713) | Support codegen for not thread-safe expressions |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8630](https://issues.apache.org/jira/browse/SPARK-8630) | Prevent from checkpointing QueueInputDStream |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-7739](https://issues.apache.org/jira/browse/SPARK-7739) | Improve ChiSqSelector example code in the user guide |  Minor | Documentation, MLlib | Xiangrui Meng | Seth Hendrickson |
| [SPARK-8727](https://issues.apache.org/jira/browse/SPARK-8727) | Add missing python api |  Major | SQL | Tarek Auel | Tarek Auel |
| [SPARK-8748](https://issues.apache.org/jira/browse/SPARK-8748) | Move castability test out from Cast case class into Cast object |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8265](https://issues.apache.org/jira/browse/SPARK-8265) | Add LinearDataGenerator to pyspark.mllib.utils |  Minor | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-7714](https://issues.apache.org/jira/browse/SPARK-7714) | SparkR tests should use more specific expectations than expect\_true |  Major | SparkR | Josh Rosen | Sun Rui |
| [SPARK-8378](https://issues.apache.org/jira/browse/SPARK-8378) | Add Spark Flume Python API |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8771](https://issues.apache.org/jira/browse/SPARK-8771) | Actor system deprecation tag uses deprecated deprecation tag |  Trivial | . | holdenk | holdenk |
| [SPARK-8740](https://issues.apache.org/jira/browse/SPARK-8740) | Support GitHub OAuth tokens in dev/merge\_spark\_pr.py |  Minor | Project Infra | Josh Rosen | Josh Rosen |
| [SPARK-3071](https://issues.apache.org/jira/browse/SPARK-3071) | Increase default driver memory |  Major | Spark Core | Xiangrui Meng | Ilya Ganelin |
| [SPARK-8787](https://issues.apache.org/jira/browse/SPARK-8787) | Change the parameter  order of @deprecated in package object sql |  Trivial | SQL | Vinod KC | Vinod KC |
| [SPARK-8690](https://issues.apache.org/jira/browse/SPARK-8690) | Add a setting to disable SparkSQL parquet schema merge by using datasource API |  Minor | SQL | thegiive | thegiive |
| [SPARK-8647](https://issues.apache.org/jira/browse/SPARK-8647) | Potential issues with the constant hashCode |  Minor | MLlib | Alok Singh | Alok Singh |
| [SPARK-8708](https://issues.apache.org/jira/browse/SPARK-8708) | MatrixFactorizationModel.predictAll() populates single partition only |  Major | MLlib | Antony Mayi | Liang-Chi Hsieh |
| [SPARK-3382](https://issues.apache.org/jira/browse/SPARK-3382) | GradientDescent convergence tolerance |  Minor | MLlib | Joseph K. Bradley | Kai Sasaki |
| [SPARK-6980](https://issues.apache.org/jira/browse/SPARK-6980) | Akka timeout exceptions indicate which conf controls them |  Minor | Spark Core | Imran Rashid | Bryan Cutler |
| [SPARK-8776](https://issues.apache.org/jira/browse/SPARK-8776) | Increase the default MaxPermSize |  Major | Spark Core | Yin Huai | Yin Huai |
| [SPARK-8809](https://issues.apache.org/jira/browse/SPARK-8809) | Remove ConvertNaNs analyzer rule |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7137](https://issues.apache.org/jira/browse/SPARK-7137) | Add checkInputColumn back to Params and print more info |  Trivial | ML | Joseph K. Bradley | Rekha Joshi |
| [SPARK-8837](https://issues.apache.org/jira/browse/SPARK-8837) | support using keyword in column name |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-4485](https://issues.apache.org/jira/browse/SPARK-4485) | Add broadcast outer join to  optimize left outer join and right outer join |  Critical | SQL | XiaoJing wang | Kai Zeng |
| [SPARK-6707](https://issues.apache.org/jira/browse/SPARK-6707) | Mesos Scheduler should allow the user to specify constraints based on slave attributes |  Major | Mesos, Scheduler | Ankur Chauhan | Ankur Chauhan |
| [SPARK-8759](https://issues.apache.org/jira/browse/SPARK-8759) | add default eval to binary and unary expression according to default behavior of nullable |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8788](https://issues.apache.org/jira/browse/SPARK-8788) | Java unit test for PCA transformer |  Minor | ML | Yanbo Liang | Yanbo Liang |
| [SPARK-8570](https://issues.apache.org/jira/browse/SPARK-8570) | Improve MLlib Local Matrix Documentation. |  Minor | Documentation, MLlib | Mike Dusenberry | Mike Dusenberry |
| [SPARK-8823](https://issues.apache.org/jira/browse/SPARK-8823) | Optimizations for sparse vector products in pyspark.mllib.linalg |  Minor | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8559](https://issues.apache.org/jira/browse/SPARK-8559) | Support association rule generation in FPGrowth |  Major | MLlib | Guangwen Liu | Feynman Liang |
| [SPARK-8876](https://issues.apache.org/jira/browse/SPARK-8876) | Remove InternalRow type alias in expressions package |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8879](https://issues.apache.org/jira/browse/SPARK-8879) | Remove EmptyRow class |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8883](https://issues.apache.org/jira/browse/SPARK-8883) | Remove the class OverrideFunctionRegistry |  Minor | SQL | Cheng Hao | Cheng Hao |
| [SPARK-8872](https://issues.apache.org/jira/browse/SPARK-8872) | Improve FPGrowthSuite with equivalent R code |  Minor | MLlib | Xiangrui Meng | Kashif Rasul |
| [SPARK-8785](https://issues.apache.org/jira/browse/SPARK-8785) | Improve Parquet schema merging |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-8068](https://issues.apache.org/jira/browse/SPARK-8068) | Add confusionMatrix method at class MulticlassMetrics in pyspark/mllib |  Minor | PySpark | Ai He | Yanbo Liang |
| [SPARK-8877](https://issues.apache.org/jira/browse/SPARK-8877) | Public API for association rule generation |  Minor | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-5016](https://issues.apache.org/jira/browse/SPARK-5016) | GaussianMixtureEM should distribute matrix inverse for large numFeatures, k |  Major | MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-8914](https://issues.apache.org/jira/browse/SPARK-8914) | Remove RDDApi |  Minor | SQL | Kousuke Saruta | Kousuke Saruta |
| [SPARK-8866](https://issues.apache.org/jira/browse/SPARK-8866) | Use 1 microsecond (us) precision for TimestampType |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8931](https://issues.apache.org/jira/browse/SPARK-8931) | Fallback to interpret mode if failed to compile in codegen |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-8948](https://issues.apache.org/jira/browse/SPARK-8948) | Remove ExtractValueWithOrdinal abstract class |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8863](https://issues.apache.org/jira/browse/SPARK-8863) | 'spark\_ec2.py' doesn't check '~/.aws/credentials' even if boto can support '~/.aws/credentials' |  Minor | EC2 | Juhong Park | Juhong Park |
| [SPARK-6287](https://issues.apache.org/jira/browse/SPARK-6287) | Add support for dynamic allocation in the Mesos coarse-grained scheduler |  Major | Mesos | Iulian Dragos | Iulian Dragos |
| [SPARK-8701](https://issues.apache.org/jira/browse/SPARK-8701) | Add input metadata to InputInfo and display it in the batch page |  Minor | DStreams, Web UI | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8963](https://issues.apache.org/jira/browse/SPARK-8963) | Improve Linear Regression tests to use Vectors |  Trivial | . | holdenk | holdenk |
| [SPARK-8913](https://issues.apache.org/jira/browse/SPARK-8913) | Follow-up on SPARK-8700. Cleanup the test |  Major | ML | DB Tsai | holdenk |
| [SPARK-6154](https://issues.apache.org/jira/browse/SPARK-6154) | Support Kafka, JDBC in Scala 2.11 |  Major | Build | Jianshi Huang | Iulian Dragos |
| [SPARK-8994](https://issues.apache.org/jira/browse/SPARK-8994) | Tiny cleanups to Params, Pipeline |  Trivial | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8970](https://issues.apache.org/jira/browse/SPARK-8970) | remove unnecessary abstraction for ExtractValue |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8880](https://issues.apache.org/jira/browse/SPARK-8880) | Fix confusing Stage.attemptId member variable |  Minor | Scheduler | Kay Ousterhout | Kay Ousterhout |
| [SPARK-8596](https://issues.apache.org/jira/browse/SPARK-8596) | Install and configure RStudio server on Spark EC2 |  Major | EC2, SparkR | Shivaram Venkataraman | Vincent Warmerdam |
| [SPARK-6797](https://issues.apache.org/jira/browse/SPARK-6797) | Add support for YARN cluster mode |  Critical | SparkR | Shivaram Venkataraman | Sun Rui |
| [SPARK-8991](https://issues.apache.org/jira/browse/SPARK-8991) | Update SharedParamsCodeGen's Generated Documentation |  Trivial | ML | Feynman Liang | Vinod KC |
| [SPARK-9010](https://issues.apache.org/jira/browse/SPARK-9010) | Improve the Spark Configuration document about \`spark.kryoserializer.buffer\` |  Trivial | Documentation | StanZhai | StanZhai |
| [SPARK-9029](https://issues.apache.org/jira/browse/SPARK-9029) | shortcut CaseKeyWhen if key is null |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8933](https://issues.apache.org/jira/browse/SPARK-8933) | Provide a --force flag to build/mvn that always uses downloaded maven |  Major | Build | Patrick Wendell | Brennon York |
| [SPARK-8718](https://issues.apache.org/jira/browse/SPARK-8718) | Improve EdgePartition2D for non perfect square number of partitions |  Minor | GraphX | Andrew Ray | Andrew Ray |
| [SPARK-4362](https://issues.apache.org/jira/browse/SPARK-4362) | Make prediction probability available in NaiveBayesModel |  Minor | MLlib | Jatinpreet Singh | Sean Owen |
| [SPARK-8820](https://issues.apache.org/jira/browse/SPARK-8820) | Add a configuration to set the checkpoint directory for convenience. |  Minor | DStreams | carlmartin | carlmartin |
| [SPARK-6259](https://issues.apache.org/jira/browse/SPARK-6259) | Python API for LDA |  Major | MLlib, PySpark | Joseph K. Bradley | Yu Ishikawa |
| [SPARK-8018](https://issues.apache.org/jira/browse/SPARK-8018) | KMeans should accept initial cluster centers as param |  Major | MLlib | Joseph K. Bradley | Meethu Mathew |
| [SPARK-8997](https://issues.apache.org/jira/browse/SPARK-8997) | Improve LocalPrefixSpan performance |  Major | MLlib | Xiangrui Meng | Feynman Liang |
| [SPARK-8893](https://issues.apache.org/jira/browse/SPARK-8893) | Require positive partition counts in RDD.repartition |  Trivial | Spark Core | Daniel Darabos | Daniel Darabos |
| [SPARK-8995](https://issues.apache.org/jira/browse/SPARK-8995) | Cast date strings with date, date and time and just time information to DateType and TimestampTzpe |  Major | SQL | Tarek Auel | Tarek Auel |
| [SPARK-9015](https://issues.apache.org/jira/browse/SPARK-9015) | Maven cleanup / Clean Project Import in scala-ide |  Minor | Build | Jan Prach | Jan Prach |
| [SPARK-6941](https://issues.apache.org/jira/browse/SPARK-6941) | Provide a better error message to explain that tables created from RDDs are immutable |  Blocker | SQL | Yin Huai | Yijie Shen |
| [SPARK-9085](https://issues.apache.org/jira/browse/SPARK-9085) | Remove LeafNode, UnaryNode, BinaryNode from TreeNode |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6284](https://issues.apache.org/jira/browse/SPARK-6284) | Support framework authentication and role in Mesos framework |  Major | Mesos | Timothy Chen | Timothy Chen |
| [SPARK-8899](https://issues.apache.org/jira/browse/SPARK-8899) | remove duplicated equals method for Row |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7131](https://issues.apache.org/jira/browse/SPARK-7131) | Move tree,forest implementation from spark.mllib to spark.ml |  Major | ML, MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9130](https://issues.apache.org/jira/browse/SPARK-9130) | throw exception when check equality between external and internal row |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9062](https://issues.apache.org/jira/browse/SPARK-9062) | Change output type of Tokenizer to Array(String, true) |  Minor | ML | yuhao yang | yuhao yang |
| [SPARK-8792](https://issues.apache.org/jira/browse/SPARK-8792) | Add Python API for PCA transformer |  Major | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-7127](https://issues.apache.org/jira/browse/SPARK-7127) | Broadcast spark.ml tree ensemble models for predict |  Minor | ML | Joseph K. Bradley | Bryan Cutler |
| [SPARK-9142](https://issues.apache.org/jira/browse/SPARK-9142) | Removing unnecessary self types in Catalyst |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9113](https://issues.apache.org/jira/browse/SPARK-9113) | enable analysis check code for self join |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9118](https://issues.apache.org/jira/browse/SPARK-9118) | Implement integer array parameters for ml.param as IntArrayParam |  Minor | ML | Alexander Ulanov | Rekha Joshi |
| [SPARK-8390](https://issues.apache.org/jira/browse/SPARK-8390) | Update DirectKafkaWordCount examples to show how offset ranges can be used |  Major | DStreams | Tathagata Das | Cody Koeninger |
| [SPARK-9174](https://issues.apache.org/jira/browse/SPARK-9174) | Add documentation for all public SQLConfs |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9094](https://issues.apache.org/jira/browse/SPARK-9094) | Increase io.dropwizard.metrics dependency to 3.1.2 |  Minor | Spark Core | Carl Anders Düvel | Carl Anders Düvel |
| [SPARK-9179](https://issues.apache.org/jira/browse/SPARK-9179) | Allow committers to specify the primary author of the PR to be merged |  Minor | Build | Cheng Lian | Cheng Lian |
| [SPARK-8749](https://issues.apache.org/jira/browse/SPARK-8749) | Remove HiveTypeCoercion trait |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9185](https://issues.apache.org/jira/browse/SPARK-9185) | improve code gen for mutable states to support complex initialization |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9100](https://issues.apache.org/jira/browse/SPARK-9100) | DataFrame reader/writer shortcut methods for ORC |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8875](https://issues.apache.org/jira/browse/SPARK-8875) | Shuffle code cleanup: remove BlockStoreShuffleFetcher class |  Minor | Shuffle | Kay Ousterhout | Kay Ousterhout |
| [SPARK-9036](https://issues.apache.org/jira/browse/SPARK-9036) | SparkListenerExecutorMetricsUpdate messages not included in JsonProtocol |  Minor | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-9128](https://issues.apache.org/jira/browse/SPARK-9128) | Get outerclasses and objects at the same time in ClosureCleaner |  Major | Spark Core | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-7171](https://issues.apache.org/jira/browse/SPARK-7171) | Allow for more flexible use of metric sources |  Minor | Spark Core | Jacek Lewandowski | Jacek Lewandowski |
| [SPARK-5423](https://issues.apache.org/jira/browse/SPARK-5423) | ExternalAppendOnlyMap won't delete temp spilled file if some exception happens during using it |  Major | Shuffle | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9232](https://issues.apache.org/jira/browse/SPARK-9232) | Duplicate code in JSONRelation |  Minor | SQL | Andrew Or | Andrew Or |
| [SPARK-9224](https://issues.apache.org/jira/browse/SPARK-9224) | OnlineLDAOptimizer Performance Improvements |  Major | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-4234](https://issues.apache.org/jira/browse/SPARK-4234) | Always do paritial aggregation |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-8536](https://issues.apache.org/jira/browse/SPARK-8536) | Generalize LDA to asymmetric doc-topic priors |  Major | MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-9244](https://issues.apache.org/jira/browse/SPARK-9244) | Increase some default memory limits |  Minor | Spark Core | Matei Zaharia | Matei Zaharia |
| [SPARK-9180](https://issues.apache.org/jira/browse/SPARK-9180) | Accept --name option in spark-submit |  Trivial | Spark Shell | Kenichi Maehashi | Kenichi Maehashi |
| [SPARK-9144](https://issues.apache.org/jira/browse/SPARK-9144) | Remove DAGScheduler.runLocallyWithinThread and spark.localExecution.enabled |  Major | Scheduler, Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-9262](https://issues.apache.org/jira/browse/SPARK-9262) | Treat Scala compiler warnings as errors |  Major | Build | Reynold Xin | Reynold Xin |
| [SPARK-9268](https://issues.apache.org/jira/browse/SPARK-9268) | Params.setDefault should not keep varargs annotation |  Major | Java API, ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8695](https://issues.apache.org/jira/browse/SPARK-8695) | TreeAggregation shouldn't be triggered when it doesn't save wall-clock time |  Minor | MLlib, Spark Core | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9243](https://issues.apache.org/jira/browse/SPARK-9243) | Update crosstab doc for pairs that have no occurrences |  Trivial | Documentation, PySpark, SparkR, SQL | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9122](https://issues.apache.org/jira/browse/SPARK-9122) | spark.mllib regression should support batch predict |  Major | MLlib, PySpark | Joseph K. Bradley | Yanbo Liang |
| [SPARK-9250](https://issues.apache.org/jira/browse/SPARK-9250) | ./dev/change-scala-version.sh should offer guidance what versions are accepted, i.e. 2.10 or 2.11 |  Minor | Build | Jacek Laskowski | François Garillot |
| [SPARK-9305](https://issues.apache.org/jira/browse/SPARK-9305) | Rename org.apache.spark.Row to Item |  Major | Spark Core | Reynold Xin | Reynold Xin |
| [SPARK-9285](https://issues.apache.org/jira/browse/SPARK-9285) | Remove InternalRow's inheritance from Row |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9067](https://issues.apache.org/jira/browse/SPARK-9067) | Memory overflow and open file limit exhaustion for NewParquetRDD+CoalescedRDD |  Major | Input/Output | konstantin knizhnik | Liang-Chi Hsieh |
| [SPARK-7045](https://issues.apache.org/jira/browse/SPARK-7045) | Word2Vec: avoid intermediate representation when creating model |  Minor | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-9336](https://issues.apache.org/jira/browse/SPARK-9336) | Remove all extra JoinedRows |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9334](https://issues.apache.org/jira/browse/SPARK-9334) | Remove UnsafeRowConverter in favor of UnsafeProjection |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9304](https://issues.apache.org/jira/browse/SPARK-9304) | Improve backwards compatibility of SPARK-8401 |  Critical | Build | Patrick Wendell | Sean Owen |
| [SPARK-9337](https://issues.apache.org/jira/browse/SPARK-9337) | Add an ut for Word2Vec to verify the empty vocabulary check |  Trivial | MLlib | yuhao yang | yuhao yang |
| [SPARK-9376](https://issues.apache.org/jira/browse/SPARK-9376) | use a seed in RandomDataGeneratorSuite |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7423](https://issues.apache.org/jira/browse/SPARK-7423) | spark.ml Classifier predict should not convert vectors to dense format |  Minor | ML | Joseph K. Bradley | George Dittmar |
| [SPARK-9351](https://issues.apache.org/jira/browse/SPARK-9351) | remove literals from grouping expressions in Aggregate |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-4352](https://issues.apache.org/jira/browse/SPARK-4352) | Incorporate locality preferences in dynamic allocation requests |  Critical | Spark Core, YARN | Sandy Ryza | Saisai Shao |
| [SPARK-9373](https://issues.apache.org/jira/browse/SPARK-9373) | Support StructType in Tungsten style Projection |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9397](https://issues.apache.org/jira/browse/SPARK-9397) | DataFrame should provide an API to find source data files if applicable |  Critical | SQL | Aaron Davidson | Aaron Davidson |
| [SPARK-9247](https://issues.apache.org/jira/browse/SPARK-9247) | Use BytesToBytesMap in unsafe broadcast join |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-9418](https://issues.apache.org/jira/browse/SPARK-9418) | Use sort-merge join as the default shuffle join |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8599](https://issues.apache.org/jira/browse/SPARK-8599) | Improve non-deterministic expression handling |  Critical | SQL | Yin Huai | Wenchen Fan |
| [SPARK-9251](https://issues.apache.org/jira/browse/SPARK-9251) | do not order by expressions which still need evaluation |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9352](https://issues.apache.org/jira/browse/SPARK-9352) | Add tests for standalone scheduling code |  Critical | Deploy, Tests | Andrew Or | Andrew Or |
| [SPARK-746](https://issues.apache.org/jira/browse/SPARK-746) | Automatically Use Avro Serialization for Avro Objects |  Major | Spark Core | Patrick Cogan | Joseph Batchik |
| [SPARK-9436](https://issues.apache.org/jira/browse/SPARK-9436) | Simplify Pregel by merging joins |  Minor | GraphX | Alexander Ulanov | Alexander Ulanov |
| [SPARK-9411](https://issues.apache.org/jira/browse/SPARK-9411) | Make page size configurable |  Critical | Spark Core | Reynold Xin | Josh Rosen |
| [SPARK-6793](https://issues.apache.org/jira/browse/SPARK-6793) | Implement perplexity for LDA |  Major | MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-8838](https://issues.apache.org/jira/browse/SPARK-8838) | Add config to enable/disable merging part-files when merging parquet schema |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-5561](https://issues.apache.org/jira/browse/SPARK-5561) | Generalize PeriodicGraphCheckpointer for RDDs |  Major | GraphX, MLlib, Spark Core | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8998](https://issues.apache.org/jira/browse/SPARK-8998) | Collect enough frequent prefixes before projection in PrefixSpan |  Major | MLlib | Xiangrui Meng | Zhang JiaJin |
| [SPARK-9388](https://issues.apache.org/jira/browse/SPARK-9388) | Make log messages in ExecutorRunnable more readable |  Trivial | YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-5567](https://issues.apache.org/jira/browse/SPARK-5567) | Add prediction methods to LDA |  Major | MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-9454](https://issues.apache.org/jira/browse/SPARK-9454) | LDASuite should use vector comparisons |  Minor | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-6684](https://issues.apache.org/jira/browse/SPARK-6684) | Add checkpointing to GradientBoostedTrees |  Major | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9077](https://issues.apache.org/jira/browse/SPARK-9077) | Improve error message for decision trees when numExamples \< maxCategoriesPerFeature |  Trivial | MLlib | Joseph K. Bradley | Sean Owen |
| [SPARK-9489](https://issues.apache.org/jira/browse/SPARK-9489) | Remove compatibleWith, meetsRequirements, and needsAnySort checks from Exchange |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8943](https://issues.apache.org/jira/browse/SPARK-8943) | CalendarIntervalType for time intervals |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9214](https://issues.apache.org/jira/browse/SPARK-9214) | support ml.NaiveBayes for Python |  Major | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-9496](https://issues.apache.org/jira/browse/SPARK-9496) | Do not print password in Hive Config |  Minor | SQL | Tao Wang | Tao Wang |
| [SPARK-9477](https://issues.apache.org/jira/browse/SPARK-9477) | Adding IBM Platform Application Service Controller into Spark documentation as a supported Cluster Manager (beside Yarn and Mesos). |  Minor | Documentation | Stacy Pedersen | Sean Owen |
| [SPARK-9481](https://issues.apache.org/jira/browse/SPARK-9481) | LocalLDAModel logLikelihood |  Trivial | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9308](https://issues.apache.org/jira/browse/SPARK-9308) | ml.NaiveBayesModel support predicting class probabilities |  Minor | ML | Yanbo Liang | Yanbo Liang |
| [SPARK-9507](https://issues.apache.org/jira/browse/SPARK-9507) | Remove dependency reduced POM hack now that shade plugin is updated |  Minor | Build | Sean Owen | Sean Owen |
| [SPARK-7446](https://issues.apache.org/jira/browse/SPARK-7446) | Inverse transform for StringIndexer |  Minor | ML | Xiangrui Meng | holdenk |
| [SPARK-8999](https://issues.apache.org/jira/browse/SPARK-8999) | Support non-temporal sequence in PrefixSpan |  Critical | MLlib | Xiangrui Meng | Zhang JiaJin |
| [SPARK-9000](https://issues.apache.org/jira/browse/SPARK-9000) | Support generic item type in PrefixSpan |  Critical | MLlib | Xiangrui Meng | Feynman Liang |
| [SPARK-9521](https://issues.apache.org/jira/browse/SPARK-9521) | Require Maven 3.3.3+ in the build |  Trivial | Build | Sean Owen | Sean Owen |
| [SPARK-9527](https://issues.apache.org/jira/browse/SPARK-9527) | PrefixSpan.run should return a PrefixSpanModel instead of an RDD and it should be Java-friendly |  Critical | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9535](https://issues.apache.org/jira/browse/SPARK-9535) | Modify document for codegen |  Minor | Documentation, SQL | Kousuke Saruta | KaiXinXIaoLei |
| [SPARK-9536](https://issues.apache.org/jira/browse/SPARK-9536) | NaiveBayesModel support probability prediction for PySpark.ml |  Minor | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-9537](https://issues.apache.org/jira/browse/SPARK-9537) | DecisionTreeClassifierModel support probability prediction for PySpark.ml |  Minor | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-9538](https://issues.apache.org/jira/browse/SPARK-9538) | LogisticRegression support raw and probability prediction for PySpark.ml |  Minor | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8873](https://issues.apache.org/jira/browse/SPARK-8873) | Support cleaning up shuffle files when using shuffle service in Mesos |  Blocker | Mesos | Timothy Chen | Timothy Chen |
| [SPARK-9551](https://issues.apache.org/jira/browse/SPARK-9551) | add copyTo for UnsafeRow to reuse a copy buffer |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9528](https://issues.apache.org/jira/browse/SPARK-9528) | RandomForestClassifier should extend ProbabilisticClassifier |  Major | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9554](https://issues.apache.org/jira/browse/SPARK-9554) | Turn on in-memory relation partition pruning by default |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8947](https://issues.apache.org/jira/browse/SPARK-8947) | Improve expression type coercion, casting & checking |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8131](https://issues.apache.org/jira/browse/SPARK-8131) | Improve Database support |  Critical | SQL | Yin Huai | Cheng Lian |
| [SPARK-9287](https://issues.apache.org/jira/browse/SPARK-9287) | Speedup unit test of Date expressions |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-9191](https://issues.apache.org/jira/browse/SPARK-9191) | Add ml.PCA user guide and code examples |  Minor | Documentation, ML | Yanbo Liang | Yanbo Liang |
| [SPARK-8735](https://issues.apache.org/jira/browse/SPARK-8735) | Expose metrics for runtime memory usage |  Blocker | Spark Core, SQL | Andrew Or | Andrew Or |
| [SPARK-6126](https://issues.apache.org/jira/browse/SPARK-6126) | Support UDTs in JSON |  Major | SQL | Joseph K. Bradley | Nathan Howell |
| [SPARK-9534](https://issues.apache.org/jira/browse/SPARK-9534) | Enable javac lint for scalac parity; fix a lot of build warnings, 1.5.0 edition |  Minor | Build | Sean Owen | Sean Owen |
| [SPARK-9562](https://issues.apache.org/jira/browse/SPARK-9562) | Move spark-ec2 from mesos to amplab |  Major | EC2 | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8069](https://issues.apache.org/jira/browse/SPARK-8069) | Add support for cutoff to RandomForestClassifier |  Minor | ML | holdenk | holdenk |
| [SPARK-9553](https://issues.apache.org/jira/browse/SPARK-9553) | remove the createCode and createStructCode, and replace the usage of them by createStructCode |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9447](https://issues.apache.org/jira/browse/SPARK-9447) | Python RandomForestClassifier probabilityCol, rawPredictionCol |  Major | MLlib, PySpark | holdenk | Joseph K. Bradley |
| [SPARK-9582](https://issues.apache.org/jira/browse/SPARK-9582) | LDA cleanups |  Minor | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9586](https://issues.apache.org/jira/browse/SPARK-9586) | Update BinaryClassificationEvaluator to use setRawPredictionCol |  Trivial | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9598](https://issues.apache.org/jira/browse/SPARK-9598) | do not expose generic getter in internal row |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9540](https://issues.apache.org/jira/browse/SPARK-9540) | Optimize PrefixSpan implementation |  Critical | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8159](https://issues.apache.org/jira/browse/SPARK-8159) | Improve expression function coverage (Spark 1.5) |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9215](https://issues.apache.org/jira/browse/SPARK-9215) | Implement WAL-free Kinesis receiver that give at-least once guarantee |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9360](https://issues.apache.org/jira/browse/SPARK-9360) | Support BinaryType in PrefixComparators for UnsafeExternalSort |  Major | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-9628](https://issues.apache.org/jira/browse/SPARK-9628) | Rename Int and Long to SQLDate SQLTimestamp In DateTimeUtils |  Major | . | Yijie Shen | Yijie Shen |
| [SPARK-9618](https://issues.apache.org/jira/browse/SPARK-9618) | SQLContext.read.schema().parquet() ignores the supplied schema |  Minor | SQL | Nathan Howell | Nathan Howell |
| [SPARK-9519](https://issues.apache.org/jira/browse/SPARK-9519) | Confirm stop sc successfully when application was killed |  Minor | YARN | Weizhong | Weizhong |
| [SPARK-6591](https://issues.apache.org/jira/browse/SPARK-6591) | Python data source load options should auto convert common types into strings |  Major | PySpark, SQL | Reynold Xin | Yijie Shen |
| [SPARK-9674](https://issues.apache.org/jira/browse/SPARK-9674) | Remove GeneratedAggregate |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9644](https://issues.apache.org/jira/browse/SPARK-9644) | Support update DecimalType with precision \> 18 in UnsafeRow |  Critical | . | Davies Liu | Davies Liu |
| [SPARK-9533](https://issues.apache.org/jira/browse/SPARK-9533) | Add missing methods in Word2Vec ML (Python API) |  Minor | ML, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-9632](https://issues.apache.org/jira/browse/SPARK-9632) | update InternalRow.toSeq to make it accept data type info |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9641](https://issues.apache.org/jira/browse/SPARK-9641) | spark.shuffle.service.port is not documented |  Minor | Documentation, Shuffle | Thomas Graves | Sean Owen |
| [SPARK-9493](https://issues.apache.org/jira/browse/SPARK-9493) | Chain logistic regression with isotonic regression under the pipeline API |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9548](https://issues.apache.org/jira/browse/SPARK-9548) | BytesToBytesMap could have a destructive iterator |  Blocker | SQL | Josh Rosen | Liang-Chi Hsieh |
| [SPARK-9633](https://issues.apache.org/jira/browse/SPARK-9633) | SBT download locations outdated; need an update |  Minor | Build | Sean Owen | Sean Owen |
| [SPARK-4302](https://issues.apache.org/jira/browse/SPARK-4302) | Support fixed precision decimal type in JsonParser |  Minor | SQL | Yin Huai | Davies Liu |
| [SPARK-9692](https://issues.apache.org/jira/browse/SPARK-9692) | Remove SqlNewHadoopRDD's generated Tuple2 and InterruptibleIterator |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9700](https://issues.apache.org/jira/browse/SPARK-9700) | Pick default page size more intelligently |  Blocker | SQL | Davies Liu | Reynold Xin |
| [SPARK-9412](https://issues.apache.org/jira/browse/SPARK-9412) | Support records larger than a page size |  Blocker | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9667](https://issues.apache.org/jira/browse/SPARK-9667) | Remove SparkSqlSerializer2 in favor of Unsafe exchange |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9736](https://issues.apache.org/jira/browse/SPARK-9736) | JoinedRow.anyNull should delegate to the underlying rows |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9733](https://issues.apache.org/jira/browse/SPARK-9733) | Improve explain message for data source scan node |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9677](https://issues.apache.org/jira/browse/SPARK-9677) | Enable SQLQuerySuite."aggregation with codegen updates peak execution memory" |  Blocker | SQL | Reynold Xin | Andrew Or |
| [SPARK-8481](https://issues.apache.org/jira/browse/SPARK-8481) | GaussianMixtureModel predict accepting single vector |  Minor | MLlib | Dariusz Kobylarz | Dariusz Kobylarz |
| [SPARK-8160](https://issues.apache.org/jira/browse/SPARK-8160) | Tungsten style external aggregation |  Major | SQL | Reynold Xin | Yin Huai |
| [SPARK-9756](https://issues.apache.org/jira/browse/SPARK-9756) | Make auxillary constructors for ML decision trees private |  Minor | ML | Feynman Liang | Feynman Liang |
| [SPARK-9738](https://issues.apache.org/jira/browse/SPARK-9738) | remove FromUnsafe and add its codegen version to GenerateSafe |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-4561](https://issues.apache.org/jira/browse/SPARK-4561) | PySparkSQL's Row.asDict() should convert nested rows to dictionaries |  Major | PySpark, SQL | Josh Rosen | Davies Liu |
| [SPARK-9486](https://issues.apache.org/jira/browse/SPARK-9486) | Add aliasing to data sources to allow external packages to register themselves with Spark |  Minor | SQL | Joseph Batchik | Joseph Batchik |
| [SPARK-9737](https://issues.apache.org/jira/browse/SPARK-9737) | Add the suggested configuration when required executor memory is above the max threshold of this cluster on YARN mode |  Trivial | YARN | Yadong Qi | Yadong Qi |
| [SPARK-9703](https://issues.apache.org/jira/browse/SPARK-9703) | EnsureRequirements should not add unnecessary shuffles when only ordering requirements are unsatisfied |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9759](https://issues.apache.org/jira/browse/SPARK-9759) | Improve performance of Decimal.times() and casting from integral |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-9076](https://issues.apache.org/jira/browse/SPARK-9076) | Improve NaN value handling |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9727](https://issues.apache.org/jira/browse/SPARK-9727) | Make the Kinesis project SBT name and consistent with other streaming projects |  Minor | Build | Tathagata Das | Tathagata Das |
| [SPARK-9815](https://issues.apache.org/jira/browse/SPARK-9815) | Rename PlatformDependent.UNSAFE -\> Platform |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9572](https://issues.apache.org/jira/browse/SPARK-9572) | Add StreamingContext.getActiveOrCreate() to python API |  Major | DStreams, PySpark | Tathagata Das | Tathagata Das |
| [SPARK-9814](https://issues.apache.org/jira/browse/SPARK-9814) | EqualNullSafe not passing to data sources |  Minor | SQL | Hyukjin Kwon | Hyukjin Kwon |
| [SPARK-9788](https://issues.apache.org/jira/browse/SPARK-9788) | LDA docConcentration, gammaShape 1.5 binary incompatibility fixes |  Major | MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-8625](https://issues.apache.org/jira/browse/SPARK-8625) | Propagate user exceptions in tasks back to driver |  Major | Spark Core | Tom White | Tom White |
| [SPARK-9693](https://issues.apache.org/jira/browse/SPARK-9693) | Reserve a page in all unsafe operators to avoid starving an operator |  Blocker | SQL | Andrew Or | Andrew Or |
| [SPARK-9847](https://issues.apache.org/jira/browse/SPARK-9847) | ML Params copyValues should copy default values to default map, not set map |  Critical | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9766](https://issues.apache.org/jira/browse/SPARK-9766) | check and add missing docs for PySpark ML |  Major | ML, MLlib | Yanbo Liang | Yanbo Liang |
| [SPARK-9789](https://issues.apache.org/jira/browse/SPARK-9789) | Reinstate LogisticRegression threshold Param |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9092](https://issues.apache.org/jira/browse/SPARK-9092) | Make --num-executors compatible with dynamic allocation |  Major | YARN | Niranjan Padmanabhan | Niranjan Padmanabhan |
| [SPARK-9913](https://issues.apache.org/jira/browse/SPARK-9913) | LDAUtils should be private |  Trivial | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9909](https://issues.apache.org/jira/browse/SPARK-9909) | Move weightCol to sharedParams |  Minor | ML | holdenk | holdenk |
| [SPARK-9912](https://issues.apache.org/jira/browse/SPARK-9912) | QRDecomposition should use QType and RType for type names instead of UType and VType |  Trivial | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9915](https://issues.apache.org/jira/browse/SPARK-9915) | StopWordsRemover.stopWords should use StringArrayParam |  Trivial | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9199](https://issues.apache.org/jira/browse/SPARK-9199) | Upgrade Tachyon dependency to 0.7.0 |  Major | Spark Core | Calvin Jia | Calvin Jia |
| [SPARK-9704](https://issues.apache.org/jira/browse/SPARK-9704) | Make some ML APIs public: VectorUDT, Identifiable, ProbabilisticClassifier |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9903](https://issues.apache.org/jira/browse/SPARK-9903) | Skip local processing in PrefixSpan if there are no small prefixes |  Major | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9917](https://issues.apache.org/jira/browse/SPARK-9917) | MinMaxScaler missing getters and docs |  Trivial | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9918](https://issues.apache.org/jira/browse/SPARK-9918) | Remove runs from KMeans under the pipeline API |  Major | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9914](https://issues.apache.org/jira/browse/SPARK-9914) | RFormula are missing setters for featuresCol and labelCol |  Trivial | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9922](https://issues.apache.org/jira/browse/SPARK-9922) | Rename StringIndexerInverse to IndexToString |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8744](https://issues.apache.org/jira/browse/SPARK-8744) | StringIndexerModel should have public constructor |  Trivial | ML | Joseph K. Bradley | holdenk |
| [SPARK-9934](https://issues.apache.org/jira/browse/SPARK-9934) | Deprecate NIO ConnectionManager |  Major | Spark Core | Reynold Xin | Reynold Xin |
| [SPARK-10068](https://issues.apache.org/jira/browse/SPARK-10068) | Add links to sections in MLlib's user guide |  Minor | . | Feynman Liang | Feynman Liang |
| [SPARK-9768](https://issues.apache.org/jira/browse/SPARK-9768) | Add Python API for ml.feature.ElementwiseProduct |  Minor | ML, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-10076](https://issues.apache.org/jira/browse/SPARK-10076) | make MultilayerPerceptronClassifier layers and weights public |  Major | ML | Yanbo Liang | Yanbo Liang |
| [SPARK-10085](https://issues.apache.org/jira/browse/SPARK-10085) | unnecessary array import in Python MLLib linear models |  Minor | Documentation, MLlib, PySpark | Piotr Migdał | Piotr Migdał |
| [SPARK-10088](https://issues.apache.org/jira/browse/SPARK-10088) | Support "stored as avro" HiveQL construct |  Minor | SQL | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-10095](https://issues.apache.org/jira/browse/SPARK-10095) | Should not use the private field of BigInteger |  Minor | SQL | Davies Liu | Davies Liu |
| [SPARK-9952](https://issues.apache.org/jira/browse/SPARK-9952) | Fix N^2 loop when DAGScheduler.getPreferredLocsInternal accesses cacheLocs |  Critical | Scheduler | Josh Rosen | Josh Rosen |
| [SPARK-10099](https://issues.apache.org/jira/browse/SPARK-10099) | Use @deprecated instead of @Deprecated in Scala code |  Trivial | DStreams, Spark Core | Xiangrui Meng | Tathagata Das |
| [SPARK-10070](https://issues.apache.org/jira/browse/SPARK-10070) | Remove Guava dependencies in user guides |  Minor | Documentation, ML, MLlib | Feynman Liang | Sean Owen |
| [SPARK-9977](https://issues.apache.org/jira/browse/SPARK-9977) | The usage of a label generated by StringIndexer |  Trivial | Documentation | Kai Sasaki | Kai Sasaki |
| [SPARK-8949](https://issues.apache.org/jira/browse/SPARK-8949) | Remove references to preferredNodeLocalityData in javadoc and print warning when used |  Critical | Spark Core, YARN | Patrick Wendell | Han JU |
| [SPARK-10097](https://issues.apache.org/jira/browse/SPARK-10097) | ML Evaluator should indicate if metric should be maximized or minimized |  Major | ML | Joseph K. Bradley | Feynman Liang |
| [SPARK-9981](https://issues.apache.org/jira/browse/SPARK-9981) | Make labels public in StringIndexerModel |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-6489](https://issues.apache.org/jira/browse/SPARK-6489) | Optimize lateral view with explode to not read unnecessary columns |  Major | SQL | Konstantin Shaposhnikov | Wenchen Fan |
| [SPARK-10140](https://issues.apache.org/jira/browse/SPARK-10140) | Add target fields to @Since annotation |  Major | Documentation | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10163](https://issues.apache.org/jira/browse/SPARK-10163) | Allow single-category features for GBT models |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-10178](https://issues.apache.org/jira/browse/SPARK-10178) | HiveComparision test should print out dependent tables |  Major | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-10137](https://issues.apache.org/jira/browse/SPARK-10137) | Avoid to restart receivers if scheduleReceivers returns balanced results |  Blocker | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9293](https://issues.apache.org/jira/browse/SPARK-9293) | Analysis should detect when set operations are performed on tables with different numbers of columns |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-6196](https://issues.apache.org/jira/browse/SPARK-6196) | Add MAPR 4.0.2 support to the build |  Minor | Build | Trystan Leftwich | Sean Owen |
| [SPARK-10230](https://issues.apache.org/jira/browse/SPARK-10230) | LDA public API should use docConcentration |  Minor | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-10295](https://issues.apache.org/jira/browse/SPARK-10295) | Dynamic allocation in Mesos does not release when RDDs are cached |  Minor | Documentation, Spark Core | Hans van den Bogert | Sean Owen |
| [SPARK-10344](https://issues.apache.org/jira/browse/SPARK-10344) | Add tests for extraStrategies |  Major | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-1564](https://issues.apache.org/jira/browse/SPARK-1564) | Add JavaScript into Javadoc to turn ::Experimental:: and such into badges |  Minor | Documentation | Matei Zaharia | Deron Eriksson |
| [SPARK-10348](https://issues.apache.org/jira/browse/SPARK-10348) | Improve Spark ML user guide |  Major | Documentation, ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10331](https://issues.apache.org/jira/browse/SPARK-10331) | Update user guide to address minor comments during code review |  Major | Documentation, ML, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10354](https://issues.apache.org/jira/browse/SPARK-10354) | First cost RDD shouldn't be cached in k-means\|\| and the following cost RDD should use MEMORY\_AND\_DISK |  Minor | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10148](https://issues.apache.org/jira/browse/SPARK-10148) | Display active and inactive receiver numbers in Streaming page |  Minor | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-2660](https://issues.apache.org/jira/browse/SPARK-2660) | Enable pretty-printing SchemaRDD Rows |  Major | SQL | Aaron Davidson | Michael Armbrust |
| [SPARK-2695](https://issues.apache.org/jira/browse/SPARK-2695) | Figure out a good way to handle NullType columns. |  Major | SQL | Yin Huai | Michael Armbrust |
| [SPARK-3700](https://issues.apache.org/jira/browse/SPARK-3700) | Improve the performance of scanning JSON datasets |  Major | SQL | Yin Huai | YBL |
| [SPARK-4273](https://issues.apache.org/jira/browse/SPARK-4273) | Providing ExternalSet to avoid OOM when count(distinct) |  Minor | Spark Core, SQL | YanTang Zhai | Michael Armbrust |
| [SPARK-6632](https://issues.apache.org/jira/browse/SPARK-6632) | Optimize the parquetSchema to metastore schema reconciliation, so that the process is delegated to each map task itself |  Major | SQL | Yash Datta | Michael Armbrust |
| [SPARK-6001](https://issues.apache.org/jira/browse/SPARK-6001) | K-Means clusterer should return the assignments of input points to clusters |  Minor | MLlib | Derrick Burns | Yu Ishikawa |
| [SPARK-8144](https://issues.apache.org/jira/browse/SPARK-8144) | For PySpark SQL, automatically convert values provided in readwriter options to string |  Major | PySpark, SQL | Joseph K. Bradley | Yijie Shen |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-7515](https://issues.apache.org/jira/browse/SPARK-7515) | Update documentation for PySpark on YARN with cluster mode |  Minor | Documentation | Kousuke Saruta | Kousuke Saruta |
| [SPARK-7635](https://issues.apache.org/jira/browse/SPARK-7635) | SparkContextSchedulerCreationSuite tests may fail due to unrecognized UnsatisfiedLinkError message. |  Minor | Spark Core | Matthew Brandyberry | Tim Ellison |
| [SPARK-7063](https://issues.apache.org/jira/browse/SPARK-7063) | Update lz4 for Java 7 to avoid: when lz4 compression is used, it causes core dump |  Minor | Spark Core | Jenny MA | Jenny MA |
| [SPARK-6246](https://issues.apache.org/jira/browse/SPARK-6246) | spark-ec2 can't handle clusters with \> 100 nodes |  Minor | EC2 | Nicholas Chammas | Alex Slusarenko |
| [SPARK-7775](https://issues.apache.org/jira/browse/SPARK-7775) | YARN AM tried to sleep negative milliseconds |  Critical | YARN | Andrew Or | Andrew Or |
| [SPARK-7811](https://issues.apache.org/jira/browse/SPARK-7811) | Fix typo on slf4j configuration on metrics.properties.template |  Trivial | Spark Core | Judy Nash | Judy Nash |
| [SPARK-7863](https://issues.apache.org/jira/browse/SPARK-7863) | SimpleDateParam should not use SimpleDateFormat in multiple threads because SimpleDateFormat is not thread-safe |  Minor | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-7846](https://issues.apache.org/jira/browse/SPARK-7846) | Use different way to pass spark.yarn.keytab and spark.yarn.principal in different modes |  Major | YARN | Tao Wang | Tao Wang |
| [SPARK-7964](https://issues.apache.org/jira/browse/SPARK-7964) | The BooleanCasts rule in HiveTypeCoercion is useless |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7717](https://issues.apache.org/jira/browse/SPARK-7717) | Spark Standalone Web UI showing incorrect total memory, workers and cores |  Minor | Web UI | Swaranga Sarma | zhichao-li |
| [SPARK-8043](https://issues.apache.org/jira/browse/SPARK-8043) | update NaiveBayes and SVM examples in doc |  Minor | MLlib | yuhao yang | yuhao yang |
| [SPARK-8032](https://issues.apache.org/jira/browse/SPARK-8032) | Make NumPy version checking in mllib/\_\_init\_\_.py |  Major | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-6444](https://issues.apache.org/jira/browse/SPARK-6444) | SQL functions (either built-in or UDF) should check for data types of their arguments |  Major | SQL | Cheng Lian | Wenchen Fan |
| [SPARK-8063](https://issues.apache.org/jira/browse/SPARK-8063) | Spark master URL conflict between MASTER env variable and --master command line option |  Major | SparkR | Sun Rui | Sun Rui |
| [SPARK-8083](https://issues.apache.org/jira/browse/SPARK-8083) | Fix return to drivers link in Mesos driver page |  Major | Mesos, Web UI | Timothy Chen | Timothy Chen |
| [SPARK-8051](https://issues.apache.org/jira/browse/SPARK-8051) | StringIndexerModel (and other models) shouldn't complain if the input column is missing. |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8088](https://issues.apache.org/jira/browse/SPARK-8088) | ExecutionAllocationManager spamming INFO logs about "Lowering target number of executors" |  Major | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-7956](https://issues.apache.org/jira/browse/SPARK-7956) | Use Janino to compile SQL expression |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8098](https://issues.apache.org/jira/browse/SPARK-8098) | Show correct length of bytes on log page |  Minor | Web UI | Carson Wang | Carson Wang |
| [SPARK-8085](https://issues.apache.org/jira/browse/SPARK-8085) | Pass in user-specified schema in read.df |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8099](https://issues.apache.org/jira/browse/SPARK-8099) | In yarn-cluster mode, "--executor-cores" can't be setted into SparkConf |  Major | YARN | meiyoula | meiyoula |
| [SPARK-8112](https://issues.apache.org/jira/browse/SPARK-8112) | Received block event count through the StreamingListener can be negative |  Minor | DStreams | Tathagata Das | Shixiong Zhu |
| [SPARK-6973](https://issues.apache.org/jira/browse/SPARK-6973) | The total stages on the allJobsPage is wrong |  Minor | Web UI | meiyoula | meiyoula |
| [SPARK-8079](https://issues.apache.org/jira/browse/SPARK-8079) | NPE when HadoopFsRelation.prepareForWriteJob throws exception |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8136](https://issues.apache.org/jira/browse/SPARK-8136) | AM link download test can be flaky |  Major | Tests, YARN | Hari Shreedharan | Hari Shreedharan |
| [SPARK-8004](https://issues.apache.org/jira/browse/SPARK-8004) | Spark does not enclose column names when fetchting from jdbc sources |  Major | SQL | Rene Treffer | Liang-Chi Hsieh |
| [SPARK-7939](https://issues.apache.org/jira/browse/SPARK-7939) | Make URL partition recognition return String by default for all partition column types and values |  Major | SQL | Jianshi Huang | Liang-Chi Hsieh |
| [SPARK-8116](https://issues.apache.org/jira/browse/SPARK-8116) | sc.range() doesn't match python range() |  Minor | PySpark | Ted Blackman | Ted Blackman |
| [SPARK-8162](https://issues.apache.org/jira/browse/SPARK-8162) | Run spark-shell cause NullPointerException |  Blocker | Build, Spark Shell | Weizhong | Andrew Or |
| [SPARK-7955](https://issues.apache.org/jira/browse/SPARK-7955) | Dynamic allocation: longer timeout for executors with cached blocks |  Major | Spark Core | Hari Shreedharan | Hari Shreedharan |
| [SPARK-7792](https://issues.apache.org/jira/browse/SPARK-7792) | HiveContext registerTempTable not thread safe |  Major | SQL | Yana Kadiyska | Navis |
| [SPARK-6419](https://issues.apache.org/jira/browse/SPARK-6419) | GenerateOrdering does not support BinaryType and complex types. |  Major | SQL | Yin Huai | Davies Liu |
| [SPARK-7527](https://issues.apache.org/jira/browse/SPARK-7527) | Wrong detection of REPL mode in ClosureCleaner |  Minor | Spark Core | Oleksii Kostyliev | Shixiong Zhu |
| [SPARK-5479](https://issues.apache.org/jira/browse/SPARK-5479) | PySpark on yarn mode need to support non-local python files |  Major | PySpark, YARN | Lianhui Wang | Marcelo Vanzin |
| [SPARK-8290](https://issues.apache.org/jira/browse/SPARK-8290) | spark class command builder need read SPARK\_JAVA\_OPTS and SPARK\_DRIVER\_MEMORY properly |  Minor | Spark Core | Tao Wang | Tao Wang |
| [SPARK-8200](https://issues.apache.org/jira/browse/SPARK-8200) | Exception in StreamingLinearAlgorithm on Stream with Empty RDD. |  Minor | DStreams, MLlib | Paavo Parkkinen | Paavo Parkkinen |
| [SPARK-8285](https://issues.apache.org/jira/browse/SPARK-8285) | CombineSum should be calculated as unlimited decimal first |  Trivial | SQL | Navis | Navis |
| [SPARK-8289](https://issues.apache.org/jira/browse/SPARK-8289) | Provide a specific stack size with all Java implementations to prevent stack overflows with certain tests |  Major | Tests | Adam Roberts | Adam Roberts |
| [SPARK-6411](https://issues.apache.org/jira/browse/SPARK-6411) | PySpark DataFrames can't be created if any datetimes have timezones |  Major | PySpark, SQL | Harry Brundage | Davies Liu |
| [SPARK-8305](https://issues.apache.org/jira/browse/SPARK-8305) | Improve codegen |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8310](https://issues.apache.org/jira/browse/SPARK-8310) | Spark EC2 branch in 1.4 is wrong |  Critical | EC2 | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-7915](https://issues.apache.org/jira/browse/SPARK-7915) | Support specifying the column list for target table in CTAS |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-8322](https://issues.apache.org/jira/browse/SPARK-8322) | EC2 script not fully updated for 1.4.0 release |  Major | EC2 | Mark Smith | Mark Smith |
| [SPARK-8329](https://issues.apache.org/jira/browse/SPARK-8329) | DataSource options parser no longer accepts '\_' |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8052](https://issues.apache.org/jira/browse/SPARK-8052) | Hive on Spark: CAST string AS BIGINT produces wrong value |  Major | . | Andrey Kurochkin | Liang-Chi Hsieh |
| [SPARK-8342](https://issues.apache.org/jira/browse/SPARK-8342) | Decimal Math beyond ~2^112 is broken |  Major | SQL | Rene Treffer | Liang-Chi Hsieh |
| [SPARK-8354](https://issues.apache.org/jira/browse/SPARK-8354) | Fix off-by-factor-of-8 error when allocating scratch space in UnsafeFixedWidthAggregationMap |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8358](https://issues.apache.org/jira/browse/SPARK-8358) | DataFrame explode with alias and \* fails |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8350](https://issues.apache.org/jira/browse/SPARK-8350) | R unit tests output should be logged to "unit-tests.log" |  Minor | SparkR | Andrew Or | Andrew Or |
| [SPARK-8336](https://issues.apache.org/jira/browse/SPARK-8336) | Fix NullPointerException with functions.rand() |  Major | SQL | Ted Yu | Ted Yu |
| [SPARK-8367](https://issues.apache.org/jira/browse/SPARK-8367) | ReliableKafka will loss data when \`spark.streaming.blockInterval\` was 0 |  Major | DStreams | carlmartin | carlmartin |
| [SPARK-8156](https://issues.apache.org/jira/browse/SPARK-8156) | Respect current database when creating datasource tables |  Major | SQL | baishuo | baishuo |
| [SPARK-8309](https://issues.apache.org/jira/browse/SPARK-8309) | OpenHashMap doesn't work with more than 12M items |  Critical | Spark Core | Vyacheslav Baranov | Vyacheslav Baranov |
| [SPARK-8010](https://issues.apache.org/jira/browse/SPARK-8010) | Implict promote Numeric type to String type in HiveTypeCoercion |  Major | SQL | OopsOutOfMemory | OopsOutOfMemory |
| [SPARK-8161](https://issues.apache.org/jira/browse/SPARK-8161) | externalBlockStoreInitialized is never set to be true |  Major | Block Manager | shimingfei | shimingfei |
| [SPARK-8373](https://issues.apache.org/jira/browse/SPARK-8373) | When an RDD has no partition, Python sum will throw "Can not reduce() empty RDD" |  Minor | PySpark | Shixiong Zhu | Shixiong Zhu |
| [SPARK-7067](https://issues.apache.org/jira/browse/SPARK-7067) | Can't resolve nested column in ORDER BY |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8306](https://issues.apache.org/jira/browse/SPARK-8306) | AddJar command needs to set the new class loader to the HiveConf inside executionHive.state. |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8202](https://issues.apache.org/jira/browse/SPARK-8202) | PySpark: infinite loop during external sort |  Critical | PySpark | Davies Liu | Davies Liu |
| [SPARK-8376](https://issues.apache.org/jira/browse/SPARK-8376) | Commons Lang 3 is one of the required JAR of Spark Flume Sink but is missing in the docs |  Minor | Documentation | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8080](https://issues.apache.org/jira/browse/SPARK-8080) | Custom Receiver.store with Iterator type do not give correct count at Spark UI |  Minor | DStreams, Web UI | Dibyendu Bhattacharya | Dibyendu Bhattacharya |
| [SPARK-8339](https://issues.apache.org/jira/browse/SPARK-8339) | Itertools islice requires an integer for the stop argument. |  Minor | PySpark | Kevin Conor | Kevin Conor |
| [SPARK-8151](https://issues.apache.org/jira/browse/SPARK-8151) | Pipeline components should correctly implement copy |  Blocker | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8123](https://issues.apache.org/jira/browse/SPARK-8123) | Bucketizer must implement copy |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8150](https://issues.apache.org/jira/browse/SPARK-8150) | IDFModel must implement copy |  Major | ML | Joseph K. Bradley | Xiangrui Meng |
| [SPARK-8087](https://issues.apache.org/jira/browse/SPARK-8087) | PipelineModel.copy didn't copy the stages |  Blocker | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8476](https://issues.apache.org/jira/browse/SPARK-8476) | Setters inc/decDiskBytesSpilled in TaskMetrics should also be private. |  Minor | Spark Core | Takuya Ueshin | Takuya Ueshin |
| [SPARK-7180](https://issues.apache.org/jira/browse/SPARK-7180) | SerializationDebugger fails with ArrayOutOfBoundsException |  Major | Spark Core | Andrew Or | Tathagata Das |
| [SPARK-8090](https://issues.apache.org/jira/browse/SPARK-8090) | SerializationDebugger does not handle classes with writeReplace correctly |  Major | Spark Core | Tathagata Das | Tathagata Das |
| [SPARK-8091](https://issues.apache.org/jira/browse/SPARK-8091) | SerializationDebugger does not handle classes with writeObject method |  Major | Spark Core | Tathagata Das | Tathagata Das |
| [SPARK-8451](https://issues.apache.org/jira/browse/SPARK-8451) | SparkSubmitSuite never checks for process exit code |  Major | Spark Submit, Tests | Andrew Or | Andrew Or |
| [SPARK-8368](https://issues.apache.org/jira/browse/SPARK-8368) | ClassNotFoundException in closure for map |  Blocker | SQL | CHEN Zhiwei | Yin Huai |
| [SPARK-8461](https://issues.apache.org/jira/browse/SPARK-8461) | ClassNotFoundException when code generation is enabled |  Blocker | SQL | Cheng Lian | Davies Liu |
| [SPARK-8452](https://issues.apache.org/jira/browse/SPARK-8452) | expose jobGroup API in SparkR |  Major | SparkR | Hossein Falaki | Hossein Falaki |
| [SPARK-8093](https://issues.apache.org/jira/browse/SPARK-8093) | Spark 1.4 branch's new JSON schema inference has changed the behavior of handling inner empty JSON object. |  Critical | SQL | Harish Butani | Nathan Howell |
| [SPARK-8489](https://issues.apache.org/jira/browse/SPARK-8489) | Add regression tests for SPARK-8470 |  Critical | SQL, Tests | Andrew Or | Andrew Or |
| [SPARK-8468](https://issues.apache.org/jira/browse/SPARK-8468) | Cross-validation with RegressionEvaluator prefers higher RMSE |  Blocker | ML | Chelsea Zhang | Liang-Chi Hsieh |
| [SPARK-8379](https://issues.apache.org/jira/browse/SPARK-8379) | LeaseExpiredException when using dynamic partition with speculative execution |  Major | SQL | jeanlyn | jeanlyn |
| [SPARK-8406](https://issues.apache.org/jira/browse/SPARK-8406) | Race condition when writing Parquet files |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8420](https://issues.apache.org/jira/browse/SPARK-8420) | Inconsistent behavior with Dataframe Timestamp between 1.3.1 and 1.4.0 |  Blocker | SQL | Justin Yip | Michael Armbrust |
| [SPARK-8104](https://issues.apache.org/jira/browse/SPARK-8104) | move the auto alias logic into Analyzer |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8532](https://issues.apache.org/jira/browse/SPARK-8532) | In Python's DataFrameWriter, save/saveAsTable/json/parquet/jdbc always override mode |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-7153](https://issues.apache.org/jira/browse/SPARK-7153) | support Long type ordinal in GetItem |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7859](https://issues.apache.org/jira/browse/SPARK-7859) | Collect\_SET behaves different under different version of JDK |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-7781](https://issues.apache.org/jira/browse/SPARK-7781) | GradientBoostedTrees is missing maxBins parameter in pyspark |  Major | MLlib | Don Drake | holdenk |
| [SPARK-8483](https://issues.apache.org/jira/browse/SPARK-8483) | Remove commons-lang3 depedency from flume-sink |  Major | DStreams | Hari Shreedharan | Hari Shreedharan |
| [SPARK-8432](https://issues.apache.org/jira/browse/SPARK-8432) | Fix hashCode and equals() of BinaryType in Row |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8525](https://issues.apache.org/jira/browse/SPARK-8525) | Bug in Streaming k-means documentation |  Minor | Documentation, MLlib | Oleksiy Dyagilev | Oleksiy Dyagilev |
| [SPARK-8049](https://issues.apache.org/jira/browse/SPARK-8049) | OneVsRest's output includes a temp column |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8578](https://issues.apache.org/jira/browse/SPARK-8578) | Should ignore user defined output committer when appending data |  Major | SQL | Cheng Lian | Yin Huai |
| [SPARK-8095](https://issues.apache.org/jira/browse/SPARK-8095) | Spark package dependencies not resolved when package is in local-ivy-cache |  Major | Spark Submit | Eron Wright | Burak Yavuz |
| [SPARK-8506](https://issues.apache.org/jira/browse/SPARK-8506) | SparkR does not provide an easy way to depend on Spark Packages when performing init from inside of R |  Minor | SparkR | holdenk | holdenk |
| [SPARK-8399](https://issues.apache.org/jira/browse/SPARK-8399) | Overlap between histograms and axis' name in Spark Streaming UI |  Minor | DStreams, Web UI | Benjamin Fradet | Benjamin Fradet |
| [SPARK-7088](https://issues.apache.org/jira/browse/SPARK-7088) | [REGRESSION] Spark 1.3.1 breaks analysis of third-party logical plans |  Critical | SQL | Santiago M. Mola | Santiago M. Mola |
| [SPARK-8558](https://issues.apache.org/jira/browse/SPARK-8558) | Script /dev/run-tests fails when \_JAVA\_OPTIONS env var set |  Minor | Build, Tests | Oleksiy Dyagilev | Oleksiy Dyagilev |
| [SPARK-8604](https://issues.apache.org/jira/browse/SPARK-8604) | Parquet data source doesn't write summary file while doing appending |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8637](https://issues.apache.org/jira/browse/SPARK-8637) | Packages argument is wrong in sparkR.init |  Blocker | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8652](https://issues.apache.org/jira/browse/SPARK-8652) | PySpark tests sometimes forget to check return status of doctest.testmod(), masking failing tests |  Blocker | PySpark, Tests | Josh Rosen | Josh Rosen |
| [SPARK-8662](https://issues.apache.org/jira/browse/SPARK-8662) | [SparkR] SparkSQL tests fail in R 3.2 |  Major | SparkR | Chris Freeman | Chris Freeman |
| [SPARK-8607](https://issues.apache.org/jira/browse/SPARK-8607) | SparkR - Third party jars are not being added to classpath in SparkRBackend |  Critical | SparkR | Chris Freeman | Chris Freeman |
| [SPARK-8623](https://issues.apache.org/jira/browse/SPARK-8623) | Hadoop RDDs fail to properly serialize configuration |  Major | Spark Core | Bolke de Bruin | Sandy Ryza |
| [SPARK-8606](https://issues.apache.org/jira/browse/SPARK-8606) | Exceptions in RDD.getPreferredLocations() and getPartitions() should not be able to crash DAGScheduler |  Critical | Scheduler | Josh Rosen | Josh Rosen |
| [SPARK-8683](https://issues.apache.org/jira/browse/SPARK-8683) | Depend on mockito-core instead of mockito-all |  Major | Build | Josh Rosen | Josh Rosen |
| [SPARK-8649](https://issues.apache.org/jira/browse/SPARK-8649) | Mapr repository is not defined properly |  Trivial | Build | Ashok Kumar | Ashok Kumar |
| [SPARK-8554](https://issues.apache.org/jira/browse/SPARK-8554) | Add the SparkR document files to \`.rat-excludes\` for \`./dev/check-license\` |  Major | SparkR, Tests | Yu Ishikawa | Yu Ishikawa |
| [SPARK-7862](https://issues.apache.org/jira/browse/SPARK-7862) | Query would hang when the using script has error output in SparkSQL |  Major | SQL | zhichao-li | Cheng Hao |
| [SPARK-8709](https://issues.apache.org/jira/browse/SPARK-8709) | Exclude hadoop-client's mockito-all dependency to fix test compilation break for Hadoop 2 |  Major | . | Josh Rosen | Josh Rosen |
| [SPARK-8710](https://issues.apache.org/jira/browse/SPARK-8710) | ScalaReflection.mirror should be a def |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-7287](https://issues.apache.org/jira/browse/SPARK-7287) | Flaky test: o.a.s.deploy.SparkSubmitSuite --packages |  Critical | Tests | Andrew Or | Yin Huai |
| [SPARK-8410](https://issues.apache.org/jira/browse/SPARK-8410) | Hive VersionsSuite RuntimeException |  Minor | SQL | Josiah Samuel Sathiadass | Burak Yavuz |
| [SPARK-8669](https://issues.apache.org/jira/browse/SPARK-8669) | Parquet 1.7 files that store binary enums crash when inferring schema |  Major | SQL | Steven She | Steven She |
| [SPARK-8031](https://issues.apache.org/jira/browse/SPARK-8031) | Version number written to Hive metastore is "0.13.1aa" instead of "0.13.1a" |  Trivial | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8650](https://issues.apache.org/jira/browse/SPARK-8650) | Use the user-specified app name priority in SparkSQLCLIDriver or HiveThriftServer2 |  Major | SQL | Yadong Qi | Yadong Qi |
| [SPARK-8680](https://issues.apache.org/jira/browse/SPARK-8680) | PropagateTypes is very slow when there are lots of columns |  Major | SQL | Davies Liu | Liang-Chi Hsieh |
| [SPARK-8592](https://issues.apache.org/jira/browse/SPARK-8592) | CoarseGrainedExecutorBackend: Cannot register with driver =\> NPE |  Minor | Scheduler, Spark Core | Sjoerd Mulder | Xu Chen |
| [SPARK-8437](https://issues.apache.org/jira/browse/SPARK-8437) | Using directory path without wildcard for filename slow for large number of files with wholeTextFiles and binaryFiles |  Minor | Input/Output | Ewan Leith | Sean Owen |
| [SPARK-8678](https://issues.apache.org/jira/browse/SPARK-8678) | Default values in Pipeline API should be immutable |  Major | ML, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8619](https://issues.apache.org/jira/browse/SPARK-8619) | Can't find the keytab file when recovering the streaming application. |  Major | DStreams | carlmartin | carlmartin |
| [SPARK-6785](https://issues.apache.org/jira/browse/SPARK-6785) | DateUtils can not handle date before 1970/01/01 correctly |  Major | SQL | Davies Liu | Christian Kadner |
| [SPARK-8628](https://issues.apache.org/jira/browse/SPARK-8628) | Race condition in AbstractSparkSQLParser.parse |  Critical | SQL | Santiago M. Mola | Vinod KC |
| [SPARK-8560](https://issues.apache.org/jira/browse/SPARK-8560) | Executors page displays negative active tasks |  Major | Spark Core, Web UI | meiyoula | meiyoula |
| [SPARK-2645](https://issues.apache.org/jira/browse/SPARK-2645) | Spark driver calls System.exit(50) after calling SparkContext.stop() the second time |  Major | Spark Core | Vlad Komarov | Rekha Joshi |
| [SPARK-8372](https://issues.apache.org/jira/browse/SPARK-8372) | History server shows incorrect information for application not started |  Minor | Deploy, Web UI | Carson Wang | Marcelo Vanzin |
| [SPARK-8736](https://issues.apache.org/jira/browse/SPARK-8736) | GBTRegressionModel thresholds prediction but should not |  Critical | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8739](https://issues.apache.org/jira/browse/SPARK-8739) | Illegal character \`\\r\` can be contained in StagePage. |  Major | Web UI, Windows | Kousuke Saruta | Kousuke Saruta |
| [SPARK-8563](https://issues.apache.org/jira/browse/SPARK-8563) | Bug that IndexedRowMatrix.computeSVD() yields the U with wrong numCols |  Major | MLlib | 19 Lee | 19 Lee |
| [SPARK-8738](https://issues.apache.org/jira/browse/SPARK-8738) | Generate better error message in Python for AnalysisException |  Major | . | Davies Liu | Davies Liu |
| [SPARK-8535](https://issues.apache.org/jira/browse/SPARK-8535) | PySpark : Can't create DataFrame from Pandas dataframe with no explicit column name |  Major | PySpark | Christophe Bourguignat | Yuri Saito |
| [SPARK-8750](https://issues.apache.org/jira/browse/SPARK-8750) | Remove the closure in functions.callUdf |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8763](https://issues.apache.org/jira/browse/SPARK-8763) | executing run-tests.py with Python 2.6 fails with absence of subprocess.check\_output function |  Major | PySpark | Tomohiko K. | Tomohiko K. |
| [SPARK-8308](https://issues.apache.org/jira/browse/SPARK-8308) | add missing save load for python doc example and tune down MatrixFactorization iterations |  Minor | MLlib | yuhao yang | yuhao yang |
| [SPARK-7820](https://issues.apache.org/jira/browse/SPARK-7820) | Java8-tests suite compile error under SBT |  Critical | Build, DStreams | Saisai Shao | Saisai Shao |
| [SPARK-8754](https://issues.apache.org/jira/browse/SPARK-8754) | YarnClientSchedulerBackend doesn't stop gracefully in failure conditions |  Minor | YARN | Devaraj K | Devaraj K |
| [SPARK-8688](https://issues.apache.org/jira/browse/SPARK-8688) | Hadoop Configuration has to disable client cache when writing or reading delegation tokens. |  Major | YARN | carlmartin | carlmartin |
| [SPARK-8687](https://issues.apache.org/jira/browse/SPARK-8687) | Spark on yarn-client mode can't send \`spark.yarn.credentials.file\` to executor. |  Major | YARN | carlmartin | carlmartin |
| [SPARK-8746](https://issues.apache.org/jira/browse/SPARK-8746) | Need to update download link for Hive 0.13.1 jars (HiveComparisonTest) |  Trivial | SQL | Christian Kadner | Christian Kadner |
| [SPARK-8747](https://issues.apache.org/jira/browse/SPARK-8747) | fix EqualNullSafe for binary type |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8581](https://issues.apache.org/jira/browse/SPARK-8581) | Simplify and clean up the checkpointing code |  Minor | Spark Core | Andrew Or | Andrew Or |
| [SPARK-8584](https://issues.apache.org/jira/browse/SPARK-8584) | Better exception message if invalid checkpoint dir is specified |  Major | Spark Core | Andrew Or | Andrew Or |
| [SPARK-8781](https://issues.apache.org/jira/browse/SPARK-8781) | Published POMs are no longer effective POMs |  Blocker | Build | Konstantin Shaposhnikov | Andrew Or |
| [SPARK-7835](https://issues.apache.org/jira/browse/SPARK-7835) | Refactor HeartbeatReceiverSuite for coverage and clean up |  Major | Spark Core, Tests | Andrew Or | Andrew Or |
| [SPARK-8803](https://issues.apache.org/jira/browse/SPARK-8803) | Crosstab element's can't contain null's and back ticks |  Major | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8572](https://issues.apache.org/jira/browse/SPARK-8572) | Type coercion for ScalaUDFs |  Critical | SQL | Yin Huai | Cheolsoo Park |
| [SPARK-8841](https://issues.apache.org/jira/browse/SPARK-8841) | Fix partition pruning percentage log message |  Trivial | SQL | Steve Lindemann | Steve Lindemann |
| [SPARK-7114](https://issues.apache.org/jira/browse/SPARK-7114) | parse error for DataFrame.filter after aggregate |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8656](https://issues.apache.org/jira/browse/SPARK-8656) | Spark Standalone master json API's worker number is not match web UI number |  Minor | Web UI | thegiive | thegiive |
| [SPARK-8463](https://issues.apache.org/jira/browse/SPARK-8463) | No suitable driver found for write.jdbc |  Major | SQL | Matthew Jones | Liang-Chi Hsieh |
| [SPARK-6747](https://issues.apache.org/jira/browse/SPARK-6747) | Throw an AnalysisException when unsupported Java list types used in Hive UDF |  Major | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-8821](https://issues.apache.org/jira/browse/SPARK-8821) | The ec2 script doesn't run on python 3 with an utf8 env |  Major | EC2 | Simon Hafner | Simon Hafner |
| [SPARK-8845](https://issues.apache.org/jira/browse/SPARK-8845) | ML use of Breeze optimization: use adjustedValue not value? |  Minor | ML | Joseph K. Bradley | DB Tsai |
| [SPARK-8794](https://issues.apache.org/jira/browse/SPARK-8794) | Column pruning isn't applied beneath sample |  Major | SQL | Eron Wright | Liang-Chi Hsieh |
| [SPARK-8868](https://issues.apache.org/jira/browse/SPARK-8868) | SqlSerializer2 can go into infinite loop when row consists only of NullType columns |  Minor | SQL | Josh Rosen | Yin Huai |
| [SPARK-8804](https://issues.apache.org/jira/browse/SPARK-8804) |  order of UTF8String is wrong if there is any non-ascii character in it |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-7050](https://issues.apache.org/jira/browse/SPARK-7050) | Fix Python Kafka test assembly jar not found issue under Maven build |  Minor | Build | Saisai Shao | Saisai Shao |
| [SPARK-8894](https://issues.apache.org/jira/browse/SPARK-8894) | Example code errors in SparkR documentation |  Major | Documentation, SparkR | Sun Rui | Sun Rui |
| [SPARK-6912](https://issues.apache.org/jira/browse/SPARK-6912) | Throw an AnalysisException when unsupported Java Map\<K,V\> types used in Hive UDF |  Major | SQL | Takeshi Yamamuro | Takeshi Yamamuro |
| [SPARK-5707](https://issues.apache.org/jira/browse/SPARK-5707) | Enabling spark.sql.codegen throws ClassNotFound exception |  Blocker | SQL | Yi Yao | Ram Sriharsha |
| [SPARK-8657](https://issues.apache.org/jira/browse/SPARK-8657) | Fail to upload conf archive to viewfs |  Minor | YARN | Tao Li | Tao Li |
| [SPARK-8900](https://issues.apache.org/jira/browse/SPARK-8900) | sparkPackages flag name is wrong in the documentation |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8783](https://issues.apache.org/jira/browse/SPARK-8783) | CTAS with WITH clause does not work |  Minor | SQL | Keuntae Park | Keuntae Park |
| [SPARK-8909](https://issues.apache.org/jira/browse/SPARK-8909) | Nice to have all the examples in scala, java,python, R to be same in sql-programming-guide |  Trivial | Documentation | Alok Singh | Alok Singh |
| [SPARK-8908](https://issues.apache.org/jira/browse/SPARK-8908) | Calling distinct() with parentheses throws error in Scala DataFrame |  Minor | SQL | Cheolsoo Park | Cheolsoo Park |
| [SPARK-8902](https://issues.apache.org/jira/browse/SPARK-8902) | Hostname missing in spark-ec2 error message |  Trivial | EC2 | Daniel Darabos | Daniel Darabos |
| [SPARK-6123](https://issues.apache.org/jira/browse/SPARK-6123) | Parquet reader should use the schema of every file to create converter |  Critical | SQL | Yin Huai | Cheng Lian |
| [SPARK-8450](https://issues.apache.org/jira/browse/SPARK-8450) | PySpark write.parquet raises Unsupported datatype DecimalType() |  Major | PySpark, SQL | Peter Hoffmann | Davies Liu |
| [SPARK-8910](https://issues.apache.org/jira/browse/SPARK-8910) | MiMa test is flaky because it starts a SQLContext |  Critical | Tests | Andrew Or | Andrew Or |
| [SPARK-8937](https://issues.apache.org/jira/browse/SPARK-8937) | A setting \`spark.unsafe.exceptionOnMemoryLeak \` is missing in ScalaTest config. |  Minor | Tests | Kousuke Saruta | Kousuke Saruta |
| [SPARK-8928](https://issues.apache.org/jira/browse/SPARK-8928) | CatalystSchemaConverter doesn't stick to behavior of old versions of Spark SQL when dealing with LISTs |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8819](https://issues.apache.org/jira/browse/SPARK-8819) | Spark doesn't compile with maven 3.3.x |  Blocker | Build | Andrew Or | Andrew Or |
| [SPARK-8940](https://issues.apache.org/jira/browse/SPARK-8940) | Don't overwrite given schema if it is not null for createDataFrame in SparkR |  Major | SparkR | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-8953](https://issues.apache.org/jira/browse/SPARK-8953) | SPARK\_EXECUTOR\_CORES is not read in SparkSubmit |  Trivial | Spark Submit | meiyoula | meiyoula |
| [SPARK-7419](https://issues.apache.org/jira/browse/SPARK-7419) | Flaky test: o.a.s.streaming.CheckpointSuite |  Critical | Tests | Andrew Or | Shixiong Zhu |
| [SPARK-7902](https://issues.apache.org/jira/browse/SPARK-7902) | SQL UDF doesn't support UDT in PySpark |  Critical | PySpark, SQL | Xiangrui Meng | Davies Liu |
| [SPARK-6289](https://issues.apache.org/jira/browse/SPARK-6289) | PySpark doesn't maintain SQL date Types |  Major | PySpark, SQL | Michael Nazario | Davies Liu |
| [SPARK-8865](https://issues.apache.org/jira/browse/SPARK-8865) | Fix bug:  init SimpleConsumerConfig with kafka params |  Minor | DStreams | guowei | guowei |
| [SPARK-8959](https://issues.apache.org/jira/browse/SPARK-8959) | Parquet-thrift and libthrift introduced as test dependencies in PR #7231 break Maven builds |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8852](https://issues.apache.org/jira/browse/SPARK-8852) | spark-streaming-flume-assembly packages too many dependencies |  Major | DStreams | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-8839](https://issues.apache.org/jira/browse/SPARK-8839) | Thrift Sever will throw \`java.util.NoSuchElementException: key not found\` exception when  many clients connect it |  Major | SQL | carlmartin | carlmartin |
| [SPARK-7944](https://issues.apache.org/jira/browse/SPARK-7944) | Spark-Shell 2.11 1.4.0-RC-03 does not add jars to class path |  Critical | Spark Shell | Alexander Nakos | Iulian Dragos |
| [SPARK-8958](https://issues.apache.org/jira/browse/SPARK-8958) | Dynamic allocation: change cached executor timeout to infinity |  Major | Spark Core | Andrew Or | Andrew Or |
| [SPARK-8675](https://issues.apache.org/jira/browse/SPARK-8675) | Executors created by LocalBackend won't get the same classpath as other executor backends |  Major | Spark Core | Min Zhou | Min Zhou |
| [SPARK-8961](https://issues.apache.org/jira/browse/SPARK-8961) | Makes BaseWriterContainer.outputWriterForRow accepts InternalRow instead of Row |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-7735](https://issues.apache.org/jira/browse/SPARK-7735) | Raise Exception on non-zero exit from pyspark pipe commands |  Minor | PySpark | Scott Taylor | Scott Taylor |
| [SPARK-8990](https://issues.apache.org/jira/browse/SPARK-8990) | DataFrameReader.parquet() ignores user specified data source options |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9006](https://issues.apache.org/jira/browse/SPARK-9006) | TimestampType may loss a microsecond after a round trip in Python DataFrame |  Blocker | PySpark, SQL | Davies Liu | Davies Liu |
| [SPARK-8950](https://issues.apache.org/jira/browse/SPARK-8950) | Correct the calculation of SchedulerDelayTime in StagePage |  Minor | Web UI | Carson Wang | Carson Wang |
| [SPARK-8954](https://issues.apache.org/jira/browse/SPARK-8954) | Building Docker Images Fails in 1.4 branch |  Major | Build | Pradeep Bashyal | Yong Tang |
| [SPARK-8636](https://issues.apache.org/jira/browse/SPARK-8636) | CaseKeyWhen has incorrect NULL handling |  Major | SQL | Santiago M. Mola | Vinod KC |
| [SPARK-9001](https://issues.apache.org/jira/browse/SPARK-9001) | sbt doc fails due to javadoc errors |  Minor | Documentation | Joseph E. Gonzalez | Joseph E. Gonzalez |
| [SPARK-8911](https://issues.apache.org/jira/browse/SPARK-8911) | Local mode endless heartbeat warnings |  Major | Spark Core | Andrew Or | Andrew Or |
| [SPARK-9031](https://issues.apache.org/jira/browse/SPARK-9031) | Merge BlockObjectWriter and DiskBlockObject writer to remove abstract class |  Major | Shuffle, Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-4072](https://issues.apache.org/jira/browse/SPARK-4072) | Storage UI does not reflect memory usage by streaming blocks |  Critical | DStreams, Web UI | Tathagata Das | Shixiong Zhu |
| [SPARK-9045](https://issues.apache.org/jira/browse/SPARK-9045) | Fix Scala 2.11 build break due in UnsafeExternalRowSorter |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9050](https://issues.apache.org/jira/browse/SPARK-9050) | Remove out-of-date code in Exchange that was obsoleted by SPARK-8317 |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-5523](https://issues.apache.org/jira/browse/SPARK-5523) | TaskMetrics and TaskInfo have innumerable copies of the hostname string |  Major | DStreams, Spark Core | Tathagata Das | Saisai Shao |
| [SPARK-9012](https://issues.apache.org/jira/browse/SPARK-9012) | Accumulators in the task table should be escaped |  Major | Web UI | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8840](https://issues.apache.org/jira/browse/SPARK-8840) | Float type coercion with hiveContext |  Major | SparkR | Evgeny SInelnikov | Liang-Chi Hsieh |
| [SPARK-9070](https://issues.apache.org/jira/browse/SPARK-9070) | JavaDataFrameSuite teardown NPEs if setup failed |  Trivial | SQL, Tests | Steve Loughran | Steve Loughran |
| [SPARK-9005](https://issues.apache.org/jira/browse/SPARK-9005) | RegressionMetrics computing incorrect explainedVariance |  Major | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-8974](https://issues.apache.org/jira/browse/SPARK-8974) | There is a bug in dynamicAllocation. When there is no running tasks, the number of executor a long time without running tasks, the number of executor does not reduce to the value of "spark.dynamicAllocation.minExecutors". |  Minor | Spark Core | KaiXinXIaoLei | KaiXinXIaoLei |
| [SPARK-8972](https://issues.apache.org/jira/browse/SPARK-8972) | Incorrect result for rollup |  Critical | SQL | Cheng Hao | Cheng Hao |
| [SPARK-6304](https://issues.apache.org/jira/browse/SPARK-6304) | Checkpointing doesn't retain driver port |  Major | DStreams | Marius Soutier | Saisai Shao |
| [SPARK-8646](https://issues.apache.org/jira/browse/SPARK-8646) | PySpark does not run on YARN if master not provided in command line |  Major | PySpark, YARN | Juliet Hougland | Lianhui Wang |
| [SPARK-9126](https://issues.apache.org/jira/browse/SPARK-9126) | StopwatchSuite shouldn't use Thread.sleep() |  Major | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8851](https://issues.apache.org/jira/browse/SPARK-8851) | in Yarn client mode, Client.scala does not login even when credentials are specified |  Major | YARN | Hari Shreedharan | Hari Shreedharan |
| [SPARK-9138](https://issues.apache.org/jira/browse/SPARK-9138) | Vectors.dense() in Python should accept numbers directly |  Critical | MLlib | Davies Liu | Davies Liu |
| [SPARK-9136](https://issues.apache.org/jira/browse/SPARK-9136) | fix several bugs in DateTimeUtils.stringToTimestamp |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-5681](https://issues.apache.org/jira/browse/SPARK-5681) | Calling graceful stop() immediately after start() on StreamingContext should not get stuck indefinitely |  Major | DStreams | Liang-Chi Hsieh | Shixiong Zhu |
| [SPARK-9090](https://issues.apache.org/jira/browse/SPARK-9090) | Fix definition of residual in LinearRegressionSummary |  Trivial | ML | Feynman Liang | Feynman Liang |
| [SPARK-8593](https://issues.apache.org/jira/browse/SPARK-8593) | History Server doesn't show complete application when one attempt inprogress |  Major | YARN | Thomas Graves | Rekha Joshi |
| [SPARK-9117](https://issues.apache.org/jira/browse/SPARK-9117) | fix BooleanSimplification in case-insensitive |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7026](https://issues.apache.org/jira/browse/SPARK-7026) | LeftSemiJoin can not work when it  has both equal condition and not equal condition. |  Major | SQL | Zhongshuai Pei | Adrian Wang |
| [SPARK-9109](https://issues.apache.org/jira/browse/SPARK-9109) | Unpersist a graph object does not work properly |  Minor | GraphX | Tien-Dung LE | Tien-Dung LE |
| [SPARK-8443](https://issues.apache.org/jira/browse/SPARK-8443) | GenerateMutableProjection Exceeds JVM Code Size Limits |  Major | SQL | Sen Fang | Sen Fang |
| [SPARK-9021](https://issues.apache.org/jira/browse/SPARK-9021) |  Change RDD.aggregate() to do reduce(mapPartitions()) instead of mapPartitions.fold() |  Major | PySpark | Nicholas Hwang | Nicholas Hwang |
| [SPARK-8705](https://issues.apache.org/jira/browse/SPARK-8705) | Javascript error in the web console when \`totalExecutionTime\` of a task is 0 |  Major | Web UI | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8103](https://issues.apache.org/jira/browse/SPARK-8103) | DAGScheduler should not launch multiple concurrent attempts for one stage on fetch failures |  Major | Scheduler, Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-9101](https://issues.apache.org/jira/browse/SPARK-9101) | Can't use null in selectExpr |  Major | PySpark | Mateusz Buśkiewicz | Mateusz Buśkiewicz |
| [SPARK-9114](https://issues.apache.org/jira/browse/SPARK-9114) | The returned value is not converted into internal type in Python UDF |  Blocker | PySpark, SQL | Davies Liu | Davies Liu |
| [SPARK-9175](https://issues.apache.org/jira/browse/SPARK-9175) | BLAS.gemm fails to update matrix C when alpha==0 and beta!=1 |  Critical | MLlib | Meihua Wu | Meihua Wu |
| [SPARK-9187](https://issues.apache.org/jira/browse/SPARK-9187) | Timeline view may show negative value for running tasks |  Minor | Web UI | Carson Wang | Carson Wang |
| [SPARK-8401](https://issues.apache.org/jira/browse/SPARK-8401) | Build system scala version selection script fails on Mac OS X |  Minor | Build | Michael Allman | Michael Allman |
| [SPARK-9193](https://issues.apache.org/jira/browse/SPARK-9193) | Avoid assigning tasks to executors under killing |  Major | Scheduler | Jie Huang | Jie Huang |
| [SPARK-8357](https://issues.apache.org/jira/browse/SPARK-8357) | Memory leakage on unsafe aggregation path with empty input |  Critical | SQL | Navis | Navis |
| [SPARK-9206](https://issues.apache.org/jira/browse/SPARK-9206) | ClassCastException using HiveContext with GoogleHadoopFileSystem as fs.defaultFS |  Major | SQL | Dennis Huo | Dennis Huo |
| [SPARK-9266](https://issues.apache.org/jira/browse/SPARK-9266) | Prevent "managed memory leak detected" exception from masking original exception |  Major | Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-9183](https://issues.apache.org/jira/browse/SPARK-9183) | NPE / confusing error message when looking up missing function in Spark SQL |  Blocker | SQL | Josh Rosen | Yijie Shen |
| [SPARK-9286](https://issues.apache.org/jira/browse/SPARK-9286) | Methods in Unevaluable should be final |  Trivial | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8092](https://issues.apache.org/jira/browse/SPARK-8092) | OneVsRest doesn't allow flexibility in label/ feature column renaming |  Major | ML | Ram Sriharsha | Ram Sriharsha |
| [SPARK-8756](https://issues.apache.org/jira/browse/SPARK-8756) | Keep cached information and avoid re-calculating footers in ParquetRelation2 |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-9236](https://issues.apache.org/jira/browse/SPARK-9236) | Left Outer Join with empty JavaPairRDD returns empty RDD |  Major | Java API | Vitalii Slobodianyk | François Garillot |
| [SPARK-9238](https://issues.apache.org/jira/browse/SPARK-9238) | two extra useless entries for bytesOfCodePointInUTF8 |  Trivial | SQL | zhichao-li | zhichao-li |
| [SPARK-9261](https://issues.apache.org/jira/browse/SPARK-9261) | StreamingTab calls public APIs in Spark core that expose shaded classes |  Minor | DStreams | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-9270](https://issues.apache.org/jira/browse/SPARK-9270) | Allow --name option in pyspark |  Minor | PySpark | Cheolsoo Park | Cheolsoo Park |
| [SPARK-9331](https://issues.apache.org/jira/browse/SPARK-9331) | Indent generated code properly when dumping them in debug code or exception mode |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9254](https://issues.apache.org/jira/browse/SPARK-9254) | sbt-launch-lib.bash should use \`curl --location\` to support HTTP/HTTPS redirection |  Major | Build | Cheng Lian | Cheng Lian |
| [SPARK-8881](https://issues.apache.org/jira/browse/SPARK-8881) | Standalone mode scheduling fails because cores assignment is not atomic |  Critical | Deploy | Nishkam Ravi | Nishkam Ravi |
| [SPARK-9260](https://issues.apache.org/jira/browse/SPARK-9260) | Standalone scheduling can overflow a worker with cores |  Major | Deploy | Andrew Or | Nishkam Ravi |
| [SPARK-9326](https://issues.apache.org/jira/browse/SPARK-9326) | Spark never closes the lock file used to prevent concurrent downloads |  Minor | Spark Core | Kay Ousterhout | Kay Ousterhout |
| [SPARK-9371](https://issues.apache.org/jira/browse/SPARK-9371) | Special chars in column names is broken in HiveContext |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9366](https://issues.apache.org/jira/browse/SPARK-9366) | TaskEnd event emitted for task has different stage attempt ID than TaskStart for same task |  Major | Spark Core | Ryan Williams | Ryan Williams |
| [SPARK-9378](https://issues.apache.org/jira/browse/SPARK-9378) | Test case "CTAS with serde" fails occasionally |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-8988](https://issues.apache.org/jira/browse/SPARK-8988) | Driver logs links is missing on secure cluster |  Major | YARN | Hari Shreedharan | Hari Shreedharan |
| [SPARK-8828](https://issues.apache.org/jira/browse/SPARK-8828) | Revert the change of SPARK-5680 |  Critical | SQL | Yin Huai | Yijie Shen |
| [SPARK-9394](https://issues.apache.org/jira/browse/SPARK-9394) | CodeFormatter should handle parentheses |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9327](https://issues.apache.org/jira/browse/SPARK-9327) | Docs incorrectly state that "spark.\*.extraClassPath" append entries |  Major | Documentation | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-9393](https://issues.apache.org/jira/browse/SPARK-9393) | Fix several error-handling bugs in ScriptTransform operator |  Critical | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9421](https://issues.apache.org/jira/browse/SPARK-9421) | Fix null-handling bug in UnsafeRow.getDouble, getFloat(), and get(ordinal, dataType) |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9419](https://issues.apache.org/jira/browse/SPARK-9419) | ShuffleMemoryManager and MemoryStore should track memory on a per-task, not per-thread, basis |  Critical | Block Manager, Spark Core | Josh Rosen | Josh Rosen |
| [SPARK-9127](https://issues.apache.org/jira/browse/SPARK-9127) | Rand/Randn codegen fails with long seed |  Blocker | SQL | Davies Liu | Reynold Xin |
| [SPARK-9448](https://issues.apache.org/jira/browse/SPARK-9448) | GenerateUnsafeProjection should not share expressions across instances |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9116](https://issues.apache.org/jira/browse/SPARK-9116) | python UDT in \_\_main\_\_ cannot be serialized by PySpark |  Critical | PySpark | Davies Liu | Davies Liu |
| [SPARK-9335](https://issues.apache.org/jira/browse/SPARK-9335) | Kinesis test hits rate limit |  Critical | DStreams, Tests | Patrick Wendell | Tathagata Das |
| [SPARK-9277](https://issues.apache.org/jira/browse/SPARK-9277) | SparseVector constructor must throw an error when declared number of elements less than array length |  Minor | MLlib | Andrey Vykhodtsev | Sean Owen |
| [SPARK-9267](https://issues.apache.org/jira/browse/SPARK-9267) | Remove highly unnecessary accumulators stringify methods |  Trivial | Spark Core | Andrew Or | François Garillot |
| [SPARK-8297](https://issues.apache.org/jira/browse/SPARK-8297) | Scheduler backend is not notified in case node fails in YARN |  Critical | YARN | Mridul Muralidharan | Mridul Muralidharan |
| [SPARK-9437](https://issues.apache.org/jira/browse/SPARK-9437) | SizeEstimator overflows for primitive arrays |  Minor | Spark Core | Imran Rashid | Imran Rashid |
| [SPARK-9479](https://issues.apache.org/jira/browse/SPARK-9479) | ReceiverTrackerSuite fails for maven build |  Major | DStreams, Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8742](https://issues.apache.org/jira/browse/SPARK-8742) | Improve SparkR error messages for DataFrame API |  Blocker | SparkR | Hossein Falaki | Hossein Falaki |
| [SPARK-6319](https://issues.apache.org/jira/browse/SPARK-6319) | Should throw analysis exception when using binary type in groupby/join |  Critical | SQL | Cheng Lian | Liang-Chi Hsieh |
| [SPARK-9509](https://issues.apache.org/jira/browse/SPARK-9509) | AppClient.stop() may throw an exception |  Major | . | Kay Ousterhout | Shixiong Zhu |
| [SPARK-9497](https://issues.apache.org/jira/browse/SPARK-9497) | Flaky test: DistributedSuite failed after the test of "repeatedly failing task that crashes JVM" |  Major | Tests | Yin Huai | Shixiong Zhu |
| [SPARK-9446](https://issues.apache.org/jira/browse/SPARK-9446) | Clear Active SparkContext in stop() method |  Minor | Spark Core | Ted Yu | Ted Yu |
| [SPARK-9202](https://issues.apache.org/jira/browse/SPARK-9202) | Worker should not have data structures which grow without bound |  Blocker | Deploy | Josh Rosen | Nan Zhu |
| [SPARK-9491](https://issues.apache.org/jira/browse/SPARK-9491) | App running on secure YARN with no HBase config will hang |  Blocker | YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-7937](https://issues.apache.org/jira/browse/SPARK-7937) | Cannot compare Hive named\_struct. (when using argmax, argmin) |  Major | SQL | Jianshi Huang | Liang-Chi Hsieh |
| [SPARK-2205](https://issues.apache.org/jira/browse/SPARK-2205) | Unnecessary exchange operators in a join on multiple tables with the same join key. |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-9511](https://issues.apache.org/jira/browse/SPARK-9511) | Table names starting with numbers no longer supported |  Blocker | SQL | Michael Armbrust | Joseph Batchik |
| [SPARK-9255](https://issues.apache.org/jira/browse/SPARK-9255) | SQL codegen fails with "value \< is not a member of TimestampType.this.InternalType" |  Major | SQL | Paul Wu | Reynold Xin |
| [SPARK-9558](https://issues.apache.org/jira/browse/SPARK-9558) | Update docs to follow the increase of memory defaults. |  Minor | Documentation | Kousuke Saruta | Kousuke Saruta |
| [SPARK-8891](https://issues.apache.org/jira/browse/SPARK-8891) | Calling aggregation expressions on null literals fails at runtime |  Blocker | SQL | Josh Rosen | Yin Huai |
| [SPARK-8416](https://issues.apache.org/jira/browse/SPARK-8416) | Thread dump page should highlight Spark executor threads |  Major | Web UI | Josh Rosen | Nan Zhu |
| [SPARK-3190](https://issues.apache.org/jira/browse/SPARK-3190) | Creation of large graph(\> 2.15 B nodes) seems to be broken:possible overflow somewhere |  Critical | GraphX | npanj | Ankur Dave |
| [SPARK-9583](https://issues.apache.org/jira/browse/SPARK-9583) | build/mvn script should not print debug messages to stdout |  Minor | Build | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-9512](https://issues.apache.org/jira/browse/SPARK-9512) | RemoveEvaluationFromSort reorders sort order |  Blocker | SQL | Yin Huai | Michael Armbrust |
| [SPARK-9609](https://issues.apache.org/jira/browse/SPARK-9609) | Spelling error in Strategy.defaultStrategy |  Trivial | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-7119](https://issues.apache.org/jira/browse/SPARK-7119) | ScriptTransform doesn't consider the output data type |  Critical | SQL | Cheng Hao | zhichao-li |
| [SPARK-9131](https://issues.apache.org/jira/browse/SPARK-9131) | Python UDFs change data values |  Blocker | PySpark, SQL | Luis Guerra | Davies Liu |
| [SPARK-9046](https://issues.apache.org/jira/browse/SPARK-9046) | Decimal type support improvement and bug fix |  Critical | SQL | Yin Huai | Davies Liu |
| [SPARK-9601](https://issues.apache.org/jira/browse/SPARK-9601) | Join example fix in streaming-programming-guide.md |  Trivial | Documentation | Jayant Shekhar | Namit Katariya |
| [SPARK-9607](https://issues.apache.org/jira/browse/SPARK-9607) | Incorrect zinc check in build/mvn |  Minor | Build | Ryan Williams | Ryan Williams |
| [SPARK-9608](https://issues.apache.org/jira/browse/SPARK-9608) | Incorrect zinc -status check in build/mvn |  Minor | Build | Ryan Williams | Ryan Williams |
| [SPARK-9593](https://issues.apache.org/jira/browse/SPARK-9593) | Hive ShimLoader loads wrong Hadoop shims when Spark is compiled against Hadoop 2.0.0-mr1-cdh4.1.1 |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9141](https://issues.apache.org/jira/browse/SPARK-9141) | DataFrame recomputed instead of using cached parent. |  Blocker | SQL | Nick Pritchard | Michael Armbrust |
| [SPARK-9054](https://issues.apache.org/jira/browse/SPARK-9054) | Rename RowOrdering to InterpretedOrdering and use newOrdering to build orderings |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9651](https://issues.apache.org/jira/browse/SPARK-9651) | UnsafeExternalSorterSuite is broken |  Major | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-8338](https://issues.apache.org/jira/browse/SPARK-8338) | Ganglia fails to start |  Minor | EC2 | Vladimir Vladimirov | Vladimir Vladimirov |
| [SPARK-6795](https://issues.apache.org/jira/browse/SPARK-6795) | Avoid reading Parquet footers on driver side when an global arbitrative schema is available |  Critical | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9482](https://issues.apache.org/jira/browse/SPARK-9482) | Broadcast join projection is not thread safe |  Blocker | SQL | Xiangrui Meng | Davies Liu |
| [SPARK-9616](https://issues.apache.org/jira/browse/SPARK-9616) | Erroneous result in Frequent Items (SQL) when merging FrequentItemCounters |  Critical | MLlib, SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-9619](https://issues.apache.org/jira/browse/SPARK-9619) | Rename Receiver.executor to Receiver.supervisor |  Minor | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9639](https://issues.apache.org/jira/browse/SPARK-9639) | JobHandler may throw NPE if JobScheduler has been stopped |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9645](https://issues.apache.org/jira/browse/SPARK-9645) | External shuffle service does not work with kerberos on |  Blocker | Spark Core, YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-9362](https://issues.apache.org/jira/browse/SPARK-9362) | Exception when using DataFrame groupby().sum on Decimal type in Python |  Major | PySpark | Jeffrey Chan | Davies Liu |
| [SPARK-8272](https://issues.apache.org/jira/browse/SPARK-8272) | BigDecimal in parquet not working |  Major | Spark Core, SQL | Bipin Roshan Nag | Davies Liu |
| [SPARK-4988](https://issues.apache.org/jira/browse/SPARK-4988) | "Create table ..as select ..from..order by .. limit 10" report error when one col is a Decimal |  Major | SQL | guowei | Davies Liu |
| [SPARK-6360](https://issues.apache.org/jira/browse/SPARK-6360) | For Spark 1.1 and 1.2, after any RDD transformations, calling saveAsParquetFile over a SchemaRDD with decimal or UDT column throws |  Major | SQL | Cheng Lian | Davies Liu |
| [SPARK-7897](https://issues.apache.org/jira/browse/SPARK-7897) | Column with an unsigned bigint should be treated as DecimalType in JDBCRDD |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-9691](https://issues.apache.org/jira/browse/SPARK-9691) | PySpark SQL rand function treats seed 0 as no seed |  Major | PySpark, SQL | Joseph K. Bradley | Yin Huai |
| [SPARK-9228](https://issues.apache.org/jira/browse/SPARK-9228) | Combine unsafe and codegen into a single option |  Blocker | SQL | Michael Armbrust | Davies Liu |
| [SPARK-9650](https://issues.apache.org/jira/browse/SPARK-9650) | Inconsistent quoting behavior for columns in scala |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8057](https://issues.apache.org/jira/browse/SPARK-8057) | Call TaskAttemptContext.getTaskAttemptID using Reflection |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9683](https://issues.apache.org/jira/browse/SPARK-9683) | copy UTF8String when convert unsafe array/map to safe |  Critical | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9734](https://issues.apache.org/jira/browse/SPARK-9734) | java.lang.IllegalArgumentException: Don't know how to save StructField(sal,DecimalType(7,2),true) to JDBC |  Major | SQL | Greg Rahn | Davies Liu |
| [SPARK-9353](https://issues.apache.org/jira/browse/SPARK-9353) | Standalone scheduling memory requirement incorrect if cores per executor is not set |  Major | Deploy | Andrew Or | Andrew Or |
| [SPARK-9614](https://issues.apache.org/jira/browse/SPARK-9614) | InternalRow representation during executionPlan.toRdd.aggregete possibly problematic |  Blocker | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8382](https://issues.apache.org/jira/browse/SPARK-8382) | Improve Analysis Unit test framework |  Major | SQL | Michael Armbrust | Wenchen Fan |
| [SPARK-9731](https://issues.apache.org/jira/browse/SPARK-9731) | Standalone scheduling incorrect cores if spark.executor.cores is not set |  Blocker | Deploy | Carson Wang | Carson Wang |
| [SPARK-6902](https://issues.apache.org/jira/browse/SPARK-6902) | Row() object can be mutated even though it should be immutable |  Major | PySpark, SQL | Jonathan Arfa | Davies Liu |
| [SPARK-6212](https://issues.apache.org/jira/browse/SPARK-6212) | The EXPLAIN output of CTAS only shows the analyzed plan |  Major | SQL | Yin Huai | Yijie Shen |
| [SPARK-8930](https://issues.apache.org/jira/browse/SPARK-8930) | Throw a AnalysisException with meaningful messages if DataFrame#explode takes a star in expressions |  Major | SQL | Takeshi Yamamuro | Yijie Shen |
| [SPARK-9743](https://issues.apache.org/jira/browse/SPARK-9743) | Scanning a HadoopFsRelation shouldn't requrire refreshing |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9784](https://issues.apache.org/jira/browse/SPARK-9784) | Exchange.isUnsafe should check whether codegen and unsafe are enabled |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9620](https://issues.apache.org/jira/browse/SPARK-9620) | generated UnsafeProjection does not support many columns or large exressions |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-9801](https://issues.apache.org/jira/browse/SPARK-9801) | Spark streaming deletes the temp file and backup files without checking if they exist or not |  Minor | DStreams | Hao Zhu | Hao Zhu |
| [SPARK-9340](https://issues.apache.org/jira/browse/SPARK-9340) | CatalystSchemaConverter and CatalystRowConverter don't handle unannotated repeated fields correctly |  Major | SQL | Damian Guy | Cheng Lian |
| [SPARK-9363](https://issues.apache.org/jira/browse/SPARK-9363) | SortMergeJoin operator should support UnsafeRow |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9785](https://issues.apache.org/jira/browse/SPARK-9785) | HashPartitioning compatibility should consider expression ordering |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9750](https://issues.apache.org/jira/browse/SPARK-9750) | SparseMatrix should override equals |  Critical | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9824](https://issues.apache.org/jira/browse/SPARK-9824) | Internal Accumulators will leak WeakReferences |  Blocker | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8498](https://issues.apache.org/jira/browse/SPARK-8498) | Fix NullPointerException in error-handling path in UnsafeShuffleWriter |  Major | Shuffle | Josh Rosen | holdenk |
| [SPARK-9649](https://issues.apache.org/jira/browse/SPARK-9649) | Flaky test: o.a.s.deploy.master.MasterSuite: recovery |  Critical | Deploy, Tests | Andrew Or | Andrew Or |
| [SPARK-9854](https://issues.apache.org/jira/browse/SPARK-9854) | RuleExecutor.timeMap should be thread-safe |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8366](https://issues.apache.org/jira/browse/SPARK-8366) | maxNumExecutorsNeeded should properly handle failed tasks |  Major | Spark Core | meiyoula | meiyoula |
| [SPARK-9806](https://issues.apache.org/jira/browse/SPARK-9806) | Don't share ReplayListenerBus between multiple applications |  Minor | Web UI | Rohit Agarwal | Rohit Agarwal |
| [SPARK-9829](https://issues.apache.org/jira/browse/SPARK-9829) | peakExecutionMemory is not correct in task table |  Major | SQL | Davies Liu | Shixiong Zhu |
| [SPARK-9426](https://issues.apache.org/jira/browse/SPARK-9426) | Job page DAG visualization is not shown |  Blocker | Web UI | Andrew Or | Carson Wang |
| [SPARK-9407](https://issues.apache.org/jira/browse/SPARK-9407) | Parquet shouldn't fail when pushing down predicates over a column whose underlying Parquet type is an ENUM |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8644](https://issues.apache.org/jira/browse/SPARK-8644) | SparkException thrown due to Executor exceptions should include caller site in stack trace |  Major | Spark Core | Aaron Davidson | Aaron Davidson |
| [SPARK-9795](https://issues.apache.org/jira/browse/SPARK-9795) | Dynamic allocation: avoid double counting when killing same executor twice |  Critical | Spark Core | Andrew Or | Andrew Or |
| [SPARK-9745](https://issues.apache.org/jira/browse/SPARK-9745) | Applications hangs when the last executor fails with dynamic allocation |  Blocker | PySpark, Scheduler, YARN | Alex Angelini | Andrew Or |
| [SPARK-9804](https://issues.apache.org/jira/browse/SPARK-9804) | "isSrcLocal" parameter in loadTable / loadPartition is incorrect for HDFS source data |  Major | SQL | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-9726](https://issues.apache.org/jira/browse/SPARK-9726) | PySpark Regression: DataFrame join no longer accepts None as join expression |  Major | PySpark | Brennan Ashton | Brennan Ashton |
| [SPARK-9449](https://issues.apache.org/jira/browse/SPARK-9449) | inputFiles misses files from MetastoreRelation |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-9826](https://issues.apache.org/jira/browse/SPARK-9826) | Cannot use custom classes in log4j.properties |  Minor | Spark Core | Michel Lemay | Michel Lemay |
| [SPARK-9870](https://issues.apache.org/jira/browse/SPARK-9870) | Disable driver UI and Master REST server in SparkSubmitSuite |  Major | Spark Core, SQL, Tests | Josh Rosen | Josh Rosen |
| [SPARK-9827](https://issues.apache.org/jira/browse/SPARK-9827) | Too many open files in TungstenExchange |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-9916](https://issues.apache.org/jira/browse/SPARK-9916) | Clear leftover sparkr.zip copies and creations (e.g. make-distribution.sh) |  Blocker | . | Burak Yavuz | Burak Yavuz |
| [SPARK-9885](https://issues.apache.org/jira/browse/SPARK-9885) | IsolatedClientLoader ignores shared prefixes and barrier prefixes when "spark.sql.hive.metastore.jars" is set to "maven" |  Critical | SQL | Cheng Lian | Yin Huai |
| [SPARK-9757](https://issues.apache.org/jira/browse/SPARK-9757) | Can't create persistent data source tables with decimal |  Blocker | SQL | Michael Armbrust | Cheng Lian |
| [SPARK-9936](https://issues.apache.org/jira/browse/SPARK-9936) | decimal precision lost when loading DataFrame from RDD |  Major | SQL | Tzach Zohar | Liang-Chi Hsieh |
| [SPARK-9073](https://issues.apache.org/jira/browse/SPARK-9073) | spark.ml Models copy() should call setParent when there is a parent |  Minor | ML | Joseph K. Bradley | Kai Sasaki |
| [SPARK-9942](https://issues.apache.org/jira/browse/SPARK-9942) | Broken pandas could crash PySpark SQL |  Blocker | PySpark, SQL | Davies Liu | Davies Liu |
| [SPARK-8976](https://issues.apache.org/jira/browse/SPARK-8976) | Python 3 crash: ValueError: invalid mode 'a+' (only r, w, b allowed) |  Major | PySpark | Olivier Delalleau | Davies Liu |
| [SPARK-9943](https://issues.apache.org/jira/browse/SPARK-9943) | Failed to serialize a deserialized UnsafeHashedRelation |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-9945](https://issues.apache.org/jira/browse/SPARK-9945) | pageSize is calculated from driver.memory instead of executor.memory |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-9958](https://issues.apache.org/jira/browse/SPARK-9958) | HiveThriftServer2Listener is not thread-safe |  Major | SQL | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9780](https://issues.apache.org/jira/browse/SPARK-9780) | In case of invalid initialization of KafkaDirectStream, NPE is thrown |  Minor | DStreams | Grigory Turunov | Cody Koeninger |
| [SPARK-9956](https://issues.apache.org/jira/browse/SPARK-9956) | Spark ML trees and ensembles fail for categorical features with 1 category |  Major | ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9946](https://issues.apache.org/jira/browse/SPARK-9946) | NPE in TaskMemoryManager |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-9589](https://issues.apache.org/jira/browse/SPARK-9589) | Flaky test: HiveCompatibilitySuite.groupby8 |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-9561](https://issues.apache.org/jira/browse/SPARK-9561) | Enable BroadcastJoinSuite |  Blocker | SQL, Tests | Andrew Or | Andrew Or |
| [SPARK-9828](https://issues.apache.org/jira/browse/SPARK-9828) | Should not share \`{}\` among instances |  Critical | ML, PySpark | Xiangrui Meng | Manoj Kumar |
| [SPARK-9809](https://issues.apache.org/jira/browse/SPARK-9809) | Task crashes because the internal accumulators are not properly initialized |  Blocker | Spark Core | Carson Wang | Carson Wang |
| [SPARK-9877](https://issues.apache.org/jira/browse/SPARK-9877) | StandaloneRestServer NPE when submitting application |  Blocker | Spark Core | Saisai Shao | Saisai Shao |
| [SPARK-9978](https://issues.apache.org/jira/browse/SPARK-9978) | Window functions require partitionBy to work as expected |  Major | PySpark | Maciej Szymkiewicz | Davies Liu |
| [SPARK-9323](https://issues.apache.org/jira/browse/SPARK-9323) | DataFrame.orderBy gives confusing analysis errors when ordering based on nested columns |  Major | SQL | Josh Rosen | Michael Armbrust |
| [SPARK-9634](https://issues.apache.org/jira/browse/SPARK-9634) | cleanup unnecessary Aliases in LogicalPlan at the end of analysis |  Major | SQL | Wenchen Fan | Michael Armbrust |
| [SPARK-9725](https://issues.apache.org/jira/browse/SPARK-9725) | spark sql query string field return empty/garbled string |  Blocker | SQL | Fei Wang | Davies Liu |
| [SPARK-9980](https://issues.apache.org/jira/browse/SPARK-9980) | SBT publishLocal error due to invalid characters in doc |  Trivial | Build | Herman van Hovell | Herman van Hovell |
| [SPARK-9955](https://issues.apache.org/jira/browse/SPARK-9955) | TPCDS Q8 failed in 1.5 |  Critical | SQL | Davies Liu | Wenchen Fan |
| [SPARK-8844](https://issues.apache.org/jira/browse/SPARK-8844) | head/collect is broken in SparkR |  Blocker | SparkR | Davies Liu | Sun Rui |
| [SPARK-10008](https://issues.apache.org/jira/browse/SPARK-10008) | Shuffle locality can take precedence over narrow dependencies for RDDs with both |  Major | Scheduler | Matei Zaharia | Matei Zaharia |
| [SPARK-9973](https://issues.apache.org/jira/browse/SPARK-9973) | Wrong initial size of in-memory columnar buffers |  Major | SQL | xukun | xukun |
| [SPARK-9760](https://issues.apache.org/jira/browse/SPARK-9760) | SparkSubmit doesn't work with --packages when --repositories is not specified |  Blocker | Spark Core | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-10005](https://issues.apache.org/jira/browse/SPARK-10005) | Parquet reader doesn't handle schema merging properly for nested structs |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9959](https://issues.apache.org/jira/browse/SPARK-9959) | Association Rules needs JavaItems |  Critical | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-7837](https://issues.apache.org/jira/browse/SPARK-7837) | NPE when save as parquet in speculative tasks |  Critical | SQL | Yin Huai | Cheng Lian |
| [SPARK-10036](https://issues.apache.org/jira/browse/SPARK-10036) | DataFrameReader.json and DataFrameWriter.json don't load the JDBC driver class before creating JDBC connection |  Major | SQL | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9592](https://issues.apache.org/jira/browse/SPARK-9592) | Last implemented based on AggregateExpression1 are calculating the values for entire DataFrame partition not on GroupedData partition. |  Minor | SQL | gaurav | Yin Huai |
| [SPARK-9974](https://issues.apache.org/jira/browse/SPARK-9974) | SBT build: com.twitter:parquet-hadoop-bundle:1.6.0 is not packaged into the assembly jar |  Blocker | Build, SQL | Cheng Lian | Cheng Lian |
| [SPARK-10038](https://issues.apache.org/jira/browse/SPARK-10038) | TungstenProject code generation fails when applied to array\<binary\> |  Blocker | SQL | Josh Rosen | Davies Liu |
| [SPARK-10080](https://issues.apache.org/jira/browse/SPARK-10080) | Binary Incompatibility in SQLContext implicits |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-10089](https://issues.apache.org/jira/browse/SPARK-10089) | SQL tests leave unmanaged files in source directory |  Trivial | SQL | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-10072](https://issues.apache.org/jira/browse/SPARK-10072) | BlockGenerator can deadlock when the queue block queue of generate blocks fills up to capacity |  Blocker | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-10102](https://issues.apache.org/jira/browse/SPARK-10102) | Fix a race condition that startReceiver may happen before setting trackerState to Started |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9606](https://issues.apache.org/jira/browse/SPARK-9606) | HiveThriftServer tests failing. |  Blocker | SQL | Michael Armbrust | Cheng Lian |
| [SPARK-10096](https://issues.apache.org/jira/browse/SPARK-10096) | CreateStruct/CreateArray/CreateNamedStruct broken with UDFs |  Blocker | SQL | Michael Armbrust | Reynold Xin |
| [SPARK-10093](https://issues.apache.org/jira/browse/SPARK-10093) | Invalid transformations for TungstenProject of struct type |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-9508](https://issues.apache.org/jira/browse/SPARK-9508) | Align graphx programming guide with the updated Pregel code |  Minor | Documentation | Alexander Ulanov | Alexander Ulanov |
| [SPARK-10107](https://issues.apache.org/jira/browse/SPARK-10107) | NPE in format\_number |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-10087](https://issues.apache.org/jira/browse/SPARK-10087) | Disable reducer locality in 1.5 |  Critical | Scheduler | Yin Huai | Yin Huai |
| [SPARK-10073](https://issues.apache.org/jira/browse/SPARK-10073) | Python withColumn for existing column name not consistent with scala |  Blocker | SQL | Michael Armbrust | Davies Liu |
| [SPARK-9627](https://issues.apache.org/jira/browse/SPARK-9627) | SQL job failed if the dataframe with string columns is cached |  Blocker | SQL | Davies Liu | Cheng Lian |
| [SPARK-10090](https://issues.apache.org/jira/browse/SPARK-10090) | After division, Decimal may have longer precision than expected |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-10083](https://issues.apache.org/jira/browse/SPARK-10083) | CaseWhen should support type coercion of DecimalType and FractionalType |  Major | SQL | Adrian Wang | Adrian Wang |
| [SPARK-10119](https://issues.apache.org/jira/browse/SPARK-10119) | Utils.isDynamicAllocationEnabled returns wrong value if dynAlloc is explicitly disabled |  Critical | Spark Core | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-10124](https://issues.apache.org/jira/browse/SPARK-10124) | Mesos cluster mode causes exception when multiple spark apps are being scheduled |  Major | Mesos | Timothy Chen | Timothy Chen |
| [SPARK-10125](https://issues.apache.org/jira/browse/SPARK-10125) | Fix a potential deadlock in JobGenerator.stop |  Major | . | Shixiong Zhu | Shixiong Zhu |
| [SPARK-10128](https://issues.apache.org/jira/browse/SPARK-10128) | Kinesis sequence numbers cannot be recovered from WAL because WAL does not use the correct classloader |  Blocker | . | Tathagata Das | Tathagata Das |
| [SPARK-10092](https://issues.apache.org/jira/browse/SPARK-10092) | Multi-DB support follow up |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9982](https://issues.apache.org/jira/browse/SPARK-9982) | SparkR DataFrame fail to return data of Decimal type |  Major | SparkR | Alex Shkurenko | Alex Shkurenko |
| [SPARK-10136](https://issues.apache.org/jira/browse/SPARK-10136) | Parquet support fail to decode Avro/Thrift arrays of primitive array (e.g. array\<array\<int\>\>) |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-10126](https://issues.apache.org/jira/browse/SPARK-10126) | Fix typo in release-build.sh which broke snapshot publishing for Scala 2.11 |  Blocker | Project Infra | Josh Rosen | Josh Rosen |
| [SPARK-10138](https://issues.apache.org/jira/browse/SPARK-10138) | Setters do not return self type in Java MultilayerPerceptronClassifier |  Blocker | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10130](https://issues.apache.org/jira/browse/SPARK-10130) | type coercion for IF should have children resolved first |  Blocker | SQL | Adrian Wang | Adrian Wang |
| [SPARK-10122](https://issues.apache.org/jira/browse/SPARK-10122) | AttributeError: 'RDD' object has no attribute 'offsetRanges' |  Major | DStreams, PySpark | Amit Ramesh | Saisai Shao |
| [SPARK-10143](https://issues.apache.org/jira/browse/SPARK-10143) | Parquet changed the behavior of calculating splits |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-10164](https://issues.apache.org/jira/browse/SPARK-10164) | GMM bug: match error |  Critical | MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-10142](https://issues.apache.org/jira/browse/SPARK-10142) | Python Streaming checkpoint recovery does not work with non-local file path |  Critical | DStreams, PySpark | Tathagata Das | Tathagata Das |
| [SPARK-10166](https://issues.apache.org/jira/browse/SPARK-10166) | Python Streaming checkpoint recovery fails if an active Python SparkContext already exists |  Critical | DStreams, PySpark | Tathagata Das | Tathagata Das |
| [SPARK-10168](https://issues.apache.org/jira/browse/SPARK-10168) | Streaming assembly jars doesn't publish correctly |  Blocker | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-10144](https://issues.apache.org/jira/browse/SPARK-10144) | Actually show peak execution memory on UI by default |  Major | Web UI | Andrew Or | Andrew Or |
| [SPARK-9758](https://issues.apache.org/jira/browse/SPARK-9758) | Compilation issue for hive test |  Trivial | Build | Ashok Kumar | Sean Owen |
| [SPARK-10190](https://issues.apache.org/jira/browse/SPARK-10190) | NPE in CatalystTypeConverters when converting null decimal value back to Scala |  Blocker | SQL | Josh Rosen | Josh Rosen |
| [SPARK-10165](https://issues.apache.org/jira/browse/SPARK-10165) | Nested Hive UDF resolution fails in Analyzer |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-7497](https://issues.apache.org/jira/browse/SPARK-7497) | test\_count\_by\_value\_and\_window is flaky |  Critical | DStreams, PySpark | Xiangrui Meng | Davies Liu |
| [SPARK-10121](https://issues.apache.org/jira/browse/SPARK-10121) | Custom Class added through Spark SQL's add jar command may not be in the class loader used by metadataHive |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-10196](https://issues.apache.org/jira/browse/SPARK-10196) | Failed to save json data with a decimal type in the schema |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9813](https://issues.apache.org/jira/browse/SPARK-9813) | Incorrect UNION ALL behavior |  Major | Spark Core, SQL | Simeon Simeonov | Josh Rosen |
| [SPARK-10210](https://issues.apache.org/jira/browse/SPARK-10210) | Exception "Could not compute split, block input-XXX not found" after streaming app driver recovers from checkpoint |  Critical | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-10177](https://issues.apache.org/jira/browse/SPARK-10177) | Parquet support interprets timestamp values differently from Hive 0.14.0+ |  Blocker | SQL | Cheng Lian | Davies Liu |
| [SPARK-10195](https://issues.apache.org/jira/browse/SPARK-10195) | Spark SQL's internal types should not be exposed via data sources Filter interfaces |  Critical | SQL | Josh Rosen | Josh Rosen |
| [SPARK-10197](https://issues.apache.org/jira/browse/SPARK-10197) | Add null check in wrapperFor (inside HiveInspectors). |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-10198](https://issues.apache.org/jira/browse/SPARK-10198) | Turn off Hive verifyPartitionPath by default |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-10245](https://issues.apache.org/jira/browse/SPARK-10245) | SQLContext can't parse literal less than 0.1 (e.g. 0.01) |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-10215](https://issues.apache.org/jira/browse/SPARK-10215) | Div of Decimal returns null |  Blocker | SQL | Cheng Hao | Davies Liu |
| [SPARK-10135](https://issues.apache.org/jira/browse/SPARK-10135) | Percent of pruned partitions is shown wrong |  Trivial | SQL | Romi Kuntsman | Reynold Xin |
| [SPARK-10305](https://issues.apache.org/jira/browse/SPARK-10305) | PySpark createDataFrame on list of LabeledPoints fails (regression) |  Critical | ML, PySpark, SQL | Joseph K. Bradley | Davies Liu |
| [SPARK-10308](https://issues.apache.org/jira/browse/SPARK-10308) | %in% is not exported in SparkR |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-10219](https://issues.apache.org/jira/browse/SPARK-10219) | Error when additional options provided as variable in write.df |  Major | SparkR | Samuel Alexander | Shivaram Venkataraman |
| [SPARK-10315](https://issues.apache.org/jira/browse/SPARK-10315) | remove document on spark.akka.failure-detector.threshold |  Minor | Documentation | Nan Zhu | Nan Zhu |
| [SPARK-10287](https://issues.apache.org/jira/browse/SPARK-10287) | After processing a query using JSON data, Spark SQL continuously refreshes metadata of the table |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-10188](https://issues.apache.org/jira/browse/SPARK-10188) | Pyspark CrossValidator with RMSE selects incorrect model |  Critical | PySpark | Noel Smith | Noel Smith |
| [SPARK-10328](https://issues.apache.org/jira/browse/SPARK-10328) | na.omit has too restrictive generic in SparkR |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-8952](https://issues.apache.org/jira/browse/SPARK-8952) | JsonFile() of SQLContext display improper warning message for a S3 path |  Major | SparkR | Sun Rui | Luciano Resende |
| [SPARK-10325](https://issues.apache.org/jira/browse/SPARK-10325) | Public Row no longer overrides hashCode / violates hashCode + equals contract |  Critical | SQL | Josh Rosen | Josh Rosen |
| [SPARK-10336](https://issues.apache.org/jira/browse/SPARK-10336) | fitIntercept is a command line option but not set in the LR example program. |  Major | Documentation, ML | Shuo Xiang | Shuo Xiang |
| [SPARK-10323](https://issues.apache.org/jira/browse/SPARK-10323) | NPE in code-gened In expression |  Critical | SQL | Yin Huai | Davies Liu |
| [SPARK-10321](https://issues.apache.org/jira/browse/SPARK-10321) | OrcRelation doesn't override sizeInBytes |  Critical | SQL | Cheng Lian | Davies Liu |
| [SPARK-10326](https://issues.apache.org/jira/browse/SPARK-10326) | Cannot launch YARN job on Windows |  Major | YARN | Marcelo Vanzin | Marcelo Vanzin |
| [SPARK-10175](https://issues.apache.org/jira/browse/SPARK-10175) | Enhance spark doap file |  Minor | Project Infra | Luciano Resende | Luciano Resende |
| [SPARK-10350](https://issues.apache.org/jira/browse/SPARK-10350) | Fix SQL Programming Guide |  Minor | Documentation, SQL | Guoqiang Li | Guoqiang Li |
| [SPARK-10226](https://issues.apache.org/jira/browse/SPARK-10226) | Error occured in SparkSQL when using  != |  Major | SQL | wangwei | wangwei |
| [SPARK-10339](https://issues.apache.org/jira/browse/SPARK-10339) | When scanning a partitioned table having thousands of partitions, Driver has a very high memory pressure because of SQL metrics |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-10334](https://issues.apache.org/jira/browse/SPARK-10334) | Partitioned table scan's query plan does not show Filter and Project on top of the table scan |  Critical | SQL | Yin Huai | Yin Huai |
| [SPARK-10369](https://issues.apache.org/jira/browse/SPARK-10369) | Fix a bug that Receiver could not be started after deregistering |  Critical | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-10341](https://issues.apache.org/jira/browse/SPARK-10341) | SMJ fail with unable to acquire memory |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-10391](https://issues.apache.org/jira/browse/SPARK-10391) | Spark 1.4.1 released news under news/spark-1-3-1-released.html |  Minor | Documentation | Jacek Laskowski | Sean Owen |
| [SPARK-10353](https://issues.apache.org/jira/browse/SPARK-10353) | MLlib BLAS gemm outputs wrong result when beta = 0.0 for transpose transpose matrix multiplication |  Major | MLlib | Burak Yavuz | Burak Yavuz |
| [SPARK-10298](https://issues.apache.org/jira/browse/SPARK-10298) | PySpark can't JSON serialize a DataFrame with DecimalType columns. |  Major | SQL | Kevin Cox | Michael Armbrust |
| [SPARK-10159](https://issues.apache.org/jira/browse/SPARK-10159) | Hive 1.3.x GenericUDFDate NPE issue |  Major | SQL | Alex Liu | Michael Armbrust |
| [SPARK-10467](https://issues.apache.org/jira/browse/SPARK-10467) | Vector is converted to tuple when extracted from Row using \_\_getitem\_\_ |  Minor | ML, PySpark, SQL | Maciej Szymkiewicz | Davies Liu |
| [SPARK-7880](https://issues.apache.org/jira/browse/SPARK-7880) | Silent failure if assembly jar is corrupted |  Minor | Spark Submit | Andrew Or | Sean Owen |
| [SPARK-7942](https://issues.apache.org/jira/browse/SPARK-7942) | Receiver's life cycle is inconsistent with streaming job. |  Major | DStreams | carlmartin | Tathagata Das |
| [SPARK-3283](https://issues.apache.org/jira/browse/SPARK-3283) | Receivers sometimes do not get spread out to multiple nodes |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9343](https://issues.apache.org/jira/browse/SPARK-9343) | DROP TABLE ignores IF EXISTS clause |  Major | SQL | Simeon Simeonov | Michael Armbrust |
| [SPARK-2063](https://issues.apache.org/jira/browse/SPARK-2063) | Creating a SchemaRDD via sql() does not correctly resolve nested types |  Major | SQL | Aaron Davidson | Michael Armbrust |
| [SPARK-2607](https://issues.apache.org/jira/browse/SPARK-2607) | SchemaRDD unionall prevents caching |  Major | SQL | Thierry Herrmann | Michael Armbrust |
| [SPARK-2824](https://issues.apache.org/jira/browse/SPARK-2824) | Allow saving Parquet files to the HiveMetastore |  Major | SQL | Aaron Davidson | Michael Armbrust |
| [SPARK-3231](https://issues.apache.org/jira/browse/SPARK-3231) | select on a table in parquet format containing smallint as a field type does not work |  Major | SQL | chirag aggarwal | Alex Rovner |
| [SPARK-3978](https://issues.apache.org/jira/browse/SPARK-3978) | Schema change on Spark-Hive (Parquet file format) table not working |  Major | SQL | Nilesh Barge | Alex Rovner |
| [SPARK-3804](https://issues.apache.org/jira/browse/SPARK-3804) | Output of Generator expressions is not stable after serialization. |  Major | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-4559](https://issues.apache.org/jira/browse/SPARK-4559) | Adding support for ucase and lcase |  Major | SQL | Fei Wang | Michael Armbrust |
| [SPARK-4278](https://issues.apache.org/jira/browse/SPARK-4278) | SparkSQL job failing with java.lang.ClassCastException |  Major | SQL | Parviz Deyhim | Yin Huai |
| [SPARK-5421](https://issues.apache.org/jira/browse/SPARK-5421) | SparkSql throw OOM at shuffle |  Major | SQL | Hong Shen | Michael Armbrust |
| [SPARK-5397](https://issues.apache.org/jira/browse/SPARK-5397) | Assigning aliases to several return values of an UDF |  Major | SQL | Max | Michael Armbrust |
| [SPARK-5314](https://issues.apache.org/jira/browse/SPARK-5314) | java.lang.OutOfMemoryError in SparkSQL with GROUP BY |  Major | SQL | Alex Baretta | Michael Armbrust |
| [SPARK-10508](https://issues.apache.org/jira/browse/SPARK-10508) | incorrect evaluation of searched case expression |  Major | SQL | N Campbell | Josh Rosen |
| [SPARK-8786](https://issues.apache.org/jira/browse/SPARK-8786) | Create a wrapper for BinaryType |  Major | SQL | Davies Liu | Josh Rosen |
| [SPARK-10504](https://issues.apache.org/jira/browse/SPARK-10504) | aggregate where NULL is defined as the value expression aborts when SUM used |  Minor | SQL | N Campbell | Yin Huai |
| [SPARK-7989](https://issues.apache.org/jira/browse/SPARK-7989) | Fix flaky tests in ExternalShuffleServiceSuite and SparkListenerWithClusterSuite |  Critical | Spark Core, Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8567](https://issues.apache.org/jira/browse/SPARK-8567) | Flaky test: o.a.s.sql.hive.HiveSparkSubmitSuite --jars |  Blocker | SQL, Tests | Yin Huai | Yin Huai |
| [SPARK-8939](https://issues.apache.org/jira/browse/SPARK-8939) | YARN EC2 default setting fails with IllegalArgumentException |  Major | EC2 | Andrew Or | Shivaram Venkataraman |
| [SPARK-8430](https://issues.apache.org/jira/browse/SPARK-8430) | ExternalShuffleBlockResolver should support UnsafeShuffleManager |  Critical | Shuffle | Lianhui Wang | Lianhui Wang |
| [SPARK-8119](https://issues.apache.org/jira/browse/SPARK-8119) | HeartbeatReceiver should not adjust application executor resources |  Critical | Spark Core | carlmartin | Andrew Or |
| [SPARK-6416](https://issues.apache.org/jira/browse/SPARK-6416) | Document that RDD.fold() requires the operator to be commutative |  Minor | Documentation, Spark Core | Josh Rosen | Sean Owen |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-7854](https://issues.apache.org/jira/browse/SPARK-7854) | refine Kryo configuration limits test |  Minor | Spark Core, Tests | Zhang, Liye | Zhang, Liye |
| [SPARK-8508](https://issues.apache.org/jira/browse/SPARK-8508) | Test case "SQLQuerySuite.test script transform for stderr" generates super long output |  Minor | SQL, Tests | Cheng Lian | Cheng Lian |
| [SPARK-8541](https://issues.apache.org/jira/browse/SPARK-8541) | sumApprox and meanApprox doctests are incorrect |  Minor | PySpark | Scott Taylor | Scott Taylor |
| [SPARK-8634](https://issues.apache.org/jira/browse/SPARK-8634) | Fix flaky test StreamingListenerSuite "receiver info reporting" |  Critical | DStreams, Tests | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8715](https://issues.apache.org/jira/browse/SPARK-8715) | ArrayOutOfBoundsException for DataFrameStatSuite.crosstab |  Major | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8810](https://issues.apache.org/jira/browse/SPARK-8810) | Gaps in SQL UDF test coverage |  Major | SQL | Spiro Michaylov | Spiro Michaylov |
| [SPARK-8765](https://issues.apache.org/jira/browse/SPARK-8765) | Flaky PySpark PowerIterationClustering test |  Critical | MLlib, PySpark | Joseph K. Bradley | Yanbo Liang |
| [SPARK-5562](https://issues.apache.org/jira/browse/SPARK-5562) | LDA should handle empty documents |  Minor | MLlib | Joseph K. Bradley | Alok Singh |
| [SPARK-9204](https://issues.apache.org/jira/browse/SPARK-9204) | Add default params test to linear regression |  Trivial | ML | holdenk | holdenk |
| [SPARK-9222](https://issues.apache.org/jira/browse/SPARK-9222) | Make class instantiation variables in DistributedLDAModel [private] clustering |  Minor | MLlib | Manoj Kumar | Manoj Kumar |
| [SPARK-9225](https://issues.apache.org/jira/browse/SPARK-9225) | LDASuite needs unit tests for empty documents |  Minor | MLlib | Feynman Liang | Meihua Wu |
| [SPARK-9030](https://issues.apache.org/jira/browse/SPARK-9030) | Add Kinesis.createStream unit tests that actual sends data |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9581](https://issues.apache.org/jira/browse/SPARK-9581) | Add test for JSON UDTs |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9211](https://issues.apache.org/jira/browse/SPARK-9211) | HiveComparisonTest generates incorrect file name for golden answer files on Windows |  Minor | SQL, Windows | Christian Kadner | Christian Kadner |
| [SPARK-9624](https://issues.apache.org/jira/browse/SPARK-9624) | Make RateControllerSuite faster and more robust |  Minor | DStreams, Tests | Tathagata Das | Tathagata Das |
| [SPARK-9640](https://issues.apache.org/jira/browse/SPARK-9640) | Do not run Python Kinesis tests when the Kinesis assembly JAR has not been generated |  Major | DStreams, Tests | Tathagata Das | Tathagata Das |
| [SPARK-9948](https://issues.apache.org/jira/browse/SPARK-9948) | Flaky test: o.a.s.AccumulatorSuite - internal accumulators |  Critical | Tests | Andrew Or | Andrew Or |
| [SPARK-9805](https://issues.apache.org/jira/browse/SPARK-9805) | Make streaming PySpark ML tests more robust using termination conditions |  Major | DStreams, MLlib, PySpark | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-10059](https://issues.apache.org/jira/browse/SPARK-10059) | Broken test: YarnClusterSuite |  Critical | . | Davies Liu | Marcelo Vanzin |
| [SPARK-10012](https://issues.apache.org/jira/browse/SPARK-10012) | Missing test case for Params#arrayLengthGt |  Trivial | ML, Tests | Kai Sasaki | Kai Sasaki |
| [SPARK-10098](https://issues.apache.org/jira/browse/SPARK-10098) | Failures in streaming.FailureSuite can leak StreamingContext and SparkContext which fails all subsequent tests |  Critical | DStreams, Tests | Tathagata Das | Tathagata Das |
| [SPARK-9939](https://issues.apache.org/jira/browse/SPARK-9939) | Resort to Java process API in test suites forking subprocesses |  Critical | SQL | Cheng Lian | Cheng Lian |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-3850](https://issues.apache.org/jira/browse/SPARK-3850) | Scala style: disallow trailing spaces |  Minor | Project Infra | Nicholas Chammas | Reynold Xin |
| [SPARK-7986](https://issues.apache.org/jira/browse/SPARK-7986) | Refactor scalastyle-config.xml to divide it into 3 sections |  Major | Build | Reynold Xin | Reynold Xin |
| [SPARK-7984](https://issues.apache.org/jira/browse/SPARK-7984) | do type coercion for key and when expressions in CaseKeyWhen |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7952](https://issues.apache.org/jira/browse/SPARK-7952) | equality check between boolean type and numeric type is broken. |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-7562](https://issues.apache.org/jira/browse/SPARK-7562) | Improve error reporting for expression data type mismatch |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8074](https://issues.apache.org/jira/browse/SPARK-8074) | Parquet should throw AnalysisException during setup for data type/name related failures |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7980](https://issues.apache.org/jira/browse/SPARK-7980) | Support SQLContext.range(end) |  Major | SQL | Reynold Xin | Animesh Baranawal |
| [SPARK-7558](https://issues.apache.org/jira/browse/SPARK-7558) | Log test name when starting and finishing each test |  Major | Tests | Patrick Wendell | Andrew Or |
| [SPARK-7743](https://issues.apache.org/jira/browse/SPARK-7743) | Upgrade Parquet to 1.7 |  Major | SQL | Thomas Omans | Thomas Omans |
| [SPARK-6909](https://issues.apache.org/jira/browse/SPARK-6909) | Remove Hive Shim code |  Critical | SQL | Michael Armbrust | Cheolsoo Park |
| [SPARK-7991](https://issues.apache.org/jira/browse/SPARK-7991) | Python DataFrame: support passing a list into describe |  Major | SQL | Reynold Xin | Amey Chaugule |
| [SPARK-4258](https://issues.apache.org/jira/browse/SPARK-4258) | NPE with new Parquet Filters |  Critical | SQL | Michael Armbrust | Thomas Omans |
| [SPARK-8146](https://issues.apache.org/jira/browse/SPARK-8146) | DataFrame Python API: Alias replace in DataFrameNaFunctions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-5451](https://issues.apache.org/jira/browse/SPARK-5451) | And predicates are not properly pushed down |  Critical | SQL | Cheng Lian | Thomas Omans |
| [SPARK-8148](https://issues.apache.org/jira/browse/SPARK-8148) | Do not use FloatType in partition column inference |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7990](https://issues.apache.org/jira/browse/SPARK-7990) | Add methods to facilitate equi-join on multiple join keys |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8215](https://issues.apache.org/jira/browse/SPARK-8215) | math function: pi |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8212](https://issues.apache.org/jira/browse/SPARK-8212) | math function: e |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-7996](https://issues.apache.org/jira/browse/SPARK-7996) | Deprecate the developer api SparkEnv.actorSystem |  Major | Spark Core | Shixiong Zhu | Ilya Ganelin |
| [SPARK-8248](https://issues.apache.org/jira/browse/SPARK-8248) | string function: length |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8217](https://issues.apache.org/jira/browse/SPARK-8217) | math function: log2 |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8201](https://issues.apache.org/jira/browse/SPARK-8201) | conditional function: if |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8205](https://issues.apache.org/jira/browse/SPARK-8205) | conditional function: nvl |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8208](https://issues.apache.org/jira/browse/SPARK-8208) | math function: ceiling |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8210](https://issues.apache.org/jira/browse/SPARK-8210) | math function: degrees |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8211](https://issues.apache.org/jira/browse/SPARK-8211) | math function: radians |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8219](https://issues.apache.org/jira/browse/SPARK-8219) | math function: negative |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8216](https://issues.apache.org/jira/browse/SPARK-8216) | math function: rename log -\> ln |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8222](https://issues.apache.org/jira/browse/SPARK-8222) | math function: alias power / pow |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8225](https://issues.apache.org/jira/browse/SPARK-8225) | math function: alias sign / signum |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8228](https://issues.apache.org/jira/browse/SPARK-8228) | conditional function: isnull |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8229](https://issues.apache.org/jira/browse/SPARK-8229) | conditional function: isnotnull |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8250](https://issues.apache.org/jira/browse/SPARK-8250) | string function: alias lower/lcase |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8251](https://issues.apache.org/jira/browse/SPARK-8251) | string function: alias upper / ucase |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7158](https://issues.apache.org/jira/browse/SPARK-7158) | collect and take return different results |  Blocker | SQL | Reynold Xin | Cheng Hao |
| [SPARK-7993](https://issues.apache.org/jira/browse/SPARK-7993) | Improve DataFrame.show() output |  Blocker | SQL | Reynold Xin | Akhil Thatipamula |
| [SPARK-8330](https://issues.apache.org/jira/browse/SPARK-8330) | DAG visualization: trim whitespace from input |  Major | Web UI | Andrew Or | Andrew Or |
| [SPARK-7186](https://issues.apache.org/jira/browse/SPARK-7186) | Decouple internal Row from external Row |  Blocker | SQL | Reynold Xin | Davies Liu |
| [SPARK-8347](https://issues.apache.org/jira/browse/SPARK-8347) | Add unit tests for abs |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8362](https://issues.apache.org/jira/browse/SPARK-8362) | Add unit tests for +, -, \*, /, % |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8065](https://issues.apache.org/jira/browse/SPARK-8065) | Add support for connecting to Hive 0.14 metastore |  Major | SQL | Reynold Xin | Marcelo Vanzin |
| [SPARK-8220](https://issues.apache.org/jira/browse/SPARK-8220) | math function: positive |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-7199](https://issues.apache.org/jira/browse/SPARK-7199) | Add date and timestamp support to UnsafeRow |  Major | SQL | Josh Rosen | Liang-Chi Hsieh |
| [SPARK-7017](https://issues.apache.org/jira/browse/SPARK-7017) | Refactor dev/run-tests into Python |  Major | Build, Project Infra | Brennon York | Brennon York |
| [SPARK-8218](https://issues.apache.org/jira/browse/SPARK-8218) | math function: log |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8283](https://issues.apache.org/jira/browse/SPARK-8283) | udf\_struct test failure |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8320](https://issues.apache.org/jira/browse/SPARK-8320) | Add example in streaming programming guide that shows union of multiple input streams |  Minor | DStreams | Tathagata Das | Neelesh Srinivas Salian |
| [SPARK-8363](https://issues.apache.org/jira/browse/SPARK-8363) | Move sqrt into math |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8353](https://issues.apache.org/jira/browse/SPARK-8353) | Show anchor links when hovering over documentation headers |  Major | Documentation | Josh Rosen | Josh Rosen |
| [SPARK-8444](https://issues.apache.org/jira/browse/SPARK-8444) | Add Python example in streaming for queueStream usage |  Minor | DStreams | Bryan Cutler | Bryan Cutler |
| [SPARK-8234](https://issues.apache.org/jira/browse/SPARK-8234) | misc function: md5 |  Major | SQL | Reynold Xin | Qian, Shilei |
| [SPARK-4118](https://issues.apache.org/jira/browse/SPARK-4118) | Create python bindings for Streaming KMeans |  Major | DStreams, MLlib, PySpark | Anant Daksh Asthana | Manoj Kumar |
| [SPARK-8422](https://issues.apache.org/jira/browse/SPARK-8422) | Introduce a module abstraction inside of dev/run-tests |  Major | Build, Project Infra | Josh Rosen | Josh Rosen |
| [SPARK-8495](https://issues.apache.org/jira/browse/SPARK-8495) | Add a \`.lintr\` file to validate the SparkR files and the \`lint-r\` script |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-7715](https://issues.apache.org/jira/browse/SPARK-7715) | Update MLlib Programming Guide for 1.4 |  Major | Documentation, ML, MLlib | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8455](https://issues.apache.org/jira/browse/SPARK-8455) | Implement N-Gram Feature Transformer |  Minor | ML | Feynman Liang | Feynman Liang |
| [SPARK-8537](https://issues.apache.org/jira/browse/SPARK-8537) | Add a validation rule about the curly braces in SparkR to \`.lintr\` |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8356](https://issues.apache.org/jira/browse/SPARK-8356) | Reconcile callUDF and callUdf |  Critical | SQL | Michael Armbrust | Benjamin Fradet |
| [SPARK-8492](https://issues.apache.org/jira/browse/SPARK-8492) | Support BinaryType in UnsafeRow |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8548](https://issues.apache.org/jira/browse/SPARK-8548) | Remove the trailing whitespaces from the SparkR files |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8300](https://issues.apache.org/jira/browse/SPARK-8300) | DataFrame hint for broadcast join |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8371](https://issues.apache.org/jira/browse/SPARK-8371) | improve unit test for MaxOf and MinOf |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8568](https://issues.apache.org/jira/browse/SPARK-8568) | Prevent accidental use of "and" and "or" to build invalid expressions in Python |  Critical | SQL | Reynold Xin | Davies Liu |
| [SPARK-7633](https://issues.apache.org/jira/browse/SPARK-7633) | Streaming Logistic Regression- Python bindings |  Major | MLlib, PySpark | Yanbo Liang | Manoj Kumar |
| [SPARK-6777](https://issues.apache.org/jira/browse/SPARK-6777) | Implement backwards-compatibility rules in Parquet schema converters |  Critical | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8075](https://issues.apache.org/jira/browse/SPARK-8075) | apply type checking interface to more expressions |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8237](https://issues.apache.org/jira/browse/SPARK-8237) | misc function: sha2 |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8613](https://issues.apache.org/jira/browse/SPARK-8613) | Add a param for disabling of feature scaling, default to true |  Major | ML | holdenk | holdenk |
| [SPARK-8583](https://issues.apache.org/jira/browse/SPARK-8583) | Refactor python/run-tests to integrate with dev/run-test's module system |  Major | Build, Project Infra, PySpark | Josh Rosen | Josh Rosen |
| [SPARK-8355](https://issues.apache.org/jira/browse/SPARK-8355) | Python DataFrameReader/Writer should mirror scala |  Critical | SQL | Michael Armbrust | Cheolsoo Park |
| [SPARK-8698](https://issues.apache.org/jira/browse/SPARK-8698) | partitionBy in Python DataFrame reader/writer interface should not default to empty tuple |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8702](https://issues.apache.org/jira/browse/SPARK-8702) | Avoid massive concating strings in Javascript |  Major | Web UI | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8693](https://issues.apache.org/jira/browse/SPARK-8693) | profiles and goals are not printed in a nice way |  Minor | Build, Project Infra | Yin Huai | Brennon York |
| [SPARK-8066](https://issues.apache.org/jira/browse/SPARK-8066) | Add support for connecting to Hive 1.0 (0.14.1) |  Major | SQL | Reynold Xin | Marcelo Vanzin |
| [SPARK-8067](https://issues.apache.org/jira/browse/SPARK-8067) | Add support for connecting to Hive 1.1 |  Major | SQL | Reynold Xin | Marcelo Vanzin |
| [SPARK-8235](https://issues.apache.org/jira/browse/SPARK-8235) | misc function: sha1 / sha |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8214](https://issues.apache.org/jira/browse/SPARK-8214) | math function: hex |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-8681](https://issues.apache.org/jira/browse/SPARK-8681) | crosstab column names in wrong order |  Critical | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-8056](https://issues.apache.org/jira/browse/SPARK-8056) | Design an easier way to construct schema for both Scala and Python |  Major | SQL | Reynold Xin | Ilya Ganelin |
| [SPARK-8721](https://issues.apache.org/jira/browse/SPARK-8721) | Rename ExpectsInputTypes =\> AutoCastInputTypes |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8434](https://issues.apache.org/jira/browse/SPARK-8434) | Add a "pretty" parameter to show |  Major | SQL | Shixiong Zhu | Shixiong Zhu |
| [SPARK-8236](https://issues.apache.org/jira/browse/SPARK-8236) | misc function: crc32 |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-4127](https://issues.apache.org/jira/browse/SPARK-4127) | Streaming Linear Regression- Python bindings |  Major | MLlib, PySpark | Anant Daksh Asthana | Manoj Kumar |
| [SPARK-8664](https://issues.apache.org/jira/browse/SPARK-8664) | Add PCA transformer |  Major | ML | Yanbo Liang | Yanbo Liang |
| [SPARK-8471](https://issues.apache.org/jira/browse/SPARK-8471) | Implement Discrete Cosine Transform feature transformer |  Minor | ML | Feynman Liang | Feynman Liang |
| [SPARK-7514](https://issues.apache.org/jira/browse/SPARK-7514) | Add MinMaxScaler to feature transformation |  Major | MLlib | yuhao yang | yuhao yang |
| [SPARK-8741](https://issues.apache.org/jira/browse/SPARK-8741) | Remove e and pi from DataFrame functions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8752](https://issues.apache.org/jira/browse/SPARK-8752) | Add ExpectsInputTypes trait for defining expected input types. |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8621](https://issues.apache.org/jira/browse/SPARK-8621) | crosstab exception when one of the value is empty |  Critical | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-6263](https://issues.apache.org/jira/browse/SPARK-6263) | Python MLlib API missing items: Utils |  Major | MLlib, PySpark | Joseph K. Bradley | Kai Sasaki |
| [SPARK-8766](https://issues.apache.org/jira/browse/SPARK-8766) | DataFrame Python API should work with column which has non-ascii character in it |  Major | PySpark | Davies Liu | Davies Liu |
| [SPARK-8770](https://issues.apache.org/jira/browse/SPARK-8770) | BinaryOperator expression |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8227](https://issues.apache.org/jira/browse/SPARK-8227) | math function: unhex |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-8758](https://issues.apache.org/jira/browse/SPARK-8758) | Add Python user guide for PowerIterationClustering |  Major | MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8223](https://issues.apache.org/jira/browse/SPARK-8223) | math function: shiftleft |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8224](https://issues.apache.org/jira/browse/SPARK-8224) | math function: shiftright |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8407](https://issues.apache.org/jira/browse/SPARK-8407) | complex type constructors: struct and named\_struct |  Major | SQL | Yijie Shen | Yijie Shen |
| [SPARK-8772](https://issues.apache.org/jira/browse/SPARK-8772) | Implement implicit type cast for expressions that define expected input types |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7104](https://issues.apache.org/jira/browse/SPARK-7104) | Support model save/load in Python's Word2Vec |  Minor | MLlib, PySpark | Joseph K. Bradley | Yu Ishikawa |
| [SPARK-8213](https://issues.apache.org/jira/browse/SPARK-8213) | math function: factorial |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-8801](https://issues.apache.org/jira/browse/SPARK-8801) | Support TypeCollection in ExpectsInputTypes |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8226](https://issues.apache.org/jira/browse/SPARK-8226) | math function: shiftrightunsigned |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-7401](https://issues.apache.org/jira/browse/SPARK-7401) | Dot product and squared\_distances should be vectorized in Vectors |  Major | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8192](https://issues.apache.org/jira/browse/SPARK-8192) | date/time function: current\_date |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8193](https://issues.apache.org/jira/browse/SPARK-8193) | date/time function: current\_timestamp |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8238](https://issues.apache.org/jira/browse/SPARK-8238) | string function: ascii |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8239](https://issues.apache.org/jira/browse/SPARK-8239) | string function: base64 |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8242](https://issues.apache.org/jira/browse/SPARK-8242) | string function: decode |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8243](https://issues.apache.org/jira/browse/SPARK-8243) | string function: encode |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8268](https://issues.apache.org/jira/browse/SPARK-8268) | string function: unbase64 |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8270](https://issues.apache.org/jira/browse/SPARK-8270) | string function: levenshtein |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8822](https://issues.apache.org/jira/browse/SPARK-8822) | clean up type checking in math.scala |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8549](https://issues.apache.org/jira/browse/SPARK-8549) | Fix the line length of SparkR |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8831](https://issues.apache.org/jira/browse/SPARK-8831) | Support AbstractDataType in TypeCollection |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8784](https://issues.apache.org/jira/browse/SPARK-8784) | Add python API for hex/unhex |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-8072](https://issues.apache.org/jira/browse/SPARK-8072) | Better AnalysisException for writing DataFrame with identically named columns |  Blocker | SQL | Reynold Xin | Animesh Baranawal |
| [SPARK-8864](https://issues.apache.org/jira/browse/SPARK-8864) | Date/time function and data type design |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8685](https://issues.apache.org/jira/browse/SPARK-8685) | dataframe left joins are not working as expected in pyspark |  Major | PySpark, SQL | axel dahl | Davies Liu |
| [SPARK-8878](https://issues.apache.org/jira/browse/SPARK-8878) | Improve unit test coverage for bitwise expressions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8886](https://issues.apache.org/jira/browse/SPARK-8886) | Python style usually don't add space before/after the = in named parameters |  Trivial | Documentation | Tijo Thomas | Tijo Thomas |
| [SPARK-8753](https://issues.apache.org/jira/browse/SPARK-8753) | Create an IntervalType data type |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8888](https://issues.apache.org/jira/browse/SPARK-8888) | Replace the hash map in DynamicPartitionWriterContainer.outputWriterForRow with java.util.HashMap |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7785](https://issues.apache.org/jira/browse/SPARK-7785) | Add pretty printing to pyspark.mllib.linalg.Matrices |  Minor | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8700](https://issues.apache.org/jira/browse/SPARK-8700) | Disable feature scaling in Logistic Regression |  Major | ML | DB Tsai | DB Tsai |
| [SPARK-6776](https://issues.apache.org/jira/browse/SPARK-6776) | Implement backwards-compatibility rules in Catalyst converters (which convert Parquet record to rows) |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8932](https://issues.apache.org/jira/browse/SPARK-8932) | Support copy in UnsafeRow as long as ObjectPool is not used |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-8926](https://issues.apache.org/jira/browse/SPARK-8926) | Good errors for invalid input to ExpectsInput expressions |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8773](https://issues.apache.org/jira/browse/SPARK-8773) | Throw type mismatch in check analysis for expressions with expected input types defined |  Major | SQL | Reynold Xin | Michael Armbrust |
| [SPARK-8942](https://issues.apache.org/jira/browse/SPARK-8942) | use double not decimal when cast double and float to timestamp |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8934](https://issues.apache.org/jira/browse/SPARK-8934) | cast from double/float to timestamp should not go through decimal |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-6266](https://issues.apache.org/jira/browse/SPARK-6266) | PySpark SparseVector missing doc for size, indices, values |  Minor | Documentation, MLlib, PySpark | Joseph K. Bradley | Kai Sasaki |
| [SPARK-8830](https://issues.apache.org/jira/browse/SPARK-8830) | levenshtein directly on top of UTF8String |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8938](https://issues.apache.org/jira/browse/SPARK-8938) | Implement toString for Interval data type |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8703](https://issues.apache.org/jira/browse/SPARK-8703) | Add CountVectorizer as a ml transformer to convert document to words count vector |  Major | ML | yuhao yang | yuhao yang |
| [SPARK-8247](https://issues.apache.org/jira/browse/SPARK-8247) | string function: instr |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8249](https://issues.apache.org/jira/browse/SPARK-8249) | string function: locate |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8252](https://issues.apache.org/jira/browse/SPARK-8252) | string function: lpad |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8254](https://issues.apache.org/jira/browse/SPARK-8254) | string function: printf |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8257](https://issues.apache.org/jira/browse/SPARK-8257) | string function: repeat |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8258](https://issues.apache.org/jira/browse/SPARK-8258) | string function: reverse |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8259](https://issues.apache.org/jira/browse/SPARK-8259) | string function: rpad |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8261](https://issues.apache.org/jira/browse/SPARK-8261) | string function: space |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8262](https://issues.apache.org/jira/browse/SPARK-8262) | string function: split |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8253](https://issues.apache.org/jira/browse/SPARK-8253) | string function: ltrim |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8260](https://issues.apache.org/jira/browse/SPARK-8260) | string function: rtrim |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8267](https://issues.apache.org/jira/browse/SPARK-8267) | string function: trim |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-2017](https://issues.apache.org/jira/browse/SPARK-2017) | web ui stage page becomes unresponsive when the number of tasks is large |  Major | Web UI | Reynold Xin | Andrew Or |
| [SPARK-8389](https://issues.apache.org/jira/browse/SPARK-8389) | Expose KafkaRDDs offsetRange in Python |  Critical | DStreams | Tathagata Das | Saisai Shao |
| [SPARK-7977](https://issues.apache.org/jira/browse/SPARK-7977) | Disallow println |  Major | Project Infra | Reynold Xin | Jon Alter |
| [SPARK-8013](https://issues.apache.org/jira/browse/SPARK-8013) | Get JDBC server working with Scala 2.11 |  Critical | SQL | Patrick Wendell | Iulian Dragos |
| [SPARK-8923](https://issues.apache.org/jira/browse/SPARK-8923) | Add @since tags to mllib.fpm |  Minor | Documentation, MLlib | Xiangrui Meng | Rahul Palamuttam |
| [SPARK-7078](https://issues.apache.org/jira/browse/SPARK-7078) | Cache-aware binary processing in-memory sort |  Major | Shuffle | Reynold Xin | Josh Rosen |
| [SPARK-7079](https://issues.apache.org/jira/browse/SPARK-7079) | Cache-aware external sort |  Major | Shuffle, Spark Core | Reynold Xin | Josh Rosen |
| [SPARK-8203](https://issues.apache.org/jira/browse/SPARK-8203) | conditional functions: greatest |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8204](https://issues.apache.org/jira/browse/SPARK-8204) | conditional function: least |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8944](https://issues.apache.org/jira/browse/SPARK-8944) | Support casting between IntervalType and StringType |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8743](https://issues.apache.org/jira/browse/SPARK-8743) | Deregister Codahale metrics for streaming when StreamingContext is closed |  Major | DStreams | Tathagata Das | Neelesh Srinivas Salian |
| [SPARK-8907](https://issues.apache.org/jira/browse/SPARK-8907) | Speed up path construction in DynamicPartitionWriterContainer.outputWriterForRow |  Major | SQL | Reynold Xin | Cheng Lian |
| [SPARK-6261](https://issues.apache.org/jira/browse/SPARK-6261) | Python MLlib API missing items: Feature |  Major | MLlib, PySpark | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9027](https://issues.apache.org/jira/browse/SPARK-9027) | Generalize predicate pushdown into the metastore |  Major | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8962](https://issues.apache.org/jira/browse/SPARK-8962) | Disallow Class.forName |  Major | Project Infra | Josh Rosen | Josh Rosen |
| [SPARK-8969](https://issues.apache.org/jira/browse/SPARK-8969) | move type-check from BinaryArithmetic and BinaryComparison to BinaryOperator |  Trivial | SQL | Wenchen Fan | Reynold Xin |
| [SPARK-8808](https://issues.apache.org/jira/browse/SPARK-8808) | Fix assignments in SparkR |  Major | SparkR | Yu Ishikawa | Sun Rui |
| [SPARK-8993](https://issues.apache.org/jira/browse/SPARK-8993) | More comprehensive type checking in expressions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8206](https://issues.apache.org/jira/browse/SPARK-8206) | math function: round |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8279](https://issues.apache.org/jira/browse/SPARK-8279) | udf\_round\_3 test fails |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9020](https://issues.apache.org/jira/browse/SPARK-9020) | Support mutable state in code gen expressions |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8221](https://issues.apache.org/jira/browse/SPARK-8221) | math function: pmod |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-9071](https://issues.apache.org/jira/browse/SPARK-9071) | MonotonicallyIncreasingID and SparkPartitionID should be marked as nondeterministic |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9086](https://issues.apache.org/jira/browse/SPARK-9086) | Remove BinaryNode from TreeNode |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6602](https://issues.apache.org/jira/browse/SPARK-6602) | Replace direct use of Akka with Spark RPC interface |  Critical | Spark Core | Reynold Xin | Shixiong Zhu |
| [SPARK-9018](https://issues.apache.org/jira/browse/SPARK-9018) | Implement a generic Stopwatch utility for ML algorithms |  Major | ML, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9060](https://issues.apache.org/jira/browse/SPARK-9060) | Revert SPARK-8359, SPARK-8800, and SPARK-8677 |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8245](https://issues.apache.org/jira/browse/SPARK-8245) | string function: format\_number |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9068](https://issues.apache.org/jira/browse/SPARK-9068) | refactor the implicit type cast code |  Minor | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9061](https://issues.apache.org/jira/browse/SPARK-9061) | Fix and re-enable ignored tests in ExpressionTypeCheckingSuite |  Blocker | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-8857](https://issues.apache.org/jira/browse/SPARK-8857) | Make sure accumulator updates don't involve thread-local lookups |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-8859](https://issues.apache.org/jira/browse/SPARK-8859) | Report accumulator updates via heartbeats (internal accumulator only) |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-9102](https://issues.apache.org/jira/browse/SPARK-9102) | Improve project collapse with nondeterministic expressions |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9093](https://issues.apache.org/jira/browse/SPARK-9093) | Fix single-quotes strings in SparkR |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8209](https://issues.apache.org/jira/browse/SPARK-8209) | math function: conv |  Major | SQL | Reynold Xin | zhichao-li |
| [SPARK-8945](https://issues.apache.org/jira/browse/SPARK-8945) | Add and Subtract expression should support IntervalType |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-9080](https://issues.apache.org/jira/browse/SPARK-9080) | IsNaN expression |  Critical | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9079](https://issues.apache.org/jira/browse/SPARK-9079) | Design NaN semantics |  Major | SQL | Reynold Xin | Michael Armbrust |
| [SPARK-8281](https://issues.apache.org/jira/browse/SPARK-8281) | udf\_asin and udf\_acos test failure |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8280](https://issues.apache.org/jira/browse/SPARK-8280) | udf7 failed due to null vs nan semantics |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-5288](https://issues.apache.org/jira/browse/SPARK-5288) | Stabilize Spark SQL data type API followup |  Major | SQL | Yin Huai | Reynold Xin |
| [SPARK-5295](https://issues.apache.org/jira/browse/SPARK-5295) | Stabilize data types |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-4867](https://issues.apache.org/jira/browse/SPARK-4867) | UDF clean up |  Blocker | SQL | Michael Armbrust | Reynold Xin |
| [SPARK-9169](https://issues.apache.org/jira/browse/SPARK-9169) | Improve unit test coverage for null expressions |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9167](https://issues.apache.org/jira/browse/SPARK-9167) | use UTC Calendar in \`stringToDate\` |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9171](https://issues.apache.org/jira/browse/SPARK-9171) | add and improve tests for nondeterministic expressions |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9151](https://issues.apache.org/jira/browse/SPARK-9151) | Implement code generation for Abs |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-9055](https://issues.apache.org/jira/browse/SPARK-9055) | WidenTypes should also support Intersect and Except in addition to Union |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8240](https://issues.apache.org/jira/browse/SPARK-8240) | string function: concat |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9150](https://issues.apache.org/jira/browse/SPARK-9150) | Create CodegenFallback and Unevaluable trait |  Critical | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8199](https://issues.apache.org/jira/browse/SPARK-8199) | date/time function: date\_format |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8184](https://issues.apache.org/jira/browse/SPARK-8184) | date/time function: weekofyear |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8183](https://issues.apache.org/jira/browse/SPARK-8183) | date/time function: second |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8182](https://issues.apache.org/jira/browse/SPARK-8182) | date/time function: minute |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8181](https://issues.apache.org/jira/browse/SPARK-8181) | date/time function: hour |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8180](https://issues.apache.org/jira/browse/SPARK-8180) | date/time function: day / dayofmonth |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8179](https://issues.apache.org/jira/browse/SPARK-8179) | date/time function: month |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8177](https://issues.apache.org/jira/browse/SPARK-8177) | date/time function: year |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8178](https://issues.apache.org/jira/browse/SPARK-8178) | date/time function: quarter |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8638](https://issues.apache.org/jira/browse/SPARK-8638) | Window Function Performance Improvements |  Major | SQL | Herman van Hovell | Herman van Hovell |
| [SPARK-9166](https://issues.apache.org/jira/browse/SPARK-9166) | Hide JVM stack trace for IllegalArgumentException in Python |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8241](https://issues.apache.org/jira/browse/SPARK-8241) | string function: concat\_ws |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9172](https://issues.apache.org/jira/browse/SPARK-9172) | DecimalPrecision should also support Intersect and Except in addition to Union |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-9048](https://issues.apache.org/jira/browse/SPARK-9048) | UnsafeSqlSerializer |  Major | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9049](https://issues.apache.org/jira/browse/SPARK-9049) | UnsafeExchange operator |  Major | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9153](https://issues.apache.org/jira/browse/SPARK-9153) | Implement code generation for StringLPad and StringRPad |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9177](https://issues.apache.org/jira/browse/SPARK-9177) | Reuse Calendar instance in WeekOfYear |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9186](https://issues.apache.org/jira/browse/SPARK-9186) | make deterministic describing the tree rather than the expression |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-6910](https://issues.apache.org/jira/browse/SPARK-6910) | Support for pushing predicates down to metastore for partition pruning |  Critical | SQL | Michael Armbrust | Cheolsoo Park |
| [SPARK-9155](https://issues.apache.org/jira/browse/SPARK-9155) | Implement code generation for StringSpace |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9159](https://issues.apache.org/jira/browse/SPARK-9159) | Implement code generation for Ascii, Base64, and UnBase64 |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9160](https://issues.apache.org/jira/browse/SPARK-9160) | Implement code generation for Encode and Decode |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8125](https://issues.apache.org/jira/browse/SPARK-8125) | Accelerate ParquetRelation2 metadata discovery |  Blocker | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9156](https://issues.apache.org/jira/browse/SPARK-9156) | Implement code generation for StringSplit |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9164](https://issues.apache.org/jira/browse/SPARK-9164) | Implement code generation for Hex and Unhex |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9052](https://issues.apache.org/jira/browse/SPARK-9052) | Fix comments after curly braces |  Major | SparkR | Shivaram Venkataraman | Yu Ishikawa |
| [SPARK-9132](https://issues.apache.org/jira/browse/SPARK-9132) | Implement code gen for Conv |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8797](https://issues.apache.org/jira/browse/SPARK-8797) | Sorting float/double column containing NaNs can lead to "Comparison method violates its general contract!" errors |  Critical | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9146](https://issues.apache.org/jira/browse/SPARK-9146) | NaN should be greater than all other values |  Critical | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9145](https://issues.apache.org/jira/browse/SPARK-9145) | Equality test on NaN = NaN should return true |  Critical | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9147](https://issues.apache.org/jira/browse/SPARK-9147) | UnsafeRow should canonicalize NaN values |  Major | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9157](https://issues.apache.org/jira/browse/SPARK-9157) | Implement code generation for Substring |  Critical | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9161](https://issues.apache.org/jira/browse/SPARK-9161) | Implement code generation for FormatNumber |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8255](https://issues.apache.org/jira/browse/SPARK-8255) | string function: regexp\_extract |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8256](https://issues.apache.org/jira/browse/SPARK-8256) | string function: regexp\_replace |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8230](https://issues.apache.org/jira/browse/SPARK-8230) | complex function: size |  Major | SQL | Reynold Xin | Pedro Rodriguez |
| [SPARK-9173](https://issues.apache.org/jira/browse/SPARK-9173) | UnionPushDown should also support Intersect and Except in addition to Union |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9081](https://issues.apache.org/jira/browse/SPARK-9081) | fillna/dropna should also fill/drop NaN values in addition to null values |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9168](https://issues.apache.org/jira/browse/SPARK-9168) | Add nanvl expression |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8915](https://issues.apache.org/jira/browse/SPARK-8915) | Add @since tags to mllib.classification |  Minor | Documentation, MLlib | Xiangrui Meng | Patrick Baier |
| [SPARK-4598](https://issues.apache.org/jira/browse/SPARK-4598) | Paginate stage page to avoid OOM with \> 100,000 tasks |  Major | Web UI | meiyoula | Shixiong Zhu |
| [SPARK-5989](https://issues.apache.org/jira/browse/SPARK-5989) | Model import/export for LDAModel |  Major | MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-9154](https://issues.apache.org/jira/browse/SPARK-9154) | Implement code generation for StringFormat |  Major | SQL | Reynold Xin | Tarek Auel |
| [SPARK-9121](https://issues.apache.org/jira/browse/SPARK-9121) | Get rid of the warnings about \`no visible global function definition\` in SparkR |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-4233](https://issues.apache.org/jira/browse/SPARK-4233) | Simplify the Aggregation Function implementation |  Major | SQL | Cheng Hao | Cheng Hao |
| [SPARK-4367](https://issues.apache.org/jira/browse/SPARK-4367) | Partial aggregation support the DISTINCT aggregation |  Major | SQL | Cheng Hao | Yin Huai |
| [SPARK-3947](https://issues.apache.org/jira/browse/SPARK-3947) | Support Scala/Java UDAF |  Major | SQL | Pei-Lun Lee | Yin Huai |
| [SPARK-3056](https://issues.apache.org/jira/browse/SPARK-3056) | Sort-based Aggregation |  Major | SQL | Cheng Hao | Yin Huai |
| [SPARK-9082](https://issues.apache.org/jira/browse/SPARK-9082) | Filter using non-deterministic expressions should not be pushed down |  Major | SQL | Yin Huai | Wenchen Fan |
| [SPARK-9165](https://issues.apache.org/jira/browse/SPARK-9165) | Implement code generation for CreateArray, CreateStruct, and CreateNamedStruct |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-8975](https://issues.apache.org/jira/browse/SPARK-8975) | Implement a mechanism to send a new rate from the driver to the block generator |  Major | DStreams | Iulian Dragos | Iulian Dragos |
| [SPARK-9223](https://issues.apache.org/jira/browse/SPARK-9223) | Support model save/load in Python's LDA |  Minor | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-8935](https://issues.apache.org/jira/browse/SPARK-8935) | Implement code generation for all casts |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9212](https://issues.apache.org/jira/browse/SPARK-9212) | update Netty version to "4.0.29.Final" for Netty Metrics |  Trivial | Shuffle, Spark Core | Zhang, Liye | Zhang, Liye |
| [SPARK-8906](https://issues.apache.org/jira/browse/SPARK-8906) | Move all internal data source related classes out of sources package |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9207](https://issues.apache.org/jira/browse/SPARK-9207) | Turn on Parquet filter push-down by default |  Critical | SQL | Cheng Lian | Cheng Lian |
| [SPARK-9216](https://issues.apache.org/jira/browse/SPARK-9216) | Define KinesisBackedBlockRDDs |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9294](https://issues.apache.org/jira/browse/SPARK-9294) | cleanup comments, code style, naming typo for the new aggregation |  Trivial | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9264](https://issues.apache.org/jira/browse/SPARK-9264) | When dealing with Union/Intersect/Except, we cast FloatType/DoubleType to the wrong DecimalType |  Blocker | SQL | Yin Huai | Davies Liu |
| [SPARK-9069](https://issues.apache.org/jira/browse/SPARK-9069) | Remove DecimalType unlimited precision/scale support |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-9200](https://issues.apache.org/jira/browse/SPARK-9200) | Don't implicitly cast non-atomic types to string type |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9249](https://issues.apache.org/jira/browse/SPARK-9249) | local variable assigned but may not be used |  Minor | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9292](https://issues.apache.org/jira/browse/SPARK-9292) | Analysis should check that join conditions' data types are booleans |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9295](https://issues.apache.org/jira/browse/SPARK-9295) | Analysis should detect sorting on unsupported column types |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9330](https://issues.apache.org/jira/browse/SPARK-9330) | create specialized getStruct getter in InternalRow |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8668](https://issues.apache.org/jira/browse/SPARK-8668) | expr function to convert SQL expression into a Column |  Major | SQL | Reynold Xin | Joseph Batchik |
| [SPARK-9291](https://issues.apache.org/jira/browse/SPARK-9291) | Conversion is applied twice on partitioned data sources |  Blocker | SQL | Reynold Xin | Cheng Lian |
| [SPARK-9192](https://issues.apache.org/jira/browse/SPARK-9192) | add initialization phase for nondeterministic expression |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9348](https://issues.apache.org/jira/browse/SPARK-9348) | Remove apply method on InternalRow |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9350](https://issues.apache.org/jira/browse/SPARK-9350) | Introduce an InternalRow generic getter that requires a DataType |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9354](https://issues.apache.org/jira/browse/SPARK-9354) | Remove InternalRow.get generic getter call in Hive integration code |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9356](https://issues.apache.org/jira/browse/SPARK-9356) | Remove the internal use of DecimalType.Unlimited |  Major | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9306](https://issues.apache.org/jira/browse/SPARK-9306) | SortMergeJoin crashes when trying to join on unsortable columns |  Major | SQL | Josh Rosen | Liang-Chi Hsieh |
| [SPARK-9368](https://issues.apache.org/jira/browse/SPARK-9368) | Support get(ordinal, dataType) generic getter in UnsafeRow |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-7943](https://issues.apache.org/jira/browse/SPARK-7943) | saveAsTable in DataFrameWriter can only add table to DataBase “default” |  Major | SQL | baishuo | Cheng Lian |
| [SPARK-8105](https://issues.apache.org/jira/browse/SPARK-8105) | sqlContext.table("databaseName.tableName") broke with SPARK-6908 |  Critical | SQL | Doug Balog | Cheng Lian |
| [SPARK-8435](https://issues.apache.org/jira/browse/SPARK-8435) | Cannot create tables in an specific database using a provider |  Major | SQL | Cristian | Cheng Lian |
| [SPARK-8714](https://issues.apache.org/jira/browse/SPARK-8714) | Refresh table not working with non-default databases |  Major | SQL | Prakash Chockalingam | Cheng Lian |
| [SPARK-8561](https://issues.apache.org/jira/browse/SPARK-8561) | Drop table can only drop the tables under database "default" |  Major | SQL | baishuo | Cheng Lian |
| [SPARK-9364](https://issues.apache.org/jira/browse/SPARK-9364) | Fix array out of bounds and use-after-free bugs in UnsafeExternalSorter |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9369](https://issues.apache.org/jira/browse/SPARK-9369) | Support IntervalType in UnsafeRow |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9349](https://issues.apache.org/jira/browse/SPARK-9349) | UDAF cleanup for 1.5 |  Blocker | SQL | Reynold Xin | Yin Huai |
| [SPARK-9355](https://issues.apache.org/jira/browse/SPARK-9355) | Remove InternalRow.get generic getter call in columnar cache code |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9332](https://issues.apache.org/jira/browse/SPARK-9332) | CatalystTypeConverters.toScala does not work on UnsafeRows |  Critical | SQL | Josh Rosen | Reynold Xin |
| [SPARK-9386](https://issues.apache.org/jira/browse/SPARK-9386) | Feature flag for metastore partitioning |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-8195](https://issues.apache.org/jira/browse/SPARK-8195) | date/time function: last\_day |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8196](https://issues.apache.org/jira/browse/SPARK-8196) | date/time function: next\_day |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-9395](https://issues.apache.org/jira/browse/SPARK-9395) | Create a SpecializedGetters interface to track all the specialized getters |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8919](https://issues.apache.org/jira/browse/SPARK-8919) | Add @since tags to mllib.recommendation |  Minor | Documentation, MLlib | Xiangrui Meng | Vinod KC |
| [SPARK-9402](https://issues.apache.org/jira/browse/SPARK-9402) | Remove CodegenFallback from Abs / FormatNumber |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8003](https://issues.apache.org/jira/browse/SPARK-8003) | Support SPARK\_\_PARTITION\_\_ID in SQL |  Major | SQL | Reynold Xin | Joseph Batchik |
| [SPARK-7105](https://issues.apache.org/jira/browse/SPARK-7105) | Support model save/load in Python's GaussianMixture |  Minor | MLlib, PySpark | Joseph K. Bradley | Manoj Kumar |
| [SPARK-9420](https://issues.apache.org/jira/browse/SPARK-9420) | Move expressions in sql/core package to catalyst. |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9422](https://issues.apache.org/jira/browse/SPARK-9422) | Remove the placeholder attributes used in the aggregation buffers |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8608](https://issues.apache.org/jira/browse/SPARK-8608) | After initializing a DataFrame with random columns and a seed, df.show should return same value |  Critical | SQL | Burak Yavuz | Wenchen Fan |
| [SPARK-8609](https://issues.apache.org/jira/browse/SPARK-8609) | After initializing a DataFrame with random columns and a seed, ordering by that random column should return same sorted order |  Critical | SQL | Burak Yavuz | Wenchen Fan |
| [SPARK-9083](https://issues.apache.org/jira/browse/SPARK-9083) | If order by clause has non-deterministic expressions, we should add a project to materialize results of these expressions |  Major | SQL | Yin Huai | Wenchen Fan |
| [SPARK-9398](https://issues.apache.org/jira/browse/SPARK-9398) | Add unit test for null inputs for date functions |  Critical | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9281](https://issues.apache.org/jira/browse/SPARK-9281) | Parse literals as decimal in SQL |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-9430](https://issues.apache.org/jira/browse/SPARK-9430) | Rename IntervalType to CalendarInterval |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8977](https://issues.apache.org/jira/browse/SPARK-8977) | Define the RateEstimator interface, and implement the ReceiverRateController |  Major | DStreams | Iulian Dragos | Iulian Dragos |
| [SPARK-8921](https://issues.apache.org/jira/browse/SPARK-8921) | Add @since tags to mllib.stat |  Minor | Documentation, MLlib | Xiangrui Meng | bimal tandel |
| [SPARK-9016](https://issues.apache.org/jira/browse/SPARK-9016) | Make random forest classifier extend Classifier abstraction |  Minor | ML | holdenk | holdenk |
| [SPARK-9460](https://issues.apache.org/jira/browse/SPARK-9460) | Avoid byte array allocation in StringPrefixComparator |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9462](https://issues.apache.org/jira/browse/SPARK-9462) | Initialize nondeterministic expressions in code gen fallback mode |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9428](https://issues.apache.org/jira/browse/SPARK-9428) | Add test cases for null inputs for expression unit tests |  Blocker | SQL | Yijie Shen | Yijie Shen |
| [SPARK-8005](https://issues.apache.org/jira/browse/SPARK-8005) | Support INPUT\_\_FILE\_\_NAME virtual column |  Major | SQL | Reynold Xin | Joseph Batchik |
| [SPARK-9248](https://issues.apache.org/jira/browse/SPARK-9248) | Closing curly-braces should always be on their own line |  Minor | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9390](https://issues.apache.org/jira/browse/SPARK-9390) | Create an array abstract class ArrayData and a default implementation backed by Array[Object] |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9361](https://issues.apache.org/jira/browse/SPARK-9361) | Refactor new aggregation code to reduce the times of checking compatibility |  Major | SQL | Liang-Chi Hsieh | Liang-Chi Hsieh |
| [SPARK-8174](https://issues.apache.org/jira/browse/SPARK-8174) | date/time function: unix\_timestamp |  Blocker | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8175](https://issues.apache.org/jira/browse/SPARK-8175) | date/time function: from\_unixtime |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8186](https://issues.apache.org/jira/browse/SPARK-8186) | date/time function: date\_add |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8187](https://issues.apache.org/jira/browse/SPARK-8187) | date/time function: date\_sub |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8194](https://issues.apache.org/jira/browse/SPARK-8194) | date/time function: add\_months |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8198](https://issues.apache.org/jira/browse/SPARK-8198) | date/time function: months\_between |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-9133](https://issues.apache.org/jira/browse/SPARK-9133) | Add and Subtract should support date/timestamp and interval type |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-9290](https://issues.apache.org/jira/browse/SPARK-9290) | DateExpressionsSuite is slow to run |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-9463](https://issues.apache.org/jira/browse/SPARK-9463) | Expose model coefficients with names in SparkR RFormula |  Major | ML, SparkR | Eric Liang | Eric Liang |
| [SPARK-7157](https://issues.apache.org/jira/browse/SPARK-7157) | Add approximate stratified sampling to DataFrame |  Minor | SQL | Joseph K. Bradley | Xiangrui Meng |
| [SPARK-9458](https://issues.apache.org/jira/browse/SPARK-9458) | Avoid object allocation in prefix generation |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9469](https://issues.apache.org/jira/browse/SPARK-9469) | TungstenSort should not do safe -\> unsafe conversion itself |  Critical | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9425](https://issues.apache.org/jira/browse/SPARK-9425) | Support DecimalType in UnsafeRow |  Blocker | SQL | Davies Liu | Davies Liu |
| [SPARK-9472](https://issues.apache.org/jira/browse/SPARK-9472) | Consistent hadoop config for streaming |  Minor | DStreams | Cody Koeninger | Cody Koeninger |
| [SPARK-8176](https://issues.apache.org/jira/browse/SPARK-8176) | date/time function: to\_date |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8197](https://issues.apache.org/jira/browse/SPARK-8197) | date/time function: trunc |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-9152](https://issues.apache.org/jira/browse/SPARK-9152) | Implement code generation for Like and RLike |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-9500](https://issues.apache.org/jira/browse/SPARK-9500) | Add TernaryExpression to simplify implementations |  Minor | SQL | Davies Liu | Davies Liu |
| [SPARK-9053](https://issues.apache.org/jira/browse/SPARK-9053) | Fix spaces around parens, infix operators etc. |  Major | SparkR | Shivaram Venkataraman | Yu Ishikawa |
| [SPARK-6885](https://issues.apache.org/jira/browse/SPARK-6885) | Decision trees: predict class probabilities |  Major | ML | Joseph K. Bradley | Yanbo Liang |
| [SPARK-8979](https://issues.apache.org/jira/browse/SPARK-8979) | Implement a PIDRateEstimator |  Major | DStreams | Iulian Dragos | Iulian Dragos |
| [SPARK-8640](https://issues.apache.org/jira/browse/SPARK-8640) | Window Function Multiple Frame Processing in Single Processing Step |  Major | SQL | Herman van Hovell | Herman van Hovell |
| [SPARK-9056](https://issues.apache.org/jira/browse/SPARK-9056) | Rename configuration \`spark.streaming.minRememberDuration\` to \`spark.streaming.fileStream.minRememberDuration\` |  Trivial | DStreams | Tathagata Das | Sameer Abhyankar |
| [SPARK-9510](https://issues.apache.org/jira/browse/SPARK-9510) | Fix remaining SparkR style violations |  Major | SparkR | Shivaram Venkataraman | Shivaram Venkataraman |
| [SPARK-9324](https://issues.apache.org/jira/browse/SPARK-9324) | Add \`unique\` as a synonym for \`distinct\` |  Major | SparkR | Shivaram Venkataraman | Hossein Falaki |
| [SPARK-9322](https://issues.apache.org/jira/browse/SPARK-9322) | Add rbind as a synonym for \`unionAll\` |  Major | SparkR | Shivaram Venkataraman | Hossein Falaki |
| [SPARK-9321](https://issues.apache.org/jira/browse/SPARK-9321) | Add nrow, ncol, dim for SparkR data frames |  Major | SparkR | Shivaram Venkataraman | Hossein Falaki |
| [SPARK-9233](https://issues.apache.org/jira/browse/SPARK-9233) | Enable code-gen in window function unit tests |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-8271](https://issues.apache.org/jira/browse/SPARK-8271) | string function: soundex |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9433](https://issues.apache.org/jira/browse/SPARK-9433) | Audit expression unit tests to test for non-foldable codegen path |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9504](https://issues.apache.org/jira/browse/SPARK-9504) | Flaky test: o.a.s.streaming.StreamingContextSuite.stop gracefully |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9451](https://issues.apache.org/jira/browse/SPARK-9451) | Support records larger than default page size in BytesToBytesMap |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9318](https://issues.apache.org/jira/browse/SPARK-9318) | Add \`merge\` as synonym for join |  Major | SparkR | Shivaram Venkataraman | Hossein Falaki |
| [SPARK-9320](https://issues.apache.org/jira/browse/SPARK-9320) | Add \`summary\` as a synonym for \`describe\` |  Major | SparkR | Shivaram Venkataraman | Hossein Falaki |
| [SPARK-9358](https://issues.apache.org/jira/browse/SPARK-9358) | GenerateUnsafeRowJoiner |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8264](https://issues.apache.org/jira/browse/SPARK-8264) | string function: substring\_index |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9415](https://issues.apache.org/jira/browse/SPARK-9415) | MapType should not support equality & ordering |  Blocker | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-8232](https://issues.apache.org/jira/browse/SPARK-8232) | complex function: sort\_array |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9517](https://issues.apache.org/jira/browse/SPARK-9517) | BytesToBytesMap should encode data the same way as UnsafeExternalSorter |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9480](https://issues.apache.org/jira/browse/SPARK-9480) | Create an map abstract class MapData and a default implementation backed by 2 ArrayData |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-8263](https://issues.apache.org/jira/browse/SPARK-8263) | string function: substr/substring should also support binary type |  Minor | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9520](https://issues.apache.org/jira/browse/SPARK-9520) | UnsafeFixedWidthAggregationMap should support in-place sorting of its own records |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9495](https://issues.apache.org/jira/browse/SPARK-9495) | Support prefix generation for date / timestamp data type |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8269](https://issues.apache.org/jira/browse/SPARK-8269) | string function: initcap |  Major | SQL | Reynold Xin | Cheng Hao |
| [SPARK-8185](https://issues.apache.org/jira/browse/SPARK-8185) | date/time function: datediff |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8188](https://issues.apache.org/jira/browse/SPARK-8188) | date/time function: from\_utc\_timestamp |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-8191](https://issues.apache.org/jira/browse/SPARK-8191) | date/time function: to\_utc\_timestamp |  Major | SQL | Reynold Xin | Adrian Wang |
| [SPARK-9459](https://issues.apache.org/jira/browse/SPARK-9459) | avoid copy for UTF8String during unsafe sorting |  Major | SQL | Davies Liu | Davies Liu |
| [SPARK-9370](https://issues.apache.org/jira/browse/SPARK-9370) | Support DecimalType in UnsafeRow |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-9529](https://issues.apache.org/jira/browse/SPARK-9529) | Improve sort on Decimal |  Critical | SQL | Davies Liu | Davies Liu |
| [SPARK-9531](https://issues.apache.org/jira/browse/SPARK-9531) | UnsafeFixedWidthAggregationMap should be able to turn itself into an UnsafeKVExternalSorter |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9543](https://issues.apache.org/jira/browse/SPARK-9543) | Add randomized testing for UnsafeKVExternalSorter |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9546](https://issues.apache.org/jira/browse/SPARK-9546) | Centralize orderable data type checking |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9404](https://issues.apache.org/jira/browse/SPARK-9404) | UnsafeArrayData |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9542](https://issues.apache.org/jira/browse/SPARK-9542) | create unsafe version of map type |  Major | SQL | Wenchen Fan | Wenchen Fan |
| [SPARK-9549](https://issues.apache.org/jira/browse/SPARK-9549) | minor bug fix in expressions |  Major | SQL | Yijie Shen | Yijie Shen |
| [SPARK-9240](https://issues.apache.org/jira/browse/SPARK-9240) | Hybrid aggregate operator using unsafe row |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9518](https://issues.apache.org/jira/browse/SPARK-9518) | Clean up GenerateUnsafeRowJoiner |  Major | SQL | Reynold Xin | Davies Liu |
| [SPARK-8064](https://issues.apache.org/jira/browse/SPARK-8064) | Upgrade Hive to 1.2 |  Blocker | SQL | Reynold Xin | Steve Loughran |
| [SPARK-9483](https://issues.apache.org/jira/browse/SPARK-9483) | UTF8String.getPrefix only works in little-endian order |  Critical | SQL | Reynold Xin | Matthew Brandyberry |
| [SPARK-9577](https://issues.apache.org/jira/browse/SPARK-9577) | Surface concrete iterator types in various sort classes |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-2016](https://issues.apache.org/jira/browse/SPARK-2016) | rdd in-memory storage UI becomes unresponsive when the number of RDD partitions is large |  Major | Web UI | Reynold Xin | Carson Wang |
| [SPARK-8244](https://issues.apache.org/jira/browse/SPARK-8244) | string function: find\_in\_set |  Minor | SQL | Reynold Xin | Tarek Auel |
| [SPARK-8246](https://issues.apache.org/jira/browse/SPARK-8246) | string function: get\_json\_object |  Major | SQL | Reynold Xin | Nathan Howell |
| [SPARK-9541](https://issues.apache.org/jira/browse/SPARK-9541) | DateTimeUtils cleanup |  Major | SQL | Yijie Shen | Yijie Shen |
| [SPARK-9452](https://issues.apache.org/jira/browse/SPARK-9452) | Support records larger than default page size in UnsafeExternalSorter |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9602](https://issues.apache.org/jira/browse/SPARK-9602) | Remove 'Actor' from the comments |  Major | Build, DStreams, PySpark, Spark Core | Nan Zhu | Nan Zhu |
| [SPARK-6485](https://issues.apache.org/jira/browse/SPARK-6485) | Add CoordinateMatrix/RowMatrix/IndexedRowMatrix in PySpark |  Major | MLlib, PySpark | Xiangrui Meng | Mike Dusenberry |
| [SPARK-8601](https://issues.apache.org/jira/browse/SPARK-8601) | Add an option to disable feature scaling in Linear Regression |  Major | ML | holdenk | holdenk |
| [SPARK-9432](https://issues.apache.org/jira/browse/SPARK-9432) | Audit expression unit tests to make sure we pass the proper numeric ranges |  Blocker | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9513](https://issues.apache.org/jira/browse/SPARK-9513) | Create Python API for all SQL functions |  Blocker | PySpark, SQL | Davies Liu | Davies Liu |
| [SPARK-8231](https://issues.apache.org/jira/browse/SPARK-8231) | complex function: array\_contains |  Major | SQL | Reynold Xin | Pedro Rodriguez |
| [SPARK-9119](https://issues.apache.org/jira/browse/SPARK-9119) | In some cases, we may save wrong decimal values to parquet |  Blocker | SQL | Yin Huai | Davies Liu |
| [SPARK-8359](https://issues.apache.org/jira/browse/SPARK-8359) | Spark SQL Decimal type precision loss on multiplication |  Major | SQL | Rene Treffer | Davies Liu |
| [SPARK-9217](https://issues.apache.org/jira/browse/SPARK-9217) | Update Kinesis Receiver to record sequence numbers |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-8861](https://issues.apache.org/jira/browse/SPARK-8861) | Add basic instrumentation to each SparkPlan operator |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-8862](https://issues.apache.org/jira/browse/SPARK-8862) | Add a web UI page that visualizes physical plans (SparkPlan) |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-6486](https://issues.apache.org/jira/browse/SPARK-6486) | Add BlockMatrix in PySpark |  Major | MLlib, PySpark | Xiangrui Meng | Mike Dusenberry |
| [SPARK-9403](https://issues.apache.org/jira/browse/SPARK-9403) | Implement code generation for In / InSet |  Major | SQL | Reynold Xin | Liang-Chi Hsieh |
| [SPARK-5895](https://issues.apache.org/jira/browse/SPARK-5895) | Add VectorSlicer |  Major | ML | Xiangrui Meng | Xusen Yin |
| [SPARK-7455](https://issues.apache.org/jira/browse/SPARK-7455) | Perf test for LDA (EM/online) |  Major | MLlib | Xiangrui Meng | yuhao yang |
| [SPARK-9611](https://issues.apache.org/jira/browse/SPARK-9611) | UnsafeFixedWidthAggregationMap.destructAndCreateExternalSorter will add an empty entry to if the map is empty. |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-7550](https://issues.apache.org/jira/browse/SPARK-7550) | Support setting the right schema & serde when writing to Hive metastore |  Blocker | SQL | Reynold Xin | Cheng Hao |
| [SPARK-9664](https://issues.apache.org/jira/browse/SPARK-9664) | Use sqlContext.udf to register UDAFs. |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-8266](https://issues.apache.org/jira/browse/SPARK-8266) | string function: translate |  Minor | SQL | Reynold Xin | zhichao-li |
| [SPARK-9615](https://issues.apache.org/jira/browse/SPARK-9615) | Use rdd.aggregate in FrequentItems |  Major | SQL | Burak Yavuz | Burak Yavuz |
| [SPARK-9659](https://issues.apache.org/jira/browse/SPARK-9659) | Rename inSet to isin to match Pandas function |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8978](https://issues.apache.org/jira/browse/SPARK-8978) | Implement the DirectKafkaRateController |  Major | DStreams | Iulian Dragos | Iulian Dragos |
| [SPARK-9556](https://issues.apache.org/jira/browse/SPARK-9556) | Make all BlockGenerators subscribe to rate limit updates |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9630](https://issues.apache.org/jira/browse/SPARK-9630) | Cleanup Hybrid Aggregate Operator. |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9709](https://issues.apache.org/jira/browse/SPARK-9709) | Avoid starving an unsafe operator in a sort |  Blocker | SQL | Andrew Or | Andrew Or |
| [SPARK-9453](https://issues.apache.org/jira/browse/SPARK-9453) | Support records larger than default page size in UnsafeShuffleExternalSorter |  Major | SQL | Josh Rosen | Davies Liu |
| [SPARK-9467](https://issues.apache.org/jira/browse/SPARK-9467) | Specialized accumulators |  Major | Spark Core | Shixiong Zhu | Shixiong Zhu |
| [SPARK-9648](https://issues.apache.org/jira/browse/SPARK-9648) | Name the SQL tab SQL instead of "Sql" |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-8890](https://issues.apache.org/jira/browse/SPARK-8890) | Reduce memory consumption for dynamic partition insert |  Critical | SQL | Reynold Xin | Michael Armbrust |
| [SPARK-9753](https://issues.apache.org/jira/browse/SPARK-9753) | TungstenAggregate should also accept InternalRow instead of just UnsafeRow |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9728](https://issues.apache.org/jira/browse/SPARK-9728) | Support CalendarIntervalType in HiveQL |  Critical | SQL | Reynold Xin | Yijie Shen |
| [SPARK-9752](https://issues.apache.org/jira/browse/SPARK-9752) | Sample operator should avoid row copying and support UnsafeRow |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9777](https://issues.apache.org/jira/browse/SPARK-9777) | Window operator can accept UnsafeRows |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-9763](https://issues.apache.org/jira/browse/SPARK-9763) | Minimize exposure of internal SQL classes |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-8114](https://issues.apache.org/jira/browse/SPARK-8114) | Remove wildcard import on TestSQLContext.\_ |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9729](https://issues.apache.org/jira/browse/SPARK-9729) | Sort Merge Join for Left and Right Outer Join |  Major | SQL | Josh Rosen | Josh Rosen |
| [SPARK-9257](https://issues.apache.org/jira/browse/SPARK-9257) | Fix the false negative of Aggregate2Sort and FinalAndCompleteAggregate2Sort's missingInput |  Minor | SQL | Yin Huai | Yin Huai |
| [SPARK-9646](https://issues.apache.org/jira/browse/SPARK-9646) | Metrics SQL/DataFrame query plans for Spark 1.5 |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-8925](https://issues.apache.org/jira/browse/SPARK-8925) | Add @since tags to mllib.util |  Minor | Documentation, MLlib | Xiangrui Meng | Sudhakar Thota |
| [SPARK-9074](https://issues.apache.org/jira/browse/SPARK-9074) | Expose more of the YARN commandline API to the SparkLauncher |  Major | Spark Core | Erick Tryzelaar | Marcelo Vanzin |
| [SPARK-9849](https://issues.apache.org/jira/browse/SPARK-9849) | DirectParquetOutputCommitter qualified name should be backward compatible |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-3865](https://issues.apache.org/jira/browse/SPARK-3865) | Dimension table broadcast shouldn't be eager |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-9831](https://issues.apache.org/jira/browse/SPARK-9831) | TPCDS Q73 Fails |  Blocker | SQL | Michael Armbrust | Davies Liu |
| [SPARK-9747](https://issues.apache.org/jira/browse/SPARK-9747) | Avoid starving an unsafe operator in an aggregate |  Blocker | SQL | Andrew Or | Andrew Or |
| [SPARK-9907](https://issues.apache.org/jira/browse/SPARK-9907) | Python crc32 is mistakenly calling md5 |  Critical | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9660](https://issues.apache.org/jira/browse/SPARK-9660) | ML 1.5 QA: API: New Scala APIs, docs |  Major | Documentation, ML, MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-9894](https://issues.apache.org/jira/browse/SPARK-9894) | Writing of JSON files with MapType is broken |  Blocker | SQL | Michael Armbrust | Yin Huai |
| [SPARK-9855](https://issues.apache.org/jira/browse/SPARK-9855) | Add expression functions into SparkR whose params are simple |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9908](https://issues.apache.org/jira/browse/SPARK-9908) | TPCDS Q98 failed when tungsten is off |  Blocker | SQL | Davies Liu | Yin Huai |
| [SPARK-9920](https://issues.apache.org/jira/browse/SPARK-9920) | The simpleString of TungstenAggregate does not show its output |  Minor | SQL | Yin Huai | Yin Huai |
| [SPARK-9832](https://issues.apache.org/jira/browse/SPARK-9832) | TPCDS Q98 Fails |  Blocker | SQL | Michael Armbrust | Davies Liu |
| [SPARK-8922](https://issues.apache.org/jira/browse/SPARK-8922) | Add @since tags to mllib.evaluation |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9927](https://issues.apache.org/jira/browse/SPARK-9927) | Revert fix of 9182 since it's pushing the wrong filter down |  Blocker | SQL | Yijie Shen | Yijie Shen |
| [SPARK-8965](https://issues.apache.org/jira/browse/SPARK-8965) | Add ml-guide Python Example: Estimator, Transformer, and Param |  Minor | Documentation, ML, PySpark | Joseph K. Bradley | Rosstin Murphy |
| [SPARK-9580](https://issues.apache.org/jira/browse/SPARK-9580) | Refactor TestSQLContext to make it non-singleton |  Blocker | SQL, Tests | Andrew Or | Andrew Or |
| [SPARK-9661](https://issues.apache.org/jira/browse/SPARK-9661) | ML 1.5 QA: API: Java compatibility, docs |  Major | Documentation, Java API, ML, MLlib | Joseph K. Bradley | Manoj Kumar |
| [SPARK-8670](https://issues.apache.org/jira/browse/SPARK-8670) | Nested columns can't be referenced (but they can be selected) |  Blocker | PySpark, SQL | Nicholas Chammas | Wenchen Fan |
| [SPARK-9966](https://issues.apache.org/jira/browse/SPARK-9966) | Handle a couple of corner cases in the PID rate estimator |  Blocker | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9968](https://issues.apache.org/jira/browse/SPARK-9968) | BlockGenerator lock structure can cause lock starvation of the block updating thread |  Major | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9949](https://issues.apache.org/jira/browse/SPARK-9949) | TakeOrderedAndProject returns wrong output attributes when project is pushed in to it |  Blocker | SQL | Yin Huai | Yin Huai |
| [SPARK-9871](https://issues.apache.org/jira/browse/SPARK-9871) | Add expression functions into SparkR which have a variable parameter |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9950](https://issues.apache.org/jira/browse/SPARK-9950) | Wrong Analysis Error for grouping/aggregating on struct fields |  Blocker | SQL | Michael Armbrust | Wenchen Fan |
| [SPARK-9526](https://issues.apache.org/jira/browse/SPARK-9526) | Utilize randomized tests to reveal potential bugs in sql expressions |  Major | SQL | Yijie Shen | Yijie Shen |
| [SPARK-8920](https://issues.apache.org/jira/browse/SPARK-8920) | Add @since tags to mllib.linalg |  Minor | Documentation, MLlib | Xiangrui Meng | Sameer Abhyankar |
| [SPARK-9787](https://issues.apache.org/jira/browse/SPARK-9787) | Test for memory leaks using the streaming tests in spark-perf |  Major | DStreams | Tathagata Das | Shixiong Zhu |
| [SPARK-8916](https://issues.apache.org/jira/browse/SPARK-8916) | Add @since tags to mllib.regression |  Minor | Documentation, MLlib | Xiangrui Meng | Prayag Chandran Nirmala |
| [SPARK-10007](https://issues.apache.org/jira/browse/SPARK-10007) | Update \`NAMESPACE\` file in SparkR for simple parameters functions |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-10029](https://issues.apache.org/jira/browse/SPARK-10029) | Add Python examples for mllib IsotonicRegression user guide |  Minor | Documentation, MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-10032](https://issues.apache.org/jira/browse/SPARK-10032) | Add Python example for mllib LDAModel user guide |  Minor | Documentation, MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8924](https://issues.apache.org/jira/browse/SPARK-8924) | Add @since tags to mllib.tree |  Minor | Documentation, MLlib | Xiangrui Meng | Bryan Cutler |
| [SPARK-10075](https://issues.apache.org/jira/browse/SPARK-10075) | Add \`when\` expressino function in SparkR |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9967](https://issues.apache.org/jira/browse/SPARK-9967) | Rename the SparkConf property to spark.streaming.backpressure.{enable --\> enabled} |  Minor | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-10060](https://issues.apache.org/jira/browse/SPARK-10060) | User guide for ml trees |  Major | Documentation, ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-10084](https://issues.apache.org/jira/browse/SPARK-10084) | Add Python example for mllib FP-growth user guide |  Minor | Documentation, MLlib | Yanbo Liang | Yanbo Liang |
| [SPARK-9856](https://issues.apache.org/jira/browse/SPARK-9856) | Add expression functions into SparkR whose params are complicated |  Major | SparkR | Yu Ishikawa | Yu Ishikawa |
| [SPARK-8918](https://issues.apache.org/jira/browse/SPARK-8918) | Add @since tags to mllib.clustering |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9899](https://issues.apache.org/jira/browse/SPARK-9899) | JSON/Parquet writing on retry or speculation broken with direct output committer |  Blocker | SQL | Michael Armbrust | Cheng Lian |
| [SPARK-9812](https://issues.apache.org/jira/browse/SPARK-9812) | Test all new Python API examples |  Critical | DStreams, Examples | Tathagata Das | Shixiong Zhu |
| [SPARK-10100](https://issues.apache.org/jira/browse/SPARK-10100) | Eliminate hash table lookup if there is no grouping key in aggregation. |  Major | SQL | Yin Huai | Reynold Xin |
| [SPARK-10108](https://issues.apache.org/jira/browse/SPARK-10108) | Add @Since annotation to mllib.feature |  Minor | Documentation, MLlib | Manoj Kumar | Manoj Kumar |
| [SPARK-9791](https://issues.apache.org/jira/browse/SPARK-9791) | Review API for developer and experimental tags |  Blocker | DStreams | Tathagata Das | Tathagata Das |
| [SPARK-7998](https://issues.apache.org/jira/browse/SPARK-7998) | Improve frequent items documentation |  Major | SQL | Reynold Xin | Burak Yavuz |
| [SPARK-8580](https://issues.apache.org/jira/browse/SPARK-8580) | Test Parquet interoperability and compatibility with other libraries/systems |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-10061](https://issues.apache.org/jira/browse/SPARK-10061) | User guide for ml ensembles (random forest and GBT) |  Major | Documentation, ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-10231](https://issues.apache.org/jira/browse/SPARK-10231) | Update @Since annotation for mllib.classification |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-7456](https://issues.apache.org/jira/browse/SPARK-7456) | Perf test for linear regression and logistic regression with elastic-net |  Major | ML | Xiangrui Meng | DB Tsai |
| [SPARK-10237](https://issues.apache.org/jira/browse/SPARK-10237) | Update @Since annotation for mllib.fpm |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10239](https://issues.apache.org/jira/browse/SPARK-10239) | Update @Since annotation for mllib.pmml |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10244](https://issues.apache.org/jira/browse/SPARK-10244) | Update @Since annotation for mllib.util |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10233](https://issues.apache.org/jira/browse/SPARK-10233) | Update @Since annotation for mllib.evaluation |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10238](https://issues.apache.org/jira/browse/SPARK-10238) | Update @Since annotation for mllib.linalg |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10240](https://issues.apache.org/jira/browse/SPARK-10240) | Update @Since annotation for mllib.random |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10242](https://issues.apache.org/jira/browse/SPARK-10242) | Update @Since annotation for mllib.stat |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10234](https://issues.apache.org/jira/browse/SPARK-10234) | Update @Since annotation for mllib.clustering |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10243](https://issues.apache.org/jira/browse/SPARK-10243) | Update @Since annotation for mllib.tree |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10235](https://issues.apache.org/jira/browse/SPARK-10235) | Update @Since annotation for mllib.regression |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10236](https://issues.apache.org/jira/browse/SPARK-10236) | Update @Since annotation for mllib.feature |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9316](https://issues.apache.org/jira/browse/SPARK-9316) | Add support for filtering using \`[\` (synonym for filter / select) |  Major | SparkR | Shivaram Venkataraman | Felix Cheung |
| [SPARK-9665](https://issues.apache.org/jira/browse/SPARK-9665) | ML 1.5 QA: API: Experimental, DeveloperApi, final, sealed audit |  Critical | ML, MLlib | Joseph K. Bradley | Xiangrui Meng |
| [SPARK-10241](https://issues.apache.org/jira/browse/SPARK-10241) | Update @Since annotation for mllib.recommendation |  Minor | Documentation, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-10252](https://issues.apache.org/jira/browse/SPARK-10252) | Update Spark SQL Programming Guide for Spark 1.5 |  Critical | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-9671](https://issues.apache.org/jira/browse/SPARK-9671) | ML 1.5 QA: Programming guide update and migration guide |  Critical | MLlib | Joseph K. Bradley | Xiangrui Meng |
| [SPARK-9933](https://issues.apache.org/jira/browse/SPARK-9933) | Test the new receiver scheduling |  Major | DStreams | Shixiong Zhu | Shixiong Zhu |
| [SPARK-10440](https://issues.apache.org/jira/browse/SPARK-10440) | Update Spark Streaming Documentation for 1.5 |  Major | Documentation, DStreams | Tathagata Das | Tathagata Das |
| [SPARK-7454](https://issues.apache.org/jira/browse/SPARK-7454) | Perf test for power iteration clustering (PIC) |  Major | MLlib | Xiangrui Meng | Feynman Liang |
| [SPARK-9666](https://issues.apache.org/jira/browse/SPARK-9666) | ML 1.5 QA: model save/load audit |  Major | MLlib | Joseph K. Bradley | yuhao yang |
| [SPARK-9668](https://issues.apache.org/jira/browse/SPARK-9668) | ML 1.5 QA: Docs: Check for new APIs |  Major | Documentation, ML, MLlib | Joseph K. Bradley | Feynman Liang |
| [SPARK-6945](https://issues.apache.org/jira/browse/SPARK-6945) | Provide SQL tab in the Spark UI |  Major | SQL, Web UI | Patrick Wendell | Andrew Or |
| [SPARK-6946](https://issues.apache.org/jira/browse/SPARK-6946) | Add visualization of logical and physical plans for SQL/DataFrames |  Major | SQL, Web UI | Patrick Wendell | Andrew Or |
| [SPARK-3702](https://issues.apache.org/jira/browse/SPARK-3702) | Standardize MLlib classes for learners, models |  Critical | MLlib | Joseph K. Bradley | Joseph K. Bradley |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [SPARK-8145](https://issues.apache.org/jira/browse/SPARK-8145) | Trigger a double click on the span to show full job description |  Major | Web UI | Yuming Wang | Yuming Wang |
| [SPARK-8274](https://issues.apache.org/jira/browse/SPARK-8274) | Fix wrong URLs in MLlib Frequent Pattern Mining Documentation |  Trivial | Documentation, MLlib | Favio Vázquez | Favio Vázquez |
| [SPARK-7666](https://issues.apache.org/jira/browse/SPARK-7666) | MLlib Python doc parity check |  Major | MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8462](https://issues.apache.org/jira/browse/SPARK-8462) | Documentation fixes for Spark SQL |  Minor | Documentation | Lars Francke | Lars Francke |
| [SPARK-7265](https://issues.apache.org/jira/browse/SPARK-7265) | Improving documentation for Spark SQL Hive support |  Trivial | Documentation | Jihong MA | Jihong MA |
| [SPARK-8639](https://issues.apache.org/jira/browse/SPARK-8639) | Instructions for executing jekyll in docs/README.md could be slightly more clear, typo in docs/api.md |  Trivial | Documentation | Rosstin Murphy | Rosstin Murphy |
| [SPARK-3629](https://issues.apache.org/jira/browse/SPARK-3629) | Improvements to YARN doc |  Minor | Documentation, YARN | Matei Zaharia | Neelesh Srinivas Salian |
| [SPARK-8615](https://issues.apache.org/jira/browse/SPARK-8615) | sql programming guide recommends deprecated code |  Minor | Documentation | Gergely Svigruha | Tijo Thomas |
| [SPARK-3258](https://issues.apache.org/jira/browse/SPARK-3258) | Python API for streaming MLlib algorithms |  Major | DStreams, MLlib, PySpark | Xiangrui Meng | Manoj Kumar |
| [SPARK-8769](https://issues.apache.org/jira/browse/SPARK-8769) | toLocalIterator should mention it results in many jobs |  Trivial | Documentation | holdenk | holdenk |
| [SPARK-8457](https://issues.apache.org/jira/browse/SPARK-8457) | Documentation for N-Gram feature transformer |  Trivial | ML | Feynman Liang | Feynman Liang |
| [SPARK-8927](https://issues.apache.org/jira/browse/SPARK-8927) | Doc format wrong for some config descriptions |  Trivial | Documentation | Jon Alter | Jon Alter |
| [SPARK-7555](https://issues.apache.org/jira/browse/SPARK-7555) | User guide update for ElasticNet |  Major | ML | Joseph K. Bradley | Shuo Xiang |
| [SPARK-8278](https://issues.apache.org/jira/browse/SPARK-8278) | Remove deprecated JsonRDD functionality in Spark SQL |  Critical | SQL | Nathan Howell | Reynold Xin |
| [SPARK-9198](https://issues.apache.org/jira/browse/SPARK-9198) | Typo in PySpark SparseVector docs (bad index) |  Minor | Documentation, MLlib, PySpark | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-8002](https://issues.apache.org/jira/browse/SPARK-8002) | Support virtual columns in SQL and DataFrames |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9490](https://issues.apache.org/jira/browse/SPARK-9490) | MLlib evaluation metrics guide example python code uses deprecated print statement |  Trivial | Documentation, MLlib | Seth Hendrickson | Sean Owen |
| [SPARK-9530](https://issues.apache.org/jira/browse/SPARK-9530) | ScalaDoc should not indicate LDAModel.describeTopics and DistributedLDAModel.topDocumentsPerTopic as approximate. |  Minor | MLlib | Meihua Wu | Meihua Wu |
| [SPARK-9149](https://issues.apache.org/jira/browse/SPARK-9149) | Add an example of spark.ml KMeans |  Minor | Examples, ML | Yu Ishikawa | Yu Ishikawa |
| [SPARK-9413](https://issues.apache.org/jira/browse/SPARK-9413) | Support MapType in Tungsten |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9389](https://issues.apache.org/jira/browse/SPARK-9389) | Support ArrayType in Tungsten |  Major | SQL | Reynold Xin | Wenchen Fan |
| [SPARK-9457](https://issues.apache.org/jira/browse/SPARK-9457) | Sorting improvements |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-6805](https://issues.apache.org/jira/browse/SPARK-6805) | MLlib + SparkR integration for 1.5 |  Critical | ML, SparkR | Xiangrui Meng | Eric Liang |
| [SPARK-6906](https://issues.apache.org/jira/browse/SPARK-6906) | Improve Hive integration support |  Blocker | SQL | Michael Armbrust | Michael Armbrust |
| [SPARK-9329](https://issues.apache.org/jira/browse/SPARK-9329) | Bring UnsafeRow up to feature parity with other InternalRow implementations |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9719](https://issues.apache.org/jira/browse/SPARK-9719) | spark.ml NaiveBayes doc cleanups |  Minor | ML, PySpark | Joseph K. Bradley | Feynman Liang |
| [SPARK-9751](https://issues.apache.org/jira/browse/SPARK-9751) | Audit operators to make sure they can support UnsafeRows |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9755](https://issues.apache.org/jira/browse/SPARK-9755) | Add method documentation to MultivariateOnlineSummarizer |  Minor | Documentation, MLlib | Feynman Liang | Feynman Liang |
| [SPARK-8856](https://issues.apache.org/jira/browse/SPARK-8856) | Better instrumentation and visualization for physical plan (Spark 1.5) |  Major | SQL | Reynold Xin | Shixiong Zhu |
| [SPARK-7165](https://issues.apache.org/jira/browse/SPARK-7165) | Sort-merge Join for left/right outer joins |  Blocker | SQL | Adrian Wang | Josh Rosen |
| [SPARK-9713](https://issues.apache.org/jira/browse/SPARK-9713) | Document SparkR MLlib glm() integration in Spark 1.5 |  Critical | Documentation, ML, SparkR | Eric Liang | Eric Liang |
| [SPARK-9575](https://issues.apache.org/jira/browse/SPARK-9575) | Add documentation around Mesos shuffle service and dynamic allocation |  Major | Documentation, Mesos | Timothy Chen | Timothy Chen |
| [SPARK-7583](https://issues.apache.org/jira/browse/SPARK-7583) | User guide update for RegexTokenizer |  Major | Documentation, ML | Joseph K. Bradley | yuhao yang |
| [SPARK-7075](https://issues.apache.org/jira/browse/SPARK-7075) | Project Tungsten (Spark 1.5 Phase 1) |  Major | Block Manager, Shuffle, Spark Core, SQL | Reynold Xin | Reynold Xin |
| [SPARK-5180](https://issues.apache.org/jira/browse/SPARK-5180) | Data source API improvement (Spark 1.5) |  Blocker | SQL | Yin Huai | Cheng Lian |
| [SPARK-9898](https://issues.apache.org/jira/browse/SPARK-9898) | User guide for PrefixSpan |  Major | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-7707](https://issues.apache.org/jira/browse/SPARK-7707) | User guide and example code for KernelDensity |  Major | Documentation, MLlib | Xiangrui Meng | Sandy Ryza |
| [SPARK-9902](https://issues.apache.org/jira/browse/SPARK-9902) | Add Java and Python examples to user guide for 1-sample KS test |  Major | MLlib | Feynman Liang | Jose Cambronero |
| [SPARK-7808](https://issues.apache.org/jira/browse/SPARK-7808) | Scala package doc for spark.ml.feature |  Major | Documentation, ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9900](https://issues.apache.org/jira/browse/SPARK-9900) | User Guide for Association Rule Generation |  Major | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-8473](https://issues.apache.org/jira/browse/SPARK-8473) | Documentation for DCT |  Minor | ML | Feynman Liang | Feynman Liang |
| [SPARK-9705](https://issues.apache.org/jira/browse/SPARK-9705) | outdated Python 3 and IPython information |  Blocker | Documentation, PySpark | Piotr Migdał | Davies Liu |
| [SPARK-8445](https://issues.apache.org/jira/browse/SPARK-8445) | MLlib 1.5 Roadmap |  Critical | ML, MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-8521](https://issues.apache.org/jira/browse/SPARK-8521) | Feature Transformers in 1.5 |  Major | ML | Xiangrui Meng | Xiangrui Meng |
| [SPARK-9208](https://issues.apache.org/jira/browse/SPARK-9208) | Audit DataFrame expression API for 1.5 release |  Blocker | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9895](https://issues.apache.org/jira/browse/SPARK-9895) | User Guide for RFormula Feature Transformer |  Major | ML | Feynman Liang | Eric Liang |
| [SPARK-9242](https://issues.apache.org/jira/browse/SPARK-9242) | Audit both built-in aggregate function and UDAF interface before 1.5.0 release |  Blocker | SQL | Yin Huai | Reynold Xin |
| [SPARK-9846](https://issues.apache.org/jira/browse/SPARK-9846) | User guide for Multilayer Perceptron Classifier |  Major | Documentation, ML | Xiangrui Meng | Alexander Ulanov |
| [SPARK-9864](https://issues.apache.org/jira/browse/SPARK-9864) | Replace \`@since\` JavaDoc tag by \`@Since\` annotation in MLlib |  Critical | Documentation, ML, MLlib | Xiangrui Meng | Manoj Kumar |
| [SPARK-9893](https://issues.apache.org/jira/browse/SPARK-9893) | User guide for VectorSlicer |  Major | ML | Feynman Liang | Xusen Yin |
| [SPARK-7710](https://issues.apache.org/jira/browse/SPARK-7710) | User guide and example code for math/stat functions in DataFrames |  Critical | Documentation, SQL | Xiangrui Meng | Burak Yavuz |
| [SPARK-10118](https://issues.apache.org/jira/browse/SPARK-10118) | Improve SparkR API docs for 1.5 release |  Major | Documentation, SparkR | Shivaram Venkataraman | Yu Ishikawa |
| [SPARK-10214](https://issues.apache.org/jira/browse/SPARK-10214) | Improve SparkR Column, DataFrame API docs |  Major | SparkR | Shivaram Venkataraman | Yu Ishikawa |
| [SPARK-8531](https://issues.apache.org/jira/browse/SPARK-8531) | Update ML user guide for MinMaxScaler |  Minor | ML | yuhao yang | yuhao yang |
| [SPARK-9800](https://issues.apache.org/jira/browse/SPARK-9800) | GradientDescent$.runMiniBatchSGD docs |  Minor | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9797](https://issues.apache.org/jira/browse/SPARK-9797) | Document StreamingLinearRegressionWithSGD default parameter values |  Trivial | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9888](https://issues.apache.org/jira/browse/SPARK-9888) | Update LDA User Guide |  Major | MLlib | Feynman Liang | Feynman Liang |
| [SPARK-7772](https://issues.apache.org/jira/browse/SPARK-7772) | User guide for spark.ml trees and ensembles |  Major | Documentation, ML | Joseph K. Bradley | Joseph K. Bradley |
| [SPARK-9148](https://issues.apache.org/jira/browse/SPARK-9148) | User-facing documentation for NaN handling semantics |  Critical | Documentation, SQL | Josh Rosen | Michael Armbrust |
| [SPARK-9901](https://issues.apache.org/jira/browse/SPARK-9901) | User guide for RowMatrix Tall-and-skinny QR |  Major | MLlib | Feynman Liang | yuhao yang |
| [SPARK-9906](https://issues.apache.org/jira/browse/SPARK-9906) | User guide for LogisticRegressionSummary |  Major | ML | Feynman Liang | Manoj Kumar |
| [SPARK-9680](https://issues.apache.org/jira/browse/SPARK-9680) | Update programming guide section for ml.feature.StopWordsRemover |  Minor | ML | yuhao yang | Feynman Liang |
| [SPARK-9911](https://issues.apache.org/jira/browse/SPARK-9911) | User guide for MulticlassClassificationEvaluator |  Major | ML | Feynman Liang | Manoj Kumar |
| [SPARK-9905](https://issues.apache.org/jira/browse/SPARK-9905) | User guide for LinearRegressionSummary |  Major | ML | Feynman Liang | Feynman Liang |
| [SPARK-9890](https://issues.apache.org/jira/browse/SPARK-9890) | User guide for CountVectorizer |  Major | ML | Feynman Liang | yuhao yang |
| [SPARK-9910](https://issues.apache.org/jira/browse/SPARK-9910) | User guide for train validation split |  Major | ML | Feynman Liang | Martin Zapletal |
| [SPARK-10492](https://issues.apache.org/jira/browse/SPARK-10492) | Update Streaming documentation about rate limiting and backpressure |  Major | Documentation, DStreams | Tathagata Das | Tathagata Das |
| [SPARK-9565](https://issues.apache.org/jira/browse/SPARK-9565) | Spark SQL 1.5.0 QA/testing umbrella |  Critical | SQL | Reynold Xin | Michael Armbrust |
| [SPARK-9566](https://issues.apache.org/jira/browse/SPARK-9566) | Spark 1.5.0 YARN testing umbrella |  Major | YARN | Reynold Xin | Reynold Xin |
| [SPARK-9564](https://issues.apache.org/jira/browse/SPARK-9564) | Spark 1.5.0 Testing Plan |  Critical | Build, Tests | Reynold Xin | Reynold Xin |
| [SPARK-9568](https://issues.apache.org/jira/browse/SPARK-9568) | Spark MLlib 1.5.0 testing umbrella |  Major | MLlib | Reynold Xin | Xiangrui Meng |
| [SPARK-9569](https://issues.apache.org/jira/browse/SPARK-9569) | Spark streaming 1.5.0 testing umbrella |  Critical | DStreams | Reynold Xin | Tathagata Das |
| [SPARK-6116](https://issues.apache.org/jira/browse/SPARK-6116) | DataFrame API improvement umbrella ticket (Spark 1.5) |  Critical | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9424](https://issues.apache.org/jira/browse/SPARK-9424) | Document recent Parquet changes in Spark 1.5 |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-6942](https://issues.apache.org/jira/browse/SPARK-6942) | Umbrella: UI Visualizations for Core and Dataframes |  Major | Spark Core, SQL, Web UI | Patrick Wendell | Andrew Or |
| [SPARK-1856](https://issues.apache.org/jira/browse/SPARK-1856) | Standardize MLlib interfaces |  Critical | MLlib | Xiangrui Meng | Xiangrui Meng |
| [SPARK-7084](https://issues.apache.org/jira/browse/SPARK-7084) | Improve the saveAsTable documentation |  Minor | SQL | madhukara phatak | madhukara phatak |
| [SPARK-8757](https://issues.apache.org/jira/browse/SPARK-8757) | Check missing and add user guide for MLlib Python API |  Major | Documentation, MLlib, PySpark | Yanbo Liang |  |
| [SPARK-7733](https://issues.apache.org/jira/browse/SPARK-7733) | Update build, code to use Java 7 for 1.5.0+ |  Minor | Build, Deploy, Spark Core | Sean Owen | Sean Owen |
| [SPARK-8058](https://issues.apache.org/jira/browse/SPARK-8058) | Add tests for SPARK-7853 and SPARK-8020 |  Major | SQL | Yin Huai | Yin Huai |
| [SPARK-7667](https://issues.apache.org/jira/browse/SPARK-7667) | MLlib Python API consistency check |  Major | MLlib, PySpark | Yanbo Liang | Yanbo Liang |
| [SPARK-8533](https://issues.apache.org/jira/browse/SPARK-8533) | Bump Flume version to 1.6.0 |  Minor | DStreams | Hari Shreedharan | Hari Shreedharan |
| [SPARK-9095](https://issues.apache.org/jira/browse/SPARK-9095) | Removes old Parquet support code |  Major | SQL | Cheng Lian | Cheng Lian |
| [SPARK-8850](https://issues.apache.org/jira/browse/SPARK-8850) | Turn unsafe mode on by default |  Major | SQL | Reynold Xin | Josh Rosen |
| [SPARK-9408](https://issues.apache.org/jira/browse/SPARK-9408) | Refactor mllib/linalg.py to mllib/linalg |  Major | MLlib, PySpark | Manoj Kumar | Manoj Kumar |
| [SPARK-9706](https://issues.apache.org/jira/browse/SPARK-9706) | List Binary and Source Compatibility Issues with japi-compliance checker |  Major | ML, MLlib | Feynman Liang | Feynman Liang |
| [SPARK-9712](https://issues.apache.org/jira/browse/SPARK-9712) | List source compatibility issues in Scala API from scaladocs |  Major | ML, MLlib | Feynman Liang | Feynman Liang |
| [SPARK-8633](https://issues.apache.org/jira/browse/SPARK-8633) | List missing model methods in Python Pipeline API |  Major | ML, PySpark | Xiangrui Meng | Manoj Kumar |
| [SPARK-9754](https://issues.apache.org/jira/browse/SPARK-9754) | Remove TypeCheck in debug package |  Major | SQL | Reynold Xin | Reynold Xin |
| [SPARK-9574](https://issues.apache.org/jira/browse/SPARK-9574) | Review the contents of uber JARs spark-streaming-XXX-assembly |  Major | DStreams | Tathagata Das | Shixiong Zhu |
| [SPARK-9550](https://issues.apache.org/jira/browse/SPARK-9550) | Configuration renaming, defaults changes, and deprecation for 1.5.0 (master ticket) |  Major | Spark Core, SQL | Josh Rosen | Reynold Xin |


