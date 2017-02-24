
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet (classes et héritage)

### Visibilité des objets, classes et attributs

### Designs Patterns

### Swing

### Threads

### JDBC

- Définition

de l'acronyme Java DataBase Conectivity.

JDBC est une interface de programmation qui permet au langage Java d'accéder à des bases de données par l'intermédiaire du langage SQL. Comme des interpréteurs Java sont disponibles sur la plupart des postes de travail, cela permet d'écrire des applications indépendantes des bases de données. 

extrait de http://www.journaldunet.com


- Connexion à la base de données

Pour se connecter à une base de données il est essentiel de charger dans un premier temps le pilote de la base de données à laquelle on désire se connecter grâce à un appel au DriverManager (gestionnaire de pilotes) :
```java
Class.forName("nom.de.la.classe");
```
Cette instruction charge le pilote et crée une instance de cette classe. Pour se connecter à une base de données déclarée dans l'administrateur ODBC par exemple, il faut charger le pilote JDBC-ODBC (appelé pont JDBC-ODBC) :
```java
Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
```
Certains compilateurs refusant cette notation, il faut parfois appeler le driver de la façon suivante :
```java
Class.forName("sun.jdbc.odbc.JdbcOdbcDriver").newInstance();
```
Pour se connecter à une base de données particulière, il s'agit ensuite de créer une instance de la classe Connection grâce à la méthode getConnection de l'objet DriverManager en indiquant la base de données à charger à l'aide de son URL
```java
String url = "jdbc:odbc:base_de_donnees";

Connection con = DriverManager.getConnection(url);
```
Le nom de la base de données (ici base_de_donnees) étant celle déclarée dans le panneau de configuration ODBC, c'est-à-dire le nom du DSN. La syntaxe de l'URL peut varier légèrement selon le type de la base de données. Il s'agit généralement d'une adresse de la forme :
```java
jdbc:sousprotocole:nom
```

extrait de http://www.besoindaide.com 

### Fichiers
