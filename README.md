Maven---Hadoop-WordCount
========================
Maven allows a project to build using its project object model (POM) and a set of plugins that are shared by all projects using Maven, providing a uniform build system. Once you familiarize yourself with how one Maven project builds you automatically know how all Maven projects build saving you immense amounts of time when trying to navigate many projects.

First write your Hadoop WordCount.java in any IDE (Eclipse). You can find the program in net or can use wordcount example in my Repo;;WordCount---Hadoop-MapReduce/WordCount.java
Then Right click the project ->Configure ->Convert to Maven Project.
Now a colorful window opens. Click pom.xml.
Here we can setup our pom.xml which is applicable for our project.
So for that we need to set all the dependencies.
While we run hadoop normally in eclipse we include all the jar files in lib right? but here we need to include our dependencies within pom.xml.Dont worry we will get all the dependecies in http://mvnrepository.com/.

Lets create a pom.xml. Example pom.xml for WordCount.java
How to run Maven Project:
1.Right click Project->Maven->Update Project
2.Right Click Project->Maven clean
3.Right Click Project->Maven build
   Here we need to set the goals for our Maven Project
Goal: clean compile package exec:java

Now your Maven WordCount.java is Build Sucess
An error occurs if we didnt set the params.In wordcount we need to supply the arguments : input and output
Lets give that while running the jar.

After Build Sucess if we navigate throught the target folder of our project we can see two jar file.
1.One without dependencies
2.Other with dependencies


In commandLine:
>java -jar WordCount-0.0.1-SNAPSHOT-jar-with-dependencies.jar /input/file/path /output/folder
