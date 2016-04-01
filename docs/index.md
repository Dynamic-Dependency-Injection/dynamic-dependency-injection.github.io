# Welcome to Dynamic Dependency Injection 
Here we are working on Dynamic-Dependency-Injection. You could find this 
repo on Github -> [Dynamic-Dependency-Injection](https://github.com/Dynamic-Dependency-Injection/dynamic-cdi)

## Basics about DI -Frameworks
If you want to know a little bit more about DI-Frameworks and the comparison between some of them
you could read the following.

<iframe src="//www.slideshare.net/slideshow/embed_code/key/1EJNXuXiXQrT9r" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/svenruppert/di-frameworks-hidden-pearls-20151118001" title="DI Frameworks - hidden pearls" target="_blank">DI Frameworks - hidden pearls</a> </strong> from <strong><a target="_blank" href="//www.slideshare.net/svenruppert">Sven Ruppert</a></strong> </div>

Or if you want to see it as a talk...

<iframe width="560" height="315" src="https://www.youtube.com/embed/i1_Jah55FKc?list=PLjDsqKgqBKbn4RDBDUxJ6HtxayJt6Rca3" frameborder="0" allowfullscreen></iframe>

## What goal we want to reach?
After a longer time using differend DI-Frameworks I decided to start with an internal research project to explore the possibilities to write a different DI-Framework. Something that would fit better to my needs to work with old and big legacy projects. Based on the ProxyBuilder - [www.proxybuilder.org](http://www.proxybuilder.org) that was born during the time
I was writing the german Book ***"Dynamic Proxies"*** with [Dr. Heinz Kabutz](http://www.javaspecialists.eu/), I started to use this for the implementations of my first version of the ***Dynamic Dependency Injection***  project. 

The goals I wanted to reach are:

+ as less as possible Binding Code
+ easy and simple Lifecycle
+ technical and business Model-Validation
+ easy debugging
+ easy mocking
+ Dynamic Context
+ only dependency to the JDK itself  

## Jump start 

If you want to start using this project inside your project you could start with the following dependency 
inside your ***pom.xml***

```xml
    <dependency>
      <groupId>org.rapidpm.dynamic-cdi</groupId>
      <artifactId>rapidpm-dynamic-cdi</artifactId>
      <version>***VERSION***</version>
    </dependency>
```

If you are using releases only you will get them from maven central. But if you want to use the developer snapshots too,
you have to use the maven central SNAPSHOT repository.

Add the following to your ***settings.xml*** to get the snapshots.
```
   <profile>
      <id>allow-snapshots</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <repositories>
        <repository>
          <id>snapshots-repo</id>
          <url>https://oss.sonatype.org/content/repositories/snapshots</url>
          <releases>
            <enabled>false</enabled>
          </releases>
          <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
          </snapshots>
        </repository>
      </repositories>
    </profile>
```
