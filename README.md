# spark-submit
This repository gives the overall idea regarding spark-submit related concepts

# spark-submit

     spark-submit \
     --master yarn \
     --deploy-mode cluster \
     --conf "spark.sql.shuffle.partitions=20000" \
     --conf "spark.executor.memoryOverhead=5244" \
     --conf "spark.memory.fraction=0.8" \
     --conf "spark.memory.storageFraction=0.2" \
     --conf "spark.serializer=org.apache.spark.serializer.KryoSerializer" \
     --conf "spark.sql.files.maxPartitionBytes=168435456" \
     --conf "spark.dynamicAllocation.minExecutors=1" \
     --conf "spark.dynamicAllocation.maxExecutors=200" \
     --conf "spark.dynamicAllocation.enabled=true" \
     --conf "spark.executor.extraJavaOptions=-XX:+PrintGCDetails -XX:+PrintGCTimeStamps" \ 
     --files /path/log4j.properties,/path/file2.conf,/path/file3.json \
     --class org.apache.spark.examples.SparkPi \
     /spark-home/examples/jars/spark-examples_repace-spark-version.jar 80
