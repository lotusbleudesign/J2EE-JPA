# JAVA-J2EE
Différentes étapes de création d'application J2E

TP Spring Data JPA location de voiture :

Création d’une application avec une base de données.
Dans ce module, utilisation d’H2, qui est une base de données de type in-memory.

Étapes :

Via Spring, création d’un projet avec :
-	Gradle
-	Ajouter de la librairie Spring data JPA, Spring Web et Spring Boot DevTools 


Importer via un éditeur de type Intellij ou Eclipse et modifier le fichier « build.gradle » les dépendances :

dependencies {

   implementation 'org.springframework.boot:spring-boot-starter-web'
   implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
   runtime("com.h2database:h2")
   testImplementation('org.springframework.boot:spring-boot-starter-test') {
      exclude group: 'org.junit.vintage', module: 'junit-vintage-engine'
   }
}

Activer la console H2 dans le fichier « application.properties »
spring.h2.console.enabled=true 

Builder et relancer le tout.

Vous pouvez tester la console d’H2 :
http://localhost:8080/h2-console 

Ensuite, modifiez l'URL JDBC avec la bonne URL fournie dans la console Eclipse ou Intellij.
jdbc:h2:mem:dca7f3e9-95e2-425d-9ccf-c0aa71824aa1


