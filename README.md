KeyBox
======

About
-----
A web-based ssh console to execute commands and manage multiple systems
simultaneously. KeyBox allows you to share terminal commands and upload files to
all your systems. Once the sessions have been opened you can select a single
system or any combination to run your commands.  Additional system
administrators can be added and their terminal sessions and history can be
audited. Also, KeyBox can manage and distribute public keys that have been setup
and defined.

Screenshots
-----------

![Terminals](https://freecode.com/screenshots/64/42/64429c74e1a5b4d9b7d26c490282150a_medium.png)

![More Terminals](https://freecode.com/screenshots/a0/44/a044b3e11cc1af453e8fe5b9731bd6a5_medium.png)

![Upload Files](https://freecode.com/screenshots/e6/76/e676fe542b08188cff1fdbceea15adf4_medium.png)

![Manage Systems](https://freecode.com/screenshots/71/e6/71e6464744ae95d2d03ab5bbe5a576e1_medium.png)

![Manage Users](https://freecode.com/screenshots/c0/a3/c0a3b758c80c3a634e3327f55c4293f2_medium.png)

![Define SSH Keys](https://freecode.com/screenshots/16/f9/16f94a2734f3b509df2dca9efe79cbc5_medium.png)


Prerequisites
-------------
Java JDK 1.7 or greater
http://www.oracle.com/technetwork/java/javase/overview/index.html

Browser with Web Socket support
http://caniuse.com/websockets

**Note: In Safari if using a self-signed certificate you must import the certificate into your Keychain.
Select 'Show Certificate' -> 'Always Trust' when prompted in Safari

Must run on *nix with OpenSSH version 2

Maven 3 or greater  ( Only needed if building from source )
http://maven.apache.org

To Run Bundled with Jetty
------
If your not big on the idea of building from source...

Download keybox-jetty-vXX.XX.tar.gz

https://github.com/skavanagh/KeyBox/releases

Export environment variables

     export JAVA_HOME=/path/to/jdk
     export PATH=$JAVA_HOME/bin:$PATH

Start KeyBox

        ./startKeyBox.sh

How to Configure SSL in Jetty
(it is a good idea to add or generate your own unique certificate)

http://wiki.eclipse.org/Jetty/Howto/Configure_SSL

To Build from Source
------
Export environment variables

    export JAVA_HOME=/path/to/jdk
    export M2_HOME=/path/to/maven
    export PATH=$JAVA_HOME/bin:$M2_HOME/bin:$PATH

In the directory that contains the pom.xml run

	mvn package jetty:run

**Note: Doing a mvn clean will delete the H2 DB and wipe out all the data.

Using KeyBox
------
Open browser to https://\<whatever ip\>:8443

Login with

	username:admin
	password:changeme

Steps:

1. Create systems
2. Create profiles
3. Assign systems to profile
4. Assign profiles to users
5. Users can login to create sessions on assigned systems
6. Start composite-ssh sessions or create and execute a script across multiple sessions
7. Add additional public keys to systems
8. Audit session history

Author
------
**Sean Kavanagh**

+ sean.p.kavanagh6@gmail.com
+ https://twitter.com/spkavanagh6


