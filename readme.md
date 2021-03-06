VJDBC - Remote access for JDBC-Datasources
==========================================

Code fork form original SourceForge Project http://vjdbc.sourceforge.net/


Improvements over original release  (svn revision 72)
+ 'New' RMI Dynamic usage: no need of rmi stub anymore. It is for JDK 1.5 guys.
  http://docs.oracle.com/javase/1.5.0/docs/guide/rmi/relnotes.html
+ Code Cleanup: bumped to jdk 1.8
+ Added HSQL compile dependency because used for caches and testing.





Instructions
------------
Unzip to installation directory.

See index.html in the docs directory.

Required JARs are distributed in the lib subdirectory.

For usage on the client you only need the following JAR files:
   vjdbc.jar
   commons-logging-1.1.jar
   commons-httpclient-3.0.1.jar (optional, replacement for JDK-URLConnections)
   commons-codec-1.3.jar (optional when Jakarta HttpClient is used)

A VJDBC server component needs the following JARs:
   vjdbc.jar
   vjdbc_server.jar
   commons-beanutils-core.jar
   commons-collections-3.2.jar
   commons-dbcp-1.2.1.jar
   commons-digester-1.7.jar
   commons-logging-1.1.jar
   commons-pool-1.3.jar
   jakarta-oro-2.0.8.jar
   log4j-1.2.8.jar (optional)
   + the JAR(s) containing the native JDBC driver(s)

Latest Documentation:

   http://vjdbc.sourceforge.net
   
Other Stuff
-----------
This software is distributed under the terms of the FSF Lesser Gnu Public License (see lgpl.txt).

This product includes software developed by the Apache Software Foundation (http://www.apache.org/).

And Finally ...
---------------

A big THANK YOU to the guys that supported VJDBC with donations. I don't know why the donations
aren't listed on the Sourceforge-Page but the payments definitively arrived.

It's really exciting to see that VJDBC is used in production environments but to get paid for
it makes me really proud.

TODO
---------------
+ Consider incorporating fixes from https://github.com/AugeoSoftware/VJDBC
+ Replaced
   de.simplicit.vjdbc.server.concurrent
  with the jdk concurrent package (probably more secure).
  Anyway it seems used only on an obscure 

+ Code base is old and not perfect.
  The config class has an executor (a bit weird....)
  A statistical log is included upone disconnect.
  There was some minor bad code eclipse catches (null pointer access, but only few).

