
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet

### Classes et héritage
Créer une classe :
```java
public class Ville {

  //Stocke le nom de notre ville
  String nomVille;
  //Stocke le nom du pays de notre ville
  String nomPays;
  //Stocke le nombre d'habitants de notre ville
  int nbreHabitants;

  //Constructeur par défaut
  public Ville(){
    System.out.println("Création d'une ville !");          
    nomVille = "Inconnu";
    nomPays = "Inconnu";
    nbreHabitants = 0;
  }
  
         
}
```
Maintenant on peut créer une instance de la classe Ville dans le main :

```Java
public class Sdz1{ 
  public static void main(String[] args){  
    Ville ville = new Ville(); 
  } 
}
```

    Mais si on veut attribuer un nom données à la ville ? 
    
On peut mettre un constructeur avec des arguments (nomVille, nomPays, etc...), comme ceci :


```Java
//Constructeur avec paramètres
  //J'ai ajouté un « p » en première lettre des paramètres.
  //Ce n'est pas une convention, mais ça peut être un bon moyen de les repérer.
  public Ville(String pNom, int pNbre, String pPays)
  {
    System.out.println("Création d'une ville avec des paramètres !");
    nomVille = pNom;
    nomPays = pPays;
    nbreHabitants = pNbre;
  } 
```



<p style="text-align: right">Source de l'exemple : OpenClassRoom</p>

### Visibilité des objets, classes et attributs

De nombreux langages orientés objet introduisent des attributs de visibilité pour réglémenter l'accès aux classes et aux objets, aux méthodes et aux données.

Il existe 3 modificateurs qui peuvent être utilisés pour définir les attributs de visibilité des entités (classes, méthodes ou attributs) : public, private et protected. Leur utilisation permet de définir des niveaux de protection différents (présentés dans un ordre croissant de niveau de protection offert) :


| Modificateur        | Rôle          |
| ------------- |:-------------:|
| public     | Une variable, méthode ou classe déclarée public est visible par tous les autres objets. Depuis la version 1.0, une seule classe public est permise par fichier et son nom doit correspondre à celui du fichier. Dans la philosophie orientée objet aucune donnée d'une classe ne devrait être déclarée publique : il est préférable d'écrire des méthodes pour la consulter et la modifier |
| par défaut : package friendly     | Il n'existe pas de mot clé pour définir ce niveau, qui est le niveau par défaut lorsqu'aucun modificateur n'est précisé. Cette déclaration permet à une entité (classe, méthode ou variable) d'être visible par toutes les classes se trouvant dans le même package.      | 
| protected | Si une méthode ou une variable est déclarée protected, seules les méthodes présentes dans le même package que cette classe ou ses sous-classes pourront y accéder. On ne peut pas qualifier une classe avec protected.      |
| private | C'est le niveau de protection le plus fort. Les composants ne sont visibles qu'à l'intérieur de la classe : ils ne peuvent être modifiés que par des méthodes définies dans la classe et prévues à cet effet. Les méthodes déclarées private ne peuvent pas être en même temps déclarées abstract car elles ne peuvent pas être redéfinies dans les classes filles.      |

Ces modificateurs d'accès sont mutuellement exclusifs.


Source : https://www.jmdoudoux.fr/java/dej/chap-poo.htm#poo-3


### Designs Patterns

### Swing

Développement d'interfaces graphiques :

Classes Jframe :
  exemple de code :
  
  ------------------------------------------
  import javax.swing.*;
   
  public class TestJFrame1 { 
    public static void main(String argv[]) 
      JFrame f = new JFrame("ma fenetre");
      f.setSize(300,100);
      f.setVisible(true);
    }
  }
  -----------------------------------------
  
  
  
  Utilisation du GetContentPane avec ajout d'un bouton:
  
  ----------------------------------------
  import javax.swing.*;

  public class TestJFrame2 {
     public static void main(String argv[]) {

       JFrame f = new JFrame("ma fenetre");
       f.setSize(300,100);
       JButton b =new JButton("Mon bouton");
       f.getContentPane().add(b);
       f.setVisible(true);
    }
  }
  -----------------------------------------
  
  
  
  Création d'un menu : 
  
  -----------------------------------------
  import javax.swing.*;
  import java.awt.*;


public class TestJFrame6 {
    public static void main(String argv[]) { 

       JFrame f = new JFrame("ma fenetre");
       f.setSize(300,100);
       JButton b =new JButton("Mon bouton");
       f.getContentPane().add(b);
       JMenuBar menuBar = new JMenuBar();
       f.setJMenuBar(menuBar);
       JMenu menu = new JMenu("Fichier");
       menu.add(menuItem);
       menuBar.add(menu);
       f.setVisible(true);

   }
}
 

### Threads

### JDBC

- Définition

de l'acronyme Java DataBase Conectivity.

JDBC est une interface de programmation qui permet au langage Java d'accéder à des bases de données par l'intermédiaire du langage SQL. Comme des interpréteurs Java sont disponibles sur la plupart des postes de travail, cela permet d'écrire des applications indépendantes des bases de données. 

extrait de http://www.journaldunet.com/encyclopedie/definition/340/34/20/java_database_connectivity.shtml


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

extrait de http://www.besoindaide.com/ccm/jdbc/jdbcconnect.htm 

### Fichiers
````Java
//Package à importer afin d'utiliser l'objet File
import java.io.File;

public class Main {
  public static void main(String[] args) {
    //Création de l'objet File
    File f = new File("test.txt");
    System.out.println("Chemin absolu du fichier : " + f.getAbsolutePath());
    System.out.println("Nom du fichier : " + f.getName());
    System.out.println("Est-ce qu'il existe ? " + f.exists());
    System.out.println("Est-ce un répertoire ? " + f.isDirectory());
    System.out.println("Est-ce un fichier ? " + f.isFile());
    System.out.println("Affichage des lecteurs à la racine du PC : ");
 
 for(File file : f.listRoots()){
      System.out.println(file.getAbsolutePath());
      try {
        int i = 1;  
        //On parcourt la liste des fichiers et répertoires
        for(File nom : file.listFiles()){
          //S'il s'agit d'un dossier, on ajoute un "/"
          System.out.print("\t\t" + ((nom.isDirectory()) ? nom.getName()+"/" : nom.getName()));
            if((i%4) == 0){
            System.out.print("\n");
          }
          i++;
        }
        System.out.println("\n");
      } catch (NullPointerException e) {
        //L'instruction peut générer une NullPointerException
        //s'il n'y a pas de sous-fichier !
      }
    }       
  }
}
````
Vous pouvez aussi effacer le fichier grâce la méthodedelete(), créer des répertoires avec la méthodemkdir()(le nom donné à ce répertoire ne pourra cependant pas contenir de point («.»)) etc.  

C'est par le biais des objets FileInputStream et FileOutputStream que nous allons pouvoir :

- lire dans un fichier ;
- écrire dans un fichier.

Ces classes héritent des classes abstraites InputStream et OutputStream, présentes dans le packagejava.io.

Comme vous l'avez sans doute deviné, il existe une hiérarchie de classes pour les traitementsinet une autre pour les traitementsout. Ne vous y trompez pas, les classes héritant d'InputStreamsont destinées à la lecture et les classes héritant d'OutputStreamse chargent de l'écriture !  

Sources : https://openclassrooms.com/courses/apprenez-a-programmer-en-java/les-flux-d-entree-sortie
