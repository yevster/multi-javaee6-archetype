This archetype will generates a *very basic* multi module Java EE 6 project composed of a parent pom project and 4 nested modules : 

      __artifactId__    : parent pom project
      +---__rootArtifactId__-ear : EAR 6.0 module 
      +---__rootArtifactId__-ejb : EJB 3.1 module
      +---__rootArtifactId__-util: Java Utility module
      +---__rootArtifactId__-web : Web 3.0 module

The application itself is an over architectured hello world app yet no JSF nor persistence are involved. 
The original purpose of this archetype was to test m2e-wtp and some Eclipse server adapters behavior. But it's actually not tied to eclipse in any way so you can use it with any Java IDE.

Pre-Requisites :
-------------------

* JDK 1.8 or later
* maven 3.0 or later


How to build and use the archetype
--------------------------
If you have Maven and Git installed, simply issue the following commands in a terminal to clone this GitHub repositpry and build the archetype with Maven:
    
```bash
    git clone https://github.com/yevster/multi-javaee6-archetype.git
    cd multi-javaee6-archetype
    mvn install archetype:update-local-catalog

    #Update the local catalog
    mvn archetype:crawl
```

 You can now use the archetype from the local catalog:

    mvn archetype:generate -DarchetypeCatalog=local
