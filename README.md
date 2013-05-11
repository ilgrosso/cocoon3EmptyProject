Sample Cocoon 3 webapp without blocks.

# How to build and run

> **IMPORTANT**: be sure to use the latest Cocoon 3 SNAPSHOT artifacts from 
[ASF repository](https://repository.apache.org/content/repositories/snapshots/org/apache/cocoon/)

    $ git clone https://github.com/ilgrosso/cocoon3EmptyProject.git
    $ cd cocoon3EmptyProject
    $ git checkout SINGLE_WAR
    $ mvn clean package jetty:run
