# Demo Docker Worker
A simple Spring Application with the Database Couchbase

# Developer Workspace
[![Try a Factory ](https://codenvy.io/factory/resources/codenvy-contribute.svg)](https://codenvy.io/f?name=Java-couchbase&user=damiencuenot)

# Stack to use

FROM [codenvy/ubuntu_jdk8](https://hub.docker.com/r/codenvy/ubuntu_jdk8/)

and

FROM [dcuenot/couchbase](https://hub.docker.com/r/dcuenot/couchbase/)


# How to run

| #       | Description           | Command  |
| :------------- |:-------------| :-----|
| 1      | Build and copy war | `mvn -f ${current.project.path} clean install && cp ${current.project.path}/target/*.war $TOMCAT_HOME/webapps/ROOT.war` |
| 2      | Run Tomcat      |   `$TOMCAT_HOME/bin/catalina.sh run` |
| 3 | Stop Tomcat      |    `$TOMCAT_HOME/bin/catalina.sh stop` |
| 4 | Tomcat Debug Mode      |    `$TOMCAT_HOME/bin/catalina.sh jpda run` |

