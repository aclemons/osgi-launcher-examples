# README

This is a simple example of using the launcher to start an embedded runtime with Apache Felix using the jetty-maven-plugin.

It packages felix and the launcher in WEB-INF/lib and then includes the bundles
to be launched inside a directory WEB-INF/osgi/. The configuration file for the
osgi framework is also included here.

Bundles can be simply added to the existing directories or new directories can
be added to the config and any bundles inside them will be started in the given
order.

You can run the server with

    mvn clean install jetty:run-war -Dorg.slf4j.simpleLogger.defaultLogLevel=trace -Dfelix.cm.dir="$(pwd)"/config
    
The example includes the Felix web console which can be browsed at http://localhost:8080/system/console/

The login credentials are admin:admin.
