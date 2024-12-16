# Q1 : Empreinte mémroire en mode JVM ?
Réponse: 204124 KB (environ 204 MB)

# Q2: Temps et  taille  réponse   liste les questions
Temps: 0.374015s
Taille: 158 bytes

# Q3: Temps et  taille  réponse  liste des propositions
Temps: 0.076822s
Taille: 115 bytes

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps: 0.109887s
Taille: 1 bytes

# Q5 : Empreinte mémroire en mode natif ?
Réponse: 2264 KB (environ 2 MB)

# Q6: Temps et  taille  réponse   liste les questions
Temps: 0.005734s
Taille: 158 bytes

# Q7: Temps et  taille  réponse  liste des propositions
Temps: 0.021242s
Taille: 115 bytes

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps: 0.014727s
Taille: 1 bytes

# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
Réponse: Les améliorations sont significatives entre le mode JVM et le mode natif :
- Empreinte mémoire : réduction de 204MB à 2MB (98% de réduction)
- Temps de réponse :
  * Liste questions : 0.374s → 0.005s (98% plus rapide)
  * Liste propositions : 0.076s → 0.021s (72% plus rapide)
  * Évaluation : 0.109s → 0.014s (87% plus rapide)
La taille des réponses reste identique car c'est la même donnée.

En comparant les trois solutions :

1. Solution 2a (avec traductions) :
   - JVM: 217MB, Native: 2.2MB
   - Temps listing questions: 18.9s
   - Temps listing propositions: 13.2s
   - Taille réponses plus importantes (883/609 bytes)

2. Solution 2b (simplifiée) :
   - JVM: 204MB, Native: 2MB
   - Temps listing questions: 0.374s → 0.005s
   - Temps listing propositions: 0.076s → 0.021s
   - Taille réponses optimisées (158/115 bytes)

Les différences majeures :
- Suppression du système de traduction = gains importants en temps de réponse
- Simplification des DTOs = réduction taille des réponses
- Architecture plus légère = empreinte mémoire réduite

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
Réponse: Plusieurs améliorations possibles :
1. Mise en cache des réponses fréquentes avec Redis/Caffeine
2. Compression gzip des réponses HTTP pour réduire la taille
3. Pagination des résultats pour les grandes listes
4. Implementation d'un health check pour le monitoring
5. Documentation OpenAPI/Swagger de l'API
6. Optimisation des requêtes SQL avec WHERE au lieu de filtres Java
7. Mise en place d'un système de cache pour les données fréquemment accédées
8. Nettoyage du code (imports/variables inutiles)
9. Si besoin de traductions : implémentation d'un cache de traductions
10. Structure de réponse minimaliste adaptée aux besoins réels
