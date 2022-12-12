# Step 1: Command to check which Operating system you are using
'''
[root@CentOS-7~]$ cat /etc/*release
CentOS Linux release 7.7.1908 (Core)
NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"
CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"
CentOS Linux release 7.7.1908 (Core)
CentOS Linux release 7.7.1908 (Core)
'''
# Step 2: Update the yum package repository:
$ sudo yum update
This will update your system package which includes kernel and dependency package as well. As shown below screenshot.

# Step 3: Check which Java version 
[root@CentOS-7 ~]# java -version
openjdk version "1.8.0_222-ea"
OpenJDK Runtime Environment (build 1.8.0_222-ea-b03)
OpenJDK 64-Bit Server VM (build 25.222-b03, mixed mode)
[root@CentOS-7 ~]#
So, now we’ll install Java 11 and Upgrade Java 8 to Java 11 on CentOS 7

You can also download the Java package, or else follow the below steps.

# Step 4: Command to install JDK 11 in CentOS 7
$ sudo yum install java-11-openjdk-devel
Demo Output:

[root@CentOS-7 ~]# sudo yum install java-11-openjdk-devel
Loaded plugins: fastestmirror, langpacks
Loading mirror speeds from cached hostfile
* base: centos.mirrors.estointernet.in
* extras: centos.mirrors.estointernet.in
* updates: centos.excellmedia.net
Resolving Dependencies
--> Running transaction check
---> Package java-11-openjdk-devel.x86_64 1:11.0.7.10-4.el7_8 will be installed
--> Processing Dependency: java-11-openjdk(x86-64) = 1:11.0.7.10-4.el7_8 for package: 1:java-11-openjdk-devel-11.0.7.10-4.el7_8.x86_64
--> Running transaction check
---> Package java-11-openjdk.x86_64 1:11.0.7.10-4.el7_8 will be installed
--> Processing Dependency: java-11-openjdk-headless(x86-64) = 1:11.0.7.10-4.el7_8 for package: 1:java-11-openjdk-11.0.7.10-4.el7_8.x86_64
--> Running transaction check
---> Package java-11-openjdk-headless.x86_64 1:11.0.7.10-4.el7_8 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

=======================================================================================================================================
Package Arch Version Repository Size
=======================================================================================================================================
Installing:
java-11-openjdk-devel x86_64 1:11.0.7.10-4.el7_8 updates 3.3 M
Installing for dependencies:
java-11-openjdk x86_64 1:11.0.7.10-4.el7_8 updates 217 k
java-11-openjdk-headless x86_64 1:11.0.7.10-4.el7_8 updates 39 M

Transaction Summary
=======================================================================================================================================
Install 1 Package (+2 Dependent packages)

Total download size: 42 M
Installed size: 170 M
Is this ok [y/d/N]: y
Downloading packages:
warning: /var/cache/yum/x86_64/7/updates/packages/java-11-openjdk-11.0.7.10-4.el7_8.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID f4a80eb5: NOKEY
Public key for java-11-openjdk-11.0.7.10-4.el7_8.x86_64.rpm is not installed
(1/3): java-11-openjdk-11.0.7.10-4.el7_8.x86_64.rpm | 217 kB 00:00:03
(2/3): java-11-openjdk-devel-11.0.7.10-4.el7_8.x86_64.rpm | 3.3 MB 00:00:21
(3/3): java-11-openjdk-headless-11.0.7.10-4.el7_8.x86_64.rpm | 39 MB 00:01:09
---------------------------------------------------------------------------------------------------------------------------------------
Total 620 kB/s | 42 MB 00:01:10
Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Importing GPG key 0xF4A80EB5:
Userid : "CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>"
Fingerprint: 6341 ab27 53d7 8a78 a7c2 7bb1 24c6 a8a7 f4a8 0eb5
Package : centos-release-7-7.1908.0.el7.centos.x86_64 (@anaconda)
From : /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Is this ok [y/N]: y
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
Installing : 1:java-11-openjdk-headless-11.0.7.10-4.el7_8.x86_64 1/3
Installing : 1:java-11-openjdk-11.0.7.10-4.el7_8.x86_64 2/3
Installing : 1:java-11-openjdk-devel-11.0.7.10-4.el7_8.x86_64 3/3
Verifying : 1:java-11-openjdk-devel-11.0.7.10-4.el7_8.x86_64 1/3
Verifying : 1:java-11-openjdk-headless-11.0.7.10-4.el7_8.x86_64 2/3
Verifying : 1:java-11-openjdk-11.0.7.10-4.el7_8.x86_64 3/3

Installed:
java-11-openjdk-devel.x86_64 1:11.0.7.10-4.el7_8

Dependency Installed:
java-11-openjdk.x86_64 1:11.0.7.10-4.el7_8 java-11-openjdk-headless.x86_64 1:11.0.7.10-4.el7_8

Complete!

# Step 5: Install OpenJDK 11 JRE 
sudo yum install java-11-openjdk
JRE is a subset of JDK, and if you already installed the JDK package, you do not need to install this one. You can try with the below command.

Demo output

[root@CentOS-7 ~]# sudo yum install java-11-openjdk

Loaded plugins: fastestmirror, langpacks
Loading mirror speeds from cached hostfile
 * base: centos.mirrors.estointernet.in
 * extras: centos.mirrors.estointernet.in
 * updates: centos.excellmedia.net
Package 1:java-11-openjdk-11.0.7.10-4.el7_8.x86_64 already installed and latest version
Nothing to do

[root@CentOS-7 ~]#
Set the default Java 11 version on CentOS 7 
We will replace the default java version from Java 8 to Java 11 version.


This method is to follow when you have multiple Java versions installed on a server, and now you want to set anyone default java version. This can be done with the alternatives system utility. 

Step 1: Command to set default Java version
$ sudo alternatives --config java
Just enter the number when prompted which will change the default java version.

Demo Output:

[root@CentOS-7 ~]# sudo alternatives --config java

There are 3 programs which provide 'java'.


  Selection    Command

-----------------------------------------------

   1           java-1.7.0-openjdk.x86_64 (/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.221-2.6.18.1.el7.x86_64/jre/bin/java)

*+ 2           java-1.8.0-openjdk.x86_64 (/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.222.b03-1.el7.x86_64/jre/bin/java)

   3           java-11-openjdk.x86_64 (/usr/lib/jvm/java-11-openjdk-11.0.7.10-4.el7_8.x86_64/bin/java)


Enter to keep the current selection[+], or type selection number: 3

[root@CentOS-7 ~]#
Step 2: Verify Java version
$ java -version
Demo output:

[root@CentOS-7 ~]# java -version
openjdk version "11.0.7" 2020-04-14 LTS
OpenJDK Runtime Environment 18.9 (build 11.0.7+10-LTS)
OpenJDK 64-Bit Server VM 18.9 (build 11.0.7+10-LTS, mixed mode, sharing)
[root@CentOS-7 ~]#
How to Set JAVA_HOME Environment Variable
Step 1: Locate where Java is installed (Java path)
From the below command, you will get the exact java path

$ sudo update-alternatives --config java
Steps to Upgrade Java 8 to Java 11 on CentOS 7
Once you get the above output press the Ctrl+C button so that it will exit. The intention of this command is to get only the path where Java 11 is installed.

From the above output, you can get the path for each Java version that is installed on the system.

#--> path for Java 7
/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.221-2.6.18.1.el7.x86_64/jre/bin/java  

#--> path for Java 8
/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.222.b03-1.el7.x86_64/jre/bin/java 

#--> path for Java 11
/usr/lib/jvm/java-11-openjdk-11.0.7.10-4.el7_8.x86_64/bin/java
As we have configured Java 11, so copy the path from above.

Step 2: Add Java path at the end of the “~/.bash_profile” file
Add path at the end of the line in the “~/.bash_profile” file.
vim ~/.bash_profile

JAVA_HOME="/usr/lib/jvm/java-11-openjdk-11.0.7.10-4.el7_8.x86_64/bin/java"
Another way to configure JAVA_HOME is by adding the below the line in ~/.bash_profile.

export JAVA_HOME=$(readlink -f /usr/bin/java | sed "s:/bin/java::")
Step 3: Verify bash profile
source ~/.bash_profile
echo $JAVA_HOME
