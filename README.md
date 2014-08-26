# common-xml

A set of commonly used OGC schemas compiled to XMLBeans bindings and provided as Maven dependencies by 52°North. The 52°North common-xml project organizes some of these standards to be built as Java bindings to ease programming against all those standards. Once compiled standardized XML documents can be created, parsed and validated directly as Java objects.

More information can also be found in the 52°North Wiki: https://wiki.52north.org/bin/view/Documentation/XMLBeansBindings

## Background

The [Open Geospatial Consortium](http://opengeospatial.org) (OGC) offers lots of standards for the 
geospatial Web. Document driven services (like WMS, WCS, SOS, SPS, ...) use a standardized protocols
for communication between a Web service and a client. The XML schemas are derived from the standards 
and serve as one formal model of a standard.

But not only the OGC offers standard documents as XML schemas. The [Organization for the Advancement 
of Structured Information Standards](https://www.oasis-open.org/) or the [World Wide Web Consortium]
(http://www.w3.org/) offer (recommended) standards as XML schemas.


## Repository

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

## Add Dependencies - Examples

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

If you want to use multiple artifacts be sure to use a unique version:

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

## Project Structure

This repository contains a Maven [multi-module project](http://maven.apache.org/guides/mini/guide-multiple-modules.html). The modules can be provided into two types: official/specified schemas, unofficial/not-yet-finally-specified schemas.

For the former modules, the schema files (`.xsd`) provided by the governing organisations are provided in extra modules, namely ``52n-isotc211-schema``, ``52n-oasis-schema`, `52n-ogc-schema` and `52n-w3c-schema`. The bean submodules refererence these submodules as depedencies to include the required schema files.

In case of the latter, the schema files are directly contained within the respective bean submodule in the directory `src/main/xsd`.

## Build Single Module

You can build a specific module with ``mvn clean install -am -pl <module-name>``.
