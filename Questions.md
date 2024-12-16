# Q1 : Empreinte mémroire en mode JVM ?
Réponse:
L'empreinte mémoire (RSS) de l'application en mode JVM est de 223868 KB soit environ 223.9 MB

# Q2: Temps et  taille  réponse   liste les questions
Time: 0.333290s
Size: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Time: 0.071448s
Size: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Time: 0.098186s
Size: 1 bytes

# Q5 : Empreinte mémroire en mode natif ?
Réponse: L'empreinte mémoire (RSS) de l'application en mode Natif est de 2272 KB soit environ 2.3 MB

# Q6: Temps et  taille  réponse   liste les questions
Time: 0.005170s
Size: 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Time: 0.021974s
Size: 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Time: 0.018034s
Size: 1 bytes

# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse:
## Emprunte mémoire
- Solution initiale
    - JVM : 210608 KB
    - Natif : 2268 KB
- Ma solution
    - JVM 
    - Natif
- Votre solution
    - JVM : 223868 KB
    - Natif : 2272 KB

## Temps et taille des réponses - Liste des questions
- Solution initiale
    - JVM : Time: 22.350903s Size: 883 bytes
    - Natif : Time: 17.690825s Size: 883 bytes
- Ma solution
    - JVM
    - Natif
- Votre solution
    - JVM : Time: 0.333290s Size: 158 bytes
    - Natif : Time: 0.005170s Size: 158 bytes

## Temps et taille des réponses - Liste des propositions
- Solution initiale
    - JVM : Time: 12.801599s Size: 609 bytes
    - Natif : Time: 12.701349s Size: 609 bytes
- Ma solution
    - JVM : Time: 0.464554s Size: 571 bytes
    - Natif : 
- Votre solution
    - JVM : Time: 0.021974s Size: 115 bytes
    - Natif : Time: 0.021974s Size: 115 bytes

## Temps et taille des réponses - Évaluation des réponses
- Solution initiale
    - JVM : Time: 0.023343s Size: 1 bytes
    - Natif : Time: 0.001944s Size: 1 bytes
- Ma solution
    - JVM
    - Natif
- Votre solution
    - JVM : Time: 0.098186s Size: 1 bytes
    - Natif : Time: 0.018034s Size: 1 bytes

La solution initiale est très lente (22,3s pour lister les questions en JVM) et consomme beaucoup de mémoire (210608 KB) en raison de traductions inutiles, d’un manque de ciblage des requêtes, et d’un chargement excessif des données.

Ma solution a supprimé les traductions inutiles et optimisé les requêtes en introduisant FetchType.LAZY. Cela a réduit considérablement les temps de réponse (0,46s pour lister les questions), mais sans implémentation de cache, elle reste moins performante que celle des professeurs.

La solution des professeurs a maximisé les performances en supprimant les traductions, les endpoints inutiles, les DTO non nécessaires, et en ajoutant un cache en mémoire. Cela a ramené les temps de réponse à 0,33s en JVM et 0,005s en natif, avec des tailles de réponse réduites au strict nécessaire (158 bytes pour lister les questions).

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:
Une dernière amélioration pourrait être de simplifier la gestion des entités et de réduire les doublons dans les requêtes SQL en optimisant les relations entre Question et Proposal. Actuellement, les propositions et questions sont manipulées séparément, ce qui entraîne des requêtes redondantes et des réponses plus volumineuses.