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
<UL TYPE="square">
<LI> Download Apache Tomcat from <a href="http://tomcat.apache.org/download-80.cgi#8.5.9"> http://tomcat.apache.org/download-80.cgi#8.5.9</a>
<LI> Unzip
<LI> Servers Tab > No servers are available > create a new server...
<LI> Select Tomcat v8.0 Server and Next
</UL>

### Installation Eclipse

Le tutoriel se base sur la version Eclipse pour JEE, version utilisée Mac OS X (Cocoa) 64-bit :
http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/neon/2/eclipse-jee-neon-2-macosx-cocoa-x86_64.tar.gz

Une fois la version téléchargée il ne reste plus qu'à la dézipper dans le dossier Document et de lancer l'applicatif.


### Installation Tomcat9
<UL TYPE="square">
<LI> Faire apparaitre l'icon Server
<LI> Onglet "Window" > "Show view" > Other...
<LI> Choisir "server" > "servers"
<LI> L'onglet serveur apparait, il fait alors choisir "Click this link to create a new server... "
<LI> Choisir le server Tomcat9
<LI> Aller à la page : http://tomcat.apache.org/download-90.cgi#9.0.0.M15
<LI> Télécharger le plugin :  http://apache.mirror.globo.tech/tomcat/tomcat-9/v9.0.0.M15/bin/apache-tomcat-9.0.0.M15.zip
<LI> Copier le fichier zip dans vos documents
<LI> Sélectionner ce dossier dans eclipse pour "tomcat installation directory"
<LI> Puis valider la fenêtre
<LI> La fenêtre fermée, il apparait dans l'onglet "servers" : Tomcat v9.0 Server at localhost [Stopped, Republish]
<LI> Double cliquer dessus et vérifier que la valeur du port HTTP 1.1 est bien sur 8080
</UL>

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

### Add Tomcat 9 pluggin
<UL TYPE="square">
<LI> In the pom.xml file add in <build> balise
<LI> nb: /!\ there is no security, ... /!\
</UL>



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



<UL TYPE="square">
<LI> RUN CONFIGURATION...
<LI> name: Serveur local
<LI> base directorie : ${workspace_loc:/serverGoogle}
<LI> goals : tomcat7:run
<LI> CLOSE > RUN
<LI> go on <a href="http://localhost:8080/">http://localhost:8080/</a>
</UL>




