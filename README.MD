

# Proposition
Ce repo contient une proposition d'amélioration du repo `miage-numres-step2a`

# Fork du projet
L'objectif est de créer une copie du projet 'miage-numres-step2b' sur votre compte github.

1. Se rendre sur le projet github [miage-numres-step2b] (https://github.com/aepsilon-tek/miage-numres-step2b)

# lancement de GitPod

Pour utiliser  **GitPod** avec votre projet forké, il suffit d'ouvrir  l'url suivant dans votre navigateur :
**https://gitpod.io/#** + **URL_REPO_GITHUB**

Avec un repo _https://github.com/miage3-ae/miage-numres-step2b_ alors l'url est : **https://gitpod.io/#https://github.com/miage3-ae/miage-numres-step2b**


# Evaluer la proposition
## En mode JVM
1. Construire l'application en mode JVM
1. Lancer l'applicatif construit : `java -jar target/quarkus-app/quarkus-run.jar`
1. Répondre aux questions Q1 à Q4 du fichier **_Questions.md_**
1. Commiter  & Pusher le fichier **_Questions.md_**


## En mode Natif
1. Construire l'application en mode Natif
1. Lancer l'applicatif construit : `./target/api-quarkus-1.0.0-SNAPSHOT-runner`
1. Répondre aux questions Q5 à Q8 du fichier **_Questions.md_**
1. Commiter  & Pusher le fichier **_Questions.md_**



# Bilan
1. Répondre aux questions Q9 et Q10   **_Questions.md_**
1. Commiter  & Pusher le fichier **_Questions.md_**


# Commandes Utiles
* ```./mvnw clean compile ``` : Compilation du projet
* ```./mvnw clean package``` : Construction du projet en mode JVM
* ```./mvnw clean package -P native``` : Construction du projet en mode Natif
