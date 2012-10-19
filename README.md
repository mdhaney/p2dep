p2dep
=====

Project to build a p2 repository consisting of Eclipse features for 3rd party libraries

Build Instructions
==================
The build must be run in 2 parts, due to a limitation of Maven.  The first run wraps any non-OSGI 
bundles using the Maven Bundle plugin.  The second run builds the Eclipse features and an update site,
which can then be published somewhere or even referenced directly for your target platform.

To do the full build, execute these commands in order:

mvn clean install -P wrap
mvn clean install
