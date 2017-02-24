
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet (classes et héritage)

Bonjour les amis !

### Visibilité des objets, classes et attributs

Comment ça va ?

### Designs Patterns

### Swing

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

### Fichiers
