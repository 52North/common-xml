# Official OGC Schemas
This module includes the OGC XML schemas from http://schemas.opengis.net. The files are downloaded and 
represent a snapshot of the official schema repository. Open the timestamp file under 
`src/main/resources/TIMESTAMP.txt`.

## XMLBeans Bindings
The XML schemas provided by this module are packaged as `.jar` archive and can be used as dependency 
while compiling Java XML bindings with [Apache XMLBeans](http://xmlbeans.apache.org/ "Apache XMLBeans").
Once XML bindings have been compiled the schema dependency is not needed anymore.

## License
A license header has been added to each `xsd` and `xml` file to include the license when packaging `xsd` file in the compiled artifact.

As noted before this module contains a snapshot of the official OGC XML schemas which can be accessed 
under http://schemas.opengis.net. Please consider the [schema copyright notices](http://www.opengeospatial.org/ogc/document) 
and the [OGC Copyright Notice and Disclaimers](http://www.opengeospatial.org/ogc/legal). If there are any 
questions left there is also a [copyright FAQ](http://www.opengeospatial.org/ogc/legalfaq).
