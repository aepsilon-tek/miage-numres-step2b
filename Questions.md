# Q1 : Empreinte mémroire en mode JVM ?
Réponse:

   1190 211676 java -jar target/quarkus-app/quarkus-run.jar
   1388  2252 grep --color=auto quarkus-run

212676 Kb

# Q2: Temps et  taille  réponse   liste les questions
Time: 0.402064s
Size: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Time: 0.079923s
Size: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Time: 0.110824s
Size: 1 bytes

# Q5 : Empreinte mémroire en mode natif ?
Réponse:
4790  2284 grep --color=auto quarkus-run

2284 KB

# Q6: Temps et  taille  réponse   liste les questions
Time: 0.005864s
Size: 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Time: 0.035017s
Size: 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Time: 0.015085s
Size: 1 bytes

# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse:

Concernant la solution initiale vs celle-ci :

## Initiale : Temps et  taille  réponse   liste les questions
Temps: 20.259968s
Taille: 883 bytes

## Initiale :  Temps et  taille  réponse  liste des propositions
Temps: 11.241979s
Taille: 609 bytes

## Initiale :  Temps et  taille  réponse  évaluation les réponses
Temps: 0.001795s
Taille: 1 bytes

Nous constatons une très grande différence des résultats en mode JVM. Par rapport à la version initiale, celle-ci n'utilise pas le service DTO, ni même le service de traduction. De plus, Nous n'utilisons plus de QuizzService, mais un QuizzRessource, l'approche est différente, mais visiblement plus efficace.

La différence majeure entre QuizzService et QuizzResource est principalement leur rôle : QuizzService est une couche métier qui encapsule la logique de traitement des questions et propositions. Elle encapsule les accès à la base de données avec des traitements supplémentaires.
QuizzResource est une interface REST qui expose ces fonctionnalités via des endpoints HTTP pour les clients externes. Elle expose directement les entités Question et Proposal sans transformation en DTO. Cela signifie qu'elle retourne les objets tels quels.

Ma Solution ressemble à la logique de celle-ci pour retirer le service de traduction et de DTO. Mais garde la même logique que l'initiale. Les résultat sont donc plus rapides, quasi similaires que celle-ci.


# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:

Gestion des entités, réduire les doublons généré avec la nouvelle approche.
