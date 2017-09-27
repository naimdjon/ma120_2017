## Exercise 2. Hadoop WordCount.

The task: 
>given a collection of documents count the number of words in it. Output is for each word the number of times it appears.
Given this document: `this is a test document, is a simple document.`, the output is:
    
        this        1
        is          2
        a           2
        test        1
        document    2
        simple      1

Collection: `news.zip` (It's Learning) under "Exercise 2. WordCount" folder.
*You unzip it and copy it to HDFS. You should already remember how to do it from exercise 1.*

1. Make sure you have java 8 installed. One way to check is as follows. Open a terminal/shell and type:

    java -version

You should get something like:
    
    java version "1.8.0_144"
    Java(TM) SE Runtime Environment (build 1.8.0_144-b01)
    Java HotSpot(TM) 64-Bit Server VM (build 25.144-b01, mixed mode)

2. Install "IntelliJ Idea": www.jetbrains.com/idea.
3. In this exercise you will count the words using `Hadoop MapReduce`. Download the template project "hadoop-word-count". 
First you need to set up the project. Import the project (`pom.xml`) into  Intellij IDEA. Use the template project and change the mapper and reducer code, search for //TODO
When you are done, package your project. From command line, use `./mvnv clean package`.
Finally, you need to `copyFromLocal` the (news) collection to the HDFS. The collection must be uncompressed meaning you have to unzip it first. Run the word counter code. Run the job with the command:
`hadoop jar hadoop-wordcount-1.0-SNAPSHOT.jar WordCounter /user/<your_username>/<your_collection>  /user/<your_username>/output`
4. (Optional) When you see the results, you clearly see that there is a room for improvement. 
 - cleaning up the words
 - removing useless words (stopwords)
 - removing the numbers

Note:  To share a folder between your docker host and the container, you can start the container using the `-v` option:
 `docker run -it -v  /<your_local_folder>/:/hadoop naimdjon/hadoop`. 
  
   The folder will appear as `/hadoop` in your container.

