Sample POC for an alternative solution to [COCOON3-105](https://issues.apache.org/jira/browse/COCOON3-105).

# How to build and run

> **IMPORTANT**: be sure to use the latest Cocoon 3 SNAPSHOT artifacts from 
[ASF repository](https://repository.apache.org/content/repositories/snapshots/org/apache/cocoon/)

    $ git clone https://github.com/ilgrosso/cocoon3EmptyProject.git
    $ cd cocoon3EmptyProject
    $ git checkout COCOON3-105
    $ mvn clean package
    $ mvn cargo:run
    
# What you get

Three blocks:
 1. mysample
 2. mysite
 3. mysite2

distributed in two webapps.

## First webapp (mywebapp)

 * [http://localhost:8888/mywebapp/](http://localhost:8888/mywebapp/)<br/>
_mysample_ block featuring all C3 samples

## Second webapp (mywebapp2)

 * [http://localhost:8888/mywebapp2/mysite/](http://localhost:8888/mywebapp2/mysite/)<br/>
_mysite_ welcome page (static HTML)
 * [http://localhost:8888/mywebapp2/mysite/identity.xsl](http://localhost:8888/mywebapp2/mysite/identity.xsl)<br/>
XSLT read from local resources
 * [http://localhost:8888/mywebapp2/mysite2/](http://localhost:8888/mywebapp2/mysite2/)<br/>
_mysite2_ welcome page (static HTML)
 * [http://localhost:8888/mywebapp2/mysite2/identity.xsl](http://localhost:8888/mywebapp2/mysite2/identity.xsl)<br/>
XSLT read from block _mysite_
 * [http://localhost:8888/mywebapp2/mysite2/mysite-welcome](http://localhost:8888/mywebapp2/mysite2/mysite-welcome)<br/>
read block _mysite_'s pipeline
