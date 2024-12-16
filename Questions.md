# Q1 : Empreinte mémoire en mode JVM ?
Réponse:
   1272 215832 java -jar target/quarkus-app/quarkus-run.jar
   1693  2284 grep --color=auto quarkus-run

La taille de la RSS est de 215832 Ko, soit 215 Mo.

# Q2: Temps et  taille  réponse   liste les questions
Temps: 0.411846s
Taille: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Temps: 0.115652s
Taille: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps: 0.122245s
Taille: 1 bytes

# Q5 : Empreinte mémroire en mode natif ?
Réponse: 
   5705  2316 grep --color=auto quarkus-run

Il y a juste la ligne avec 2 Mo pour quarkus-run, on n'a plus la partir jar.

# Q6: Temps et  taille  réponse   liste les questions
Temps: 0.006782s
Taille: 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Temps: 0.028528s
Taille: 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps: 0.017954s
Taille: 1 bytes

# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse: Cette solution, qui est similaire à ce que nous avions déjà pensé et commencé à implémenter ne possède plus le service de traduction.
Cela rend les requêtes beaucoup plus rapides et cela se constate aux résultats en terme de temps de réponse.

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse: On peut optimiser les requêtes SQL pour limiter le volume de données chargées en mémoire, ajouter la pagination pour éviter les surcharges de mémoire et améliorer les performances, simplifier les requêtes en supprimant les objets inutiles comme les maps et les DTO.
