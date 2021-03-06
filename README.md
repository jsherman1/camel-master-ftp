camel-master-ftp
================

Example Camel project which demonstrate the use of the Camel Master Component in Fuse Fabric with a FTP Endpoint

This project provides and example camel route in blueprint that works should work in JBoss Fuse 6.0 using the Camel Master Component

Camel Router Project for Blueprint (OSGi)
=========================================

The Camel Master Component is only supported in Fuse Fabric container.  A profile should be created
as follows:

    fabric:profile-create --parents camel <profile-name>
    
    fabric:profile-edit --features camel-ftp <profile-name>

    fabric:profile-edit --bunldes mvn:com.example/camel-master-ftp <profile-name>
    
The profile can then be provisioned on a container as follows:

    fabric:container-create-child --profile <profile-name> root mycontainer
    
    or
    
    fabric:container-add-profile mycontainer <profile-name>

For more help see the Apache Camel documentation

    http://camel.apache.org/
    
For more help on Fuse Fabric see the Fabric documentation

    http://fuse.fusesource.org/fabric/index
