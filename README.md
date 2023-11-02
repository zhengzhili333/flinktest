# flinktest

I wrote a unit test to verify this method org.apache.flink.yarn.Utils.getYarnAndHadoopConfiguration 
Put UtilsTest in this directory (flink-filesystems\flink-hadoop-fs\target\classes\org\apache\flink\runtime\util),
Run testGetYarnAndHadoopConfiguration inside the test method, after the operation
If this line is normal, the configuration is successfully read from the hdfs-site.xml file
assertEquals(v1, yarnConfiguration.get(k1, null));
However, the following line is incorrect, indicating that the configuration fails to be read from the yarn-site.xml file
assertEquals(v2, yarnConfiguration.get(k2, null));
