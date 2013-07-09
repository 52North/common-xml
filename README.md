common-xml
==========

A set of commonly used OGC schemas compiled to XMLBeans bindings and provided as Maven dependencies by 52°North. More information can also be found in the 52°North Wiki: https://wiki.52north.org/bin/view/Documentation/XMLBeansBindings 

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

You can use the dependencies as follows:
```
[...]
<dependency>
	<groupId>org.n52.sensorweb</groupId>
	<artifactId>52n-xml-kml-v220</artifactId>
	<version>1.0.0</version>
</dependency>
[...]
```

If you want to use multiple artifacts we recommend to use a property for the version so that you use artifacts that were build and tested together:

```
[...]
<properties>
	[...]
	<sensorweb.schemas.version>1.1.6-SNAPSHOT</sensorweb.schemas.version>
</properties>
[...]
<dependencies>
[...]
	<dependency>
		<groupId>org.n52.sensorweb</groupId>
		<artifactId>52n-xml-sps-v100</artifactId>
		<version>${sensorweb.schemas.version}</version>
	</dependency>
	<dependency>
		<groupId>org.n52.sensorweb</groupId>
		<artifactId>52n-xml-sos-v100</artifactId>
		<version>${sensorweb.schemas.version}</version>
	</dependency>
</dependencies>
[...]

```

Project Structure
----------

This repository contains a Maven [http://maven.apache.org/guides/mini/guide-multiple-modules.html](multi-module project). The modules can be provided into two types: official/specified schemas, unofficial/not-yet-finally-specified schemas.

For the former modules, the schema files (`.xsd`) provided by the governing organisations are provided in extra modules, namely ``52n-oasis-schema`, `52n-ogc-schema` and `52n-w3c-schema`. This allows, in the case of the OGC which provides schemas at http://schemas.opengis.net/, to directly mirror the online schema structures. The bean submodules refererence these submodules to include the required schema files.

In case of the latter, the schema files are directly contained within the respective bean submodule in the directory `src/main/xsd`.
    
