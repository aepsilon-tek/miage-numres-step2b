# Q1 : Empreinte mémoire en mode JVM ?
Réponse:Le mode JVM utilise environ 190 Mo.

# Q2: Temps et  taille  réponse   liste les questions
Temps: 0.498101s
Taille: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Temps: 0.039523s
Taille: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps: 0.005138s
Taille: 1 bytes

# Q5 : Empreinte mémoire en mode natif ?
Réponse:Pas pu compiler en natif

# Q6: Temps et  taille  réponse   liste les questions
Temps: Pas pu compiler en natif
Taille: Pas pu compiler en natif

# Q7: Temps et  taille  réponse  liste des propositions
Temps: Pas pu compiler en natif
Taille: Pas pu compiler en natif

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps: Pas pu compiler en natif
Taille: Pas pu compiler en natif


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse: La mémoire utilisée en mode JVM reste similaire autour de 188–190 Mo
Les temps de réponse ont fortement diminué grâce aux optimisations sur les requêtes et le cache des traductions
La taille des réponses reste presque identique et en mode natif, la compilation n’a pas pu être fait 

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:
Mettre en place un cache côté serveur pour éviter de recalculer les questions et propositions
Optimiser la traduction en pré-calculant ou en stockant les résultats pour toutes les catégories
