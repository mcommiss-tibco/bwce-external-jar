This repo demonstrates the use of 3rd party java libraries in BWCE Projects

It contains a java project to create a 3rd party jar file and a BWCE project which uses it.
It will demon


TIBCO BWCE 2.10.0 (hf3) (including maven plugin)
Java 17
Maven (studio embedded)


Compile / install 3rd jar
==============================
- create a BWCE business studio workspace (javaProject)
- import the project in javaProject into the  workspace
- right click on the JavaExternal.parent/pom.xml
- Debug As ... Maven Install

This will compile the java class and install the jar file into the local maven repo

Use 3rd Party lib in BWCE project
==================================
- create a BWCE business studio workspace (bwceProject)
- import the projects from bwceProject directory into the workspace (important not to use the same workspace as the java project)
- if error on the dependency: right click on one of the projects, Maven... Update project (update all projects).
- right click on JavaExternal.parent/pom.xml
- Debug As ... Maven Install

This will build the ear file which can be found in directory JavaExternal/target.

Opening this ear file (7-zip), then open the included jar file. 
The jar files are included under the lib directory.