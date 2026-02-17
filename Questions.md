# Q1 : Empreinte mémroire en mode JVM ?
Réponse:
   2821 197448 java -jar target/quarkus-app/quarkus-run.jar
   3774  2304 grep quarkus-run

   soit 197448KB

# Q2: Temps et  taille  réponse   liste les questions
Time: 0.544215s
Size: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Time: 0.158879s
Size: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Time: 0.104302s
Size: 1 bytes
# Q5 : Empreinte mémroire en mode natif ?
Réponse:
10257  2432 grep quarkus-run

# Q6: Temps et  taille  réponse   liste les questions
Time: 0.005093s
Size: 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Time: 0.010291s
Size: 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Time: 0.004217s
Size: 1 bytes


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse:
La solution tp2b montre des meilleures performances par rapport à la solution initiale:
Une réduction drastique des temps de réponse
Une amélioration nette en mode natif
Une architecture plus sobre
Une meilleure éco-conception

Et des performances presques similaires à ma proposition

Le mode natif apporte un gain très significatif en temps de réponse et en empreinte mémoire, ce qui confirme son intérêt pour des microservices légers.
# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:
Ajouter une pagination sur : /quizz/questions
Une amélioration pertinente serait d’introduire la pagination et/ou la compression HTTP afin de réduire la taille des échanges réseau et d’améliorer encore l’efficacité globale de l’application dans un contexte de montée en charge.