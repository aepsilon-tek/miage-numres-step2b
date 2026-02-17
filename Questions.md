# Q1 : Empreinte mémroire en mode JVM ?
Réponse: 214168 KB RSS

# Q2: Temps et  taille  réponse   liste les questions
Temps: 0.517769s
Taille: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Temps: 0.120128s
Taille: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps: 0.073481s
Taille: 1 byte

# Q5 : Empreinte mémoire en mode natif ? - "Natif ne s'execute pas"
Réponse:

# Q6: Temps et  taille  réponse   liste les questions
Temps:
Taille:

# Q7: Temps et  taille  réponse  liste des propositions
Temps:
Taille:

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps:
Taille:


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse: La solution en mode JVM offre une empreinte mémoire raisonnable de 209 MB avec des temps de réponse très rapides.

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse: Implémenter un cache au niveau des endpoints pour les données statiques comme la liste des questions et propositions, ce qui réduirait les temps de réponse et la charge base de données. Également, ajouter une pagination sur l'endpoint /questions et une optimisation des requêtes.
