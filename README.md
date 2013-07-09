# common-xml

A set of commonly used OGC schemas compiled to xmlbeans bindings.

## Background

The [Open Geospatial Consortium](http://opengeospatial.org) (OGC) offers lots of standards for the 
geospatial Web. Document driven services (like WMS, WCS, SOS, SPS, ...) use a standardized protocols
for communication between a Web service and a client. The XML schemas are derived from the standards 
and serve as one formal model of a standard.

But not only the OGC offers standard documents as XML schemas. The [Organization for the Advancement 
of Structured Information Standards](https://www.oasis-open.org/) or the [World Wide Web Consortium]
(http://www.w3.org/) offer (recommended) standards as XML schemas.

## About

The 52°North common-xml project organizes some of these standards to be built as Java bindings to 
ease programming against all those standards. Once compiled standardized XML documents can be created, 
parsed and validated directly as Java objects.
