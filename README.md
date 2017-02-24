
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet

### Classes et héritage
Créer une classe :
```java
public class Lapin {

  //Stocke le nom de notre lapin
  String nomLapin;
  //Stocke la race du lapin
  String raceLapin;
  //Stocke le nombre de lapin dans la maison
  int nbreLapins;

  //Constructeur par défaut
  public Lapin(){
    System.out.println("Création d'un lapin !");          
    nomLapin = "Inconnu";
    raceLapin = "Inconnu";
    nbreLapins = 0;
  }
  
         
}
```
Maintenant on peut créer une instance de la classe Ville dans le main :

```Java
public class Appolo 1{ 
  public static void main(String[] args){  
   tortor Appolo = newtortor(); 
  } 
}
```

    Mais si on veut attribuer un nom données à la ville ? 
    
On peut mettre un constructeur avec des arguments (nomVille, nomPays, etc...), comme ceci :


```Java
//Constructeur avec paramètres
  //J'ai ajouté un « p » en première lettre des paramètres.
  //Ce n'est pas une convention, mais ça peut être un bon moyen de les repérer.
  public tortor(String pNom, int pNbre, String pPays)
  {
    System.out.println("Création d'une ville avec des paramètres !");
    spacetown = pville;
    nationspacetown = pPays;
    extraterrestre = pNbre;
  } 
```



<p style="text-align: right">Source de l'exemple : Modifié de OpenClassRoom</p>

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

Les design patterns ou modèles de conception décrivent des organisations pratiques de classes objets. Ces organisations résultent souvent d'une conception empirique, le concepteur objet tente de faciliter la réutilisation et la maintenance du code. On peut donc concevoir un modèle d'application comme une forme d'organisation transposable à plusieurs applications. Ces systèmes peuvent apparaître complèxes aux débutants voire inutiles, il est pourtant très important d'en connaître plusieurs et de les appliquer systématiquement (dans les cas reconnus comme pouvant évoluer). L'architecte objet se construit petit à petit un "panier" de modèles.

Les design patterns ne sont pas rééllement normalisés, mais on peut les découper en trois grandes catégories :

- Les modèles de création : Ces modèles sont très courants pour déléguer à d'autres classes la construction des objets.
- Les modèles de structure : Ces modèles tendent à concevoir des agglomérations de classes avec des macro-composants.
- Les modèles de comportement : Ces modèles tentent de répartir les responsabilités entre chaque classe (l'usage est plutôt dynamique).

Si on voulait faire un parallèle avec UML, les deux premiers modèles seraient liès à des diagrammes statiques (de classes) alors que le dernier modèle est davantage lié à un diagramme dynamique (de séquence).

1) Les modèles de Création :

On se trouve en programmation objet souvent confronté au problème d'évolution des classes. Une classe hérite d'une autre classe pour en spécialiser certains éléments. On aimerait donc qu'un objet puisse appartenir à telle ou telle classe (dans une même famille par héritage) sans avoir à chercher la classe de gestion de ces objets et la ligne de code qui effectue l'instanciation. Si on imagine un cas de création d'un objet pour une classe C donnée, réparti dans différents endroits du code, si on décide de faire évoluer la nature de C en passant par une classe descendante (une classe C' héritant de C), il faut donc reprendre l'intégralité du code de création, avec une classe chargée de la création, plus besoin et seule cette dernière est à reprendre.

2) Les modèles de Structure :

Ces modèles de conception tentent de composer des classes pour bâtir de nouvelles structures. Ces structures servent avant tout à ne pas gérer différemment des groupes d'objets et des objets uniques. Tout le monde en utilisant un logiciel de dessin vectoriel est amené à grouper des objets. Les objets ainsi conçus forment un nouvel objet que l'on peut déplacer, et manipuler sans avoir à répéter ces opérations sur chaque objet qui le compose. On obtient donc une structure plus large mais toujours facilement manipulable.

3) Les modèles de Comportement :

Le modèle de comportement simplifie l'organisation d'exécution des objets. Typiquement, une fonction est composée d'un ensemble d'actions qui parfois appartiennent à des domaines différents de la classe d'implémentation. On aimerait donc pouvoir "déléguer" certains traitement à d'autres classes. D'une manière générale, un modèle de de comportement permet de réduire la complexité de gestion d'un objet ou d'un ensemble d'objet.

4) Pour conclure :

Les Design Patterns représentent un espace très riche de composition ou de simplification de votre développement objet. Nous en avons étudié quelques uns ici, mais il en existe beaucoup d'autres et vous serez également amenés à en trouver de nouveaux. Attention à ne pas se laisser "griser" par ces patterns, trop de patterns est un "anti-pattern", une belle architecture est toujours un équilibre entre le possible et le nécéssaire. L'objectif étant de maximiser le "nécéssaire" et donc de faire de bonnes prévisions. Une mauvaise prévision sera d'autant plus pénalisante que votre projet doit avançer à une certaine cadence.

(Source : http://abrillant.developpez.com/tutoriel/java/design/pattern/introduction/)


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
Pour éviter toute ambiguïté, il est important de préciser qu'un thread n'est pas un processus. En effet, les processus vivent dans des espaces virtuels isolés alors que les threads sont des traitements qui vivent ensemble au sein d'un même processus.

Les threads partagent la même mémoire contrairement aux processus.

Un thread est donc une portion de code capable de s'exécuter en parallèle à d'autres traitements. Ils sont utiles dans bien des cas et parfois même nécessaires comme nous le verrons plus loin dans la section à propos de Swing.

Ils servent à maintes choses par exemple :

 * faire des traitements en tâche de fond, c'est le cas de la coloration syntaxique des éditeurs ;
 * exécuter plusieurs instances d'un même code pour accélérer le traitement, pour de longs traitements n'utilisant pas les mêmes ressources ;
 * s'adresser de manière personnelle à plusieurs clients simultanément comme les serveurs HTTP ou les chats ;
 * résoudre certaines problématiques liées au mode de fonctionnement de Swing.
Contrairement à une autre idée reçue, les threads ne s'exécutent pas en même temps, mais en temps partagé, c'est pour cette raison qu'il est important pour un thread de toujours laisser une chance aux autres de s'exécuter.

Ce n'est pas obligatoire sous Windows, car l'OS utilise un système de gestion de threads dit préemptif, c'est-à-dire qu'il donne et reprend lui-même une fenêtre d'exécution.

Le schéma ci-dessous illustre les temps d'exécution et de latence des threads.

![Texte alternatif](http://alwin.developpez.com/tutorial/JavaThread/images/image594.jpg "Temps d'execution et latence de threads")

La classe thread du package java.lang est celle qui doit impérativement être dérivée pour qu'une classe puisse être considérée comme un thread et donc, exécutable en parallèle.

Cette classe concrète implémente l'interface Runnable. Le code que vous désirez voir exécuter lors de l'activation doit donc être placé dans la méthode run() vue précédemment.

Les principaux constructeurs de la classe thread sont :


`public Thread();
public Thread(Runnable runnable);`

Le lancement d'un thread doit se faire par la méthode start().

* Lancement d'un thread

`MonThread t = new MonThread() ;
t.start();`

Voici un exemple simple d'implémentation de thread.
* Exemple


``public class Monthread extends thread {
  public void run() {
    // faire quelque chose
  }
}``


* Exemple avec passage de paramètre


`public class Monthread extends thread {
  private String str;
  public Monthread(String str) {
    this.str = str;
  }
  public void run() {
    // faire quelque chose avec str
  }
}`

[http://alwin.developpez.com/tutorial/JavaThread/](http://alwin.developpez.com/tutorial/JavaThread/ "Lien vers la source")
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
