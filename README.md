OSGi wrapper for Microsoft SQL Server JDBC driver
=================================================

Overview
--------

This Maven project wraps the Microsoft SQL Server JDBC drivers as OSGi bundles.

Build instructions
------------------

The build depends on the official JDBC driver JAR files provided by Microsoft. 

For example to build the bundles for SQL Server 2012R, follow the steps below.

1. Download the [JDBC drivers for Microsoft SQL Server](https://msdn.microsoft.com/en-us/sqlserver/aa937724.aspx).
2. Extract the package contents.
3. Edit the POM to reflect the Microsoft SQL Server JDBC driver version.
4. Install the driver to the local Maven repository

        mvn install:install-file -Dfile=sqljdbc.jar -DgroupId=com.microsoft -DartifactId=sqljdbc3 -Dversion=4.0.2206.100 -Dpackaging=jar
        mvn install:install-file -Dfile=sqljdbc4.jar -DgroupId=com.microsoft -DartifactId=sqljdbc4 -Dversion=4.0.2206.100 -Dpackaging=jar

5. Build and install the OSGi wrapped driver bundle

        mvn install

Licensing
---------

This Maven build script is licensed under the terms contained in the file named "LICENSE.txt" in this directory.
