### install note

[reference url](http://www.powerxing.com/install-hadoop/)

**url:**
1. http://localhost:8088/cluster
2. http://localhost:50070

hadoop-env.sh set JAVA_HOME

**cmd**
1. start hdfs
  - core-site.xml and hdfs-site.xml
  - hdfs namenode -format
  - start-dfs.sh
  - stop-dfs.sh
  - hdfs dfs -mkdir -p /user/hadoop
2. start yarn
  - mapred-site.xml and yarn-site.xml
  - start-yarn.sh
  - mr-jobhistory-daemon.sh start historyserver
  - stop-yarn.sh
  - mr-jobhistory-daemon.sh stop historyserver
