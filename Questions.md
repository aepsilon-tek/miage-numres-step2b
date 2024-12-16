# Q1 : Empreinte mémroire en mode JVM ?
Réponse:
205020
# Q2: Temps et  taille  réponse   liste les questions
Time: 0.338410s
Size: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Time: 0.072448s
Size: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Time: 0.107892s
Size: 1 bytes

# Q5 : Empreinte mémroire en mode natif ?
Réponse:2.16MO

# Q6: Temps et  taille  réponse   liste les questions
Temps:0.005521s
Taille:149 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Temps::0.018300S
Taille:109 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps:0.012581S
Taille:1 bytes


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse:
La suppression des appels à l'API de traduction, qui n'étaient pas indispensables, a permis d'accélérer considérablement le temps de réponse de nos APIs. En éliminant ces appels, le temps de réponse de l'API listerQuestions a été réduit de 15 secondes.

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse:Il serait avisé de mettre en place un mécanisme de mise en cache côté serveur afin d'optimiser l'accès aux données les plus sollicitées. 
