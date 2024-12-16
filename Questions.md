Liste des questions : curl -w "\nTime: %{time_total}s\nSize: %{size_download} bytes\n" http://localhost:8080/quizz/questions
Liste des propositions : curl -w "\nTime: %{time_total}s\nSize: %{size_download} bytes\n" http://localhost:8080/quizz/questions/1/proposals
Evaluation des réponses : curl -w "\nTime: %{time_total}s\nSize: %{size_download} bytes\n" http://localhost:8080/quizz/proposals/evaluate  -H 'accept: application/json'  -H 'content-type: application/json; charset=UTF-8' --data-raw '[{"id":1},{"id":2}]'
# Q1 : Empreinte mémroire en mode JVM ?
Empreinte mémoire en mode JVM : 248 Mo

# Q2: Temps et  taille  réponse   liste les questions
Temps : 0.588000s
Taille : 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Temps : 0.141848s
Taille : 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps : 0.194043s
Taille : 1 byte

# Q5 : Empreinte mémroire en mode natif ?
Réponse: 5682  2256 grep --color=auto quarkus-run

# Q6: Temps et  taille  réponse   liste les questions
Temps : 0.010226s
Taille : 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Temps : 0.035090s
Taille : 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps : 0.016892s
Taille : 1 byte


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
1. Solution initiale :
Problèmes :
Temps de réponse élevé à cause du chargement de toutes les données sans optimisation.
Taille des réponses plus grande, car les relations inutiles (comme les traductions) étaient incluses.
Aucune pagination, donc impact mémoire important.
Temps et taille :
Temps : Plus élevé (~0.5s à ~0.6s pour les requêtes simples).
Taille : Plus grande à cause des champs inutiles.

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse: Mise en cache des réponses fréquemment utilisées
Description :
Mettre en place une couche de cache pour les endpoints fréquemment appelés, tels que :
GET /quizz/questions
GET /quizz/questions/{id}/proposals
et Utiliser Quarkus Cache pour conserver les réponses en mémoire temporairement, réduisant ainsi les appels à la base de données.