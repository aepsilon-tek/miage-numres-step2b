# Q1 : Empreinte mémroire en mode JVM ?
L'empreinte mémoire est 214M (mémoire résidentielle RES) par processus Java exécutant l'application Quarkus.

# Q2: Temps et  taille  réponse   liste les questions
Temps: 0.083026s  
Taille: 53 octets

# Q3: Temps et  taille  réponse  liste des propositions
Temps: 0.002335s  

# Q4: Temps et  taille  réponse  évaluation les réponses
Temps: 0.001621s  
Taille: 53 octets

# Q5 : Empreinte mémroire en mode natif ?
Réponse: 75.9M (mémoire résidentielle - RES)

# Q6: Temps et  taille  réponse   liste les questions
Temps: 0.001622s  
Taille: 53 octets

# Q7: Temps et  taille  réponse  liste des propositions
Temps: 0.000652s  
Taille: 53 octets

# Q8: Temps et  taille  réponse  évaluation les réponses
Temps: 0.000780s  
Taille: 53 octets


# Q9 :  Que constatez-vous en comparant les métriques de la solution  initiales vs la votre vs celle-ci ?
En comparant les solutions, voici les constats :

1. **Temps d'exécution** :
   - **Mode JVM** : Plus lent en raison du besoin d'interprétation.
     - Exemple : Temps pour `/api/questions` : ~0.083026s.
   - **Mode Natif** : Temps d'exécution considérablement réduit.
     - Exemple : Temps pour `/api/questions` : ~0.001622s.

2. **Empreinte mémoire** :
   - **Mode JVM** : Plus élevée (223940 KB).
   - **Mode Natif** : Plus optimisée (99548 KB).

3. **Taille des réponses** :
   - La taille des réponses reste constante (53 octets pour tous les endpoints).
   - Les op

# Q10 : Quelle dernière amélioration pourriez-vous proposer?
**Description** : Mise en place de la compression des réponses HTTP.

**Problème** :  
- Actuellement, la taille des réponses JSON peut être optimisée davantage pour les environnements où la bande passante est limitée.

**Implémentation** :  
- Activation de la compression **GZIP** côté serveur avec Quarkus.
- Ajout des headers pour activer la compression côté client :
  - `Accept-Encoding: gzip`.

**Avantages** :  
- Réduction significative de la taille des réponses.
- Amélioration des temps de transfert.

**Impact attendu** :
- Exemple pour `/api/questions` :  
   - Taille avant compression : **53 octets**.  
   - Taille après compression : **~20-30 octets**.
   - Temps total réduit en conséquence.
