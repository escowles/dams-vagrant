# dams-vagrant
UCSD DAMS Vagrant Virtual Machine 

## Requirements

* [Vagrant](https://www.vagrantup.com/)
* [VirtualBox](https://www.virtualbox.org/)

## Usage

1. `git clone git@github.com:ucsdlib/dams-vagrant.git`
2. `cd dams-vagrant`
3. `vagrant up`

You can shell into the machine with `vagrant ssh` or `ssh -p 2222 vagrant@localhost`

## Environment

* Ubuntu 14.04 64-bit machine with: 
  * [Tomcat 7](http://tomcat.apache.org) at [http://localhost:8080](http://localhost:8080)
    * Manager username = "tomcat", password = "tomcat"
  * [DAMS Repository](https://github.com/ucsdlib/damsrepo) at [http://localhost:8080/dams](http://localhost:8080/dams)
    * Installed in Tomcat container
    * Data and configuration files in "/pub/dams"
  * [Solr 4.0.0](http://lucene.apache.org/solr/) at [http://localhost:8080/solr](http://localhost:8080/solr), for indexing & searching your content.
    * Installed in Tomcat container
    * Data and configuration files in "/var/lib/tomcat7/solr"

## Thanks

This VM setup was heavily influenced (read: copied) from [Fedora 4 VM](https://github.com/fcrepo4-labs/fcrepo4-vagrant)
