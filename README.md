# Configuration du projet Java avec Maven et JavaFX

## 1. Gestion du projet avec Maven
Notre projet Java utilise **Maven** pour la gestion et la compilation.

Clonage du projet depuis Git
Exécutez la commande suivante pour récupérer le projet :

```
git clone https://github.com/sylvain78saravanane/env-ensitech-java.git
cd env-ensitech
```
Build du projet :

````
mvn clean install
````

and RUN !

```
mvn compile
```



### 📌 **Compilation des tests unitaires avec JUnit**
#### **Ajout de JUnit dans `pom.xml`**
Ajoutez la dépendance suivante pour **JUnit 4.13.2** dans le fichier `pom.xml` :

```xml
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
    <scope>test</scope>
</dependency>
```

#### **Exécution des tests avec Maven**
Utilisez la commande suivante pour exécuter les tests :
```sh
mvn test
```

---

## 2. Configuration de JavaFX

### 📌 **Ajout de la bibliothèque JavaFX dans le projet**

Dans IntelliJ IDEA :
1. **File > Project Structure > Libraries**
2. Cliquez sur **New Project Library**
3. **Ajoutez la bibliothèque JavaFX** (Téléchargez-la si nécessaire : [Gluon JavaFX](https://gluonhq.com/products/javafx/))
4. Création d'un ficher .fxml, qui contient la structure de l'interface graphique de notre application

## 3. Vérification du code avec Checkstyle

📄 **Documentation officielle** : [Checkstyle](https://checkstyle.org/)

### 📌 **Ajout de Checkstyle dans `pom.xml`**
Ajoutez cette dépendance :
```xml
<dependency>
    <groupId>com.puppycrawl.tools</groupId>
    <artifactId>checkstyle</artifactId>
    <version>10.21.4</version>
</dependency>
```

### 📌 **Exécution des vérifications Checkstyle avec Maven**

1. Vérification des erreurs Checkstyle :
```sh
mvn checkstyle:check
```

2. Génération d'un rapport HTML des erreurs sous forme d'un tableau :
```sh
mvn checkstyle:checkstyle
```
📂 **Le fichier HTML est généré dans :**
```
target/site/checkstyle.html
```
