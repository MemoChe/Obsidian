In case of Fedora it is as simple as putting `sudo dnf install tomcat` and then start our server in `sudo systemctl start tomcat.service`. The path to place our applications is in /var/lib/tomcat/webapps/.

`TOMCATS_BASE="/var/lib/tomcats/"` => It is the path where we will put our .war files.
`JAVA_HOME="/usr/lib/jvm/jre"` => 
`CATALINA_HOME="/usr/share/tomcat"`