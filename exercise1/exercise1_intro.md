In this exercise we will setup an environment on your machine. There are two methods to run the exercise: 

1. **Manual**. Install the following:
 * java
 * maven
 * hadoop
2. **docker** base image `sequenceiq/hadoop-docker:2.7.1` (recommended)


### Method 1. Manual.
1. Download java:

    <http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>

Accept and choose the installation file depending on your platform.
For windows users, install it on `C:\java` or other place without space in the filename.

For linux users, if you use apt-get or yum.

2. Download maven (if you don't have it already).

<http://apache.uib.no/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.zip>

Setup your path so maven is available from command line.

Linux: `export PATH=<path_where_you_extracted_zip>/bin:$PATH`

Windows: Open Environmental variables, e.g. http://bit.ly/1iW3PV0  : Find variable "path" and append the `<maven path>/bin`

Check in the command line if `mvn -version` works.

### Method 2. Docker.
The base image can be obtained from docker hub.
1. Install docker (if you don't have it). 
2. Run: `docker run -it naimdjon/hadoop /start`
3. You can find hadoop at `/opt/hadoop/latest/`.
4. Run a sample command, for example list: `hadoop fs -ls`


Check the following commands:

 * `-ls`
 * `-mkdir`
 * `-copyFromLocal`
 * `-moveFromLocal`
 * `-copyToLocal`
 * `-cat`

