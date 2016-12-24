# serverGoogle
<p>A java project with :</p>
<UL TYPE="square">
<LI> Eclipse: Open Source IDE
<LI> Maven: Open Source - Apache build manager for Java projects 
<LI> Apache Tomcat: open-source Java Servlet Container
<LI> Google API: Google API Client Library for Java provides functionality common to all Google APIs, for example HTTP transport, error handling, authentication, JSON parsing, media download/upload, and batching.
</UL>
<BR>
## Sources
<UL TYPE="square">
<LI> <a href="https://developers.google.com/api-client-library/java/">Google Java API</a>
</UL>
<BR>
## Tutorial

### Maven installation
<UL TYPE="square">
<LI> HELP > INSTALL NEW SOFTWARE 
<LI> select in "work with" => "Neon - http://download.eclipse.org/releases/neon"
<LI> find in "General purpose tools" => m2e    for Maven Integration for Eclipse
</UL>

### Maven Web project
<UL TYPE="square">
<LI> PROJECT... > MAVEN PROJECT 
<LI> choose in archetype "Maven-archetype-webapp"
</UL>

### Add Tomcat 7 pluggin
<UL TYPE="square">
<LI> In the pom.xml file add in <build> balise
<LI> nb: /!\ there is no security, ... /!\
</UL>
<BR>
	<plugins>
	<!-- Tomcat plugin -->
	<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.0</version>
	<configuration>
	<path>/</path>
	<port>8080</port>
	</configuration>
	</plugin>
	</plugins>
<BR> 
<UL TYPE="square">
<LI> RUN CONFIGURATION...
<LI> name: Serveur local
<LI> base directorie : ${workspace_loc:/serverGoogle}
<LI> goals : tomcat7:run
<LI> CLOSE > RUN
<LI> go on <a href="http://localhost:8080/">http://localhost:8080/</a>
</UL>




