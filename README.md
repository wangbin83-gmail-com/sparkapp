生成maven标准结构：

mvn archetype:generate  -DarchetypeGroupId=com.wangyin.wyrcm.spark  -DarchetypeArtifactId=sparkapp -DarchetypeVersion=1.0-SNAPSHOT -DgroupId=com.wangyin.wyrcm.spark -DartifactId=sample -Dversion=0.1-SNAPSHOT -Dpackage=com.wangyin.wyrcm.spark

其中，需要自定义如下变量：

groupId
artifactId
version
package

编译：

cd sample
export MAVEN_OPTS="-Xmx2g -XX:MaxPermSize=512M -XX:ReservedCodeCacheSize=512m"
mvn -Dhadoop.version=2.0.0-cdh4.7.0 -Dyarn.version=2.0.0-cdh4.7.0 -DskipTests package -U
