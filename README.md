
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet (classes et héritage)

### Visibilité des objets, classes et attributs

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

### Threads

### JDBC

### Fichiers
