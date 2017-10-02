---
layout: post
title:  "How to set up Maven environmental variables in Ubuntu (16.04)"
date:   2017-09-27 17:06:34 +1000
categories: ubuntu maven
---
At this point you should have downloaded latest [Maven release from Apache][maven] and extracted it to a preferred location. Now we need to edit .profile /home/user in order to set up Maven environment variables in Ubuntu (16.04). You can either open the /home/user folder and Ctrl+H to view the hidden files and open it. Otherwise, you can open up a terminal and open the file in your favourite text editor as below;

sudo gedit .profile

Add the below to .profile file.

export MAVEN_HOME=/bin/apache-maven-3.5.0

export PATH=$PATH:$MAVEN_HOME/bin

Now restart the system and run the below command in a terminal to verify.

mvn -v

It should result the below;

Apache Maven 3.5.0 (ff8f5e7444045639af65f6095c62210b5713f426; 2017-04-04T05:39:06+10:00)
Maven home: /bin/apache-maven-3.5.0
Java version: 1.8.0_144, vendor: Oracle Corporation
Java home: /usr/lib/jvm/java-8-oracle/jre
Default locale: en_AU, platform encoding: UTF-8
OS name: "linux", version: "4.4.0-96-generic", arch: "amd64", family: "unix"


[maven]: http://maven.apache.org/download.cgi
