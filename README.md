# codecoverage
Using cobertura maven plugin
https://wiki.jenkins-ci.org/display/JENKINS/Cobertura+Plugin

In case of multimodule project. you will add below plugin entry in pluginManagement tag
  <plugin>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>cobertura-maven-plugin</artifactId>
    <version>2.2</version>
    <configuration>
      <formats>
        <format>xml</format>
      </formats>
    </configuration>
    <executions>
      <execution>
        <phase>package</phase>
        <goals>
          <goal>cobertura</goal>
        </goals>
      </execution>
    </executions>
</plugin>


And below snippet in every modules' pom file
 <plugin>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>cobertura-maven-plugin</artifactId>
 </plugin>

To publish the result on Jenkins, add cobertura plugin on jenkins
https://wiki.jenkins-ci.org/display/JENKINS/Cobertura+Plugin 
