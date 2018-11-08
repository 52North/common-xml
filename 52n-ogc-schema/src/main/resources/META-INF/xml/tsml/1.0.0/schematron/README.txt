The schematron schema in this directory have been tested using Probatron4j which is a freely available Java JAR application that implements basic schematron support: http://www.probatron.org/probatron4j.html




The tests may be applied by installing probatron and then calling it using the following syntax:


    java -jar [PathToProbatron]/probatron.jar -r1 [XML file] [schematron file]



Alternatively there is a python script in ../../python that can be used (OGC SVN).

XSD schema-aware functions (such as schema-element) have not been used in these schematron as these are not well supported outside of a couple of commercial implementations. 
