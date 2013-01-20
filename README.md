sso-embedded-tomcat
===================

Enable SSO in embedded tomcat instance


Steps:

 1. Install the two webapplications as artifacts  
    ```mvn install:install-file -Dfile=src/main/resources/examples.war  -DgroupId=apache.tomcat -DartifactId=examples -Dversion=1.0.0 -Dpackaging=war``` 
    ```mvn install:install-file -Dfile=src/main/resources/examples.war  -DgroupId=apache.tomcat -DartifactId=examples2 -Dversion=1.0.0 -Dpackaging=war```
   

 2. Run the project:  
    ```mvn clean install```
    This deploys the two webapplications in an embedded tomcat instance.
  
  
 3. Access the protected resources in the two web-applications  
    
    http://localhost:8080/examples/jsp/security/protected/index.jsp?role=test  
    http://localhost:8080/examples2/jsp/security/protected/index.jsp?role=test  
    
    Login using **admin/password**

    The users are configured in src/main/tomcatconf/tomcat-users.xml

