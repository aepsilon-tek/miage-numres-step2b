# Q1 : Empreinte mémroire en mode JVM ?
Réponse:L'application utilise une empreinte mémoire de 174,49 Mo en mode JVM.

# Q2: Temps et  taille  réponse   liste les questions
Temps : 0,487 secondes
Taille : 158 octets

# Q3: Temps et  taille  réponse  liste des propositions
Temps : 0,088 secondes
Taille : 115 octets

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps : 0,067 secondes
Taille : 1 octet

# Q5 : Empreinte mémroire en mode natif ?
Réponse:L'application utilise une empreinte mémoire de 2,34 Mo en mode natif.

# Q6: Temps et  taille  réponse   liste les questions
Temps : 0,002 secondes
Taille : 158 octets

# Q7: Temps et  taille  réponse  liste des propositions
Temps : 0,016 secondes
Taille : 115 octets

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps : 0,008 secondes
Taille : 1 octet


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse:Nous avons observé que les appels à l'API de traduction, bien que non nécessaires, ralentissaient significativement le temps de réponse des APIs, notamment l'API listerQuestions. En supprimant ces appels inutiles, le temps de réponse de l'application a été réduit de 20 secondes pour cette API.

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:Une optimisation supplémentaire consisterait à activer le cache d'Hibernate pour améliorer les performances en réduisant les appels répétitifs à la base de données.
