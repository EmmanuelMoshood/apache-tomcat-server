<h1 align="center">apache-tomcat-appserver</h1>
<!-- <div align="center"> <img src="https://raw.githubusercontent.com/jaiswaladi246/jaiswaladi246/main/banner2.png"> </div> -->
<h3 align="center">Hi my name is Emmanuel and I am passionate about building solutions </h3>

<h2 align="center">STEPS TO DEPLOY AN APPLICAITON FROM GITHUB TO TOMCAT:</h2>

1. setup EC2 instance with Security Group opened for port 8080
2. connect to instance and change hostname to Tomcat
3. install prerequisites, git wget unzip java
4. download and extract Tomcat to a directory in /opt
5. give full access to the directory for anyone to use Tomcat
6. start Tomcat command (sh /opt/TomcatDirectory/bin/startup.sh)
   after creating a soft link for furture access with a naming convention like startTomcat
   (sudo ln -s /opt/tomcat9/bin/startup.sh /usr/bin/starttomcat)
7. create another soft link to use in shuting down Tomcat
   (sudo ln -s /opt/tomcat9/bin/shutdown.sh /usr/bin/stoptomcat)
8. clone the git repo with the built java application to get our .war file
9. move the .war file to /opt/TomcatDirectory/webapps
   10.start Tomcat using the softlink
10. verify that Tomcat is running (ps -ef | grep tomcat) or (curl -v localhost:8080) or (telnet localhost 8080)
