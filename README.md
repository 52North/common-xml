common-xml
==========

A set of commonly used OGC schemas compiled to XMLBeans bindings and provided as Maven dependencies by 52°North.

[![Build Status](https://travis-ci.org/nuest/common-xml.png)](https://travis-ci.org/nuest/common-xml)

Repository
----------

Add the following repositories to your `pom.xml` to get release or snapshots versions respectively.

Releases:

```
[...]
<repository>
  		<id>n52-releases</id>
			<name>52n Releases</name>
			<url>http://52north.org/maven/repo/releases</url>
			<releases>
				<enabled>true</enabled>
			</releases>
			<snapshots>
				<enabled>false</enabled>
			</snapshots>
		</repository>
[...]
```

Snapshots:
```
[...]
		<repository>
			<id>n52-snapshots</id>
			<name>52n Snapshots</name>
			<url>http://52north.org/maven/repo/snapshots/</url>
			<snapshots>
				<enabled>true</enabled>
			</snapshots>
		</repository>
[...]
```

Add Dependencies - Examples
----------

Please 
```
[...]
  <dependency>
  		<groupId>org.n52.sensorweb</groupId>
			<artifactId>52n-xml-kml-v220</artifactId>
			<version>1.0.0</version>
  </dependency>
```
    
