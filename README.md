# StageFlow AI

StageFlow AI** est une plateforme web qui centralise les offres de stage et les candidatures.Elle aide les entreprises à comparer les compétences d'un CV avec celles demandées dans une offre grâce à un micro-service IA.
Le score IA est indicatif : la décision finale appartient toujours au recruteur.

---

## Membres de l'équipe et rôles

| Membre | Rôle principal |
|---|---|
| **Eya Balti** | Frontend React |
| **Roua Bayar** | Backend Spring Boot / base de données |
| **Yasmin Souiki** | Micro-service IA FastAPI |
| **Azyz Ben Hamouda** | Tests, intégration et documentation |

---

## Stack technologique

| Couche | Technologie | À quoi elle sert dans StageFlow AI |
|---|---|---|
| **Frontend** | React | Pages et formulaires utilisés par les étudiants, les entreprises et les administrateurs |
| **Backend principal** | Spring Boot (Java) | Reçoit les requêtes, applique les règles métier, gère les utilisateurs, les offres et les candidatures |
| **Micro-service IA** | FastAPI (Python) | Réalise uniquement l'analyse CV-offre (extraction NLP et comparaison des compétences) et retourne un score indicatif |
| **Base de données** | PostgreSQL | Conserve les comptes, les offres, les candidatures et les résultats d'analyse |
| **Conteneurisation** | Docker Compose | Lance tous les services ensemble pendant le développement et la démonstration |

### Comment les services communiquent
```
React  -->  Spring Boot  -->  FastAPI (IA)
                |
           PostgreSQL
```
1. L'utilisateur utilise l'application **React**.
2. React envoie les actions au backend **Spring Boot**.
3. Spring Boot vérifie les données et les enregistre dans **PostgreSQL**.
4. Quand une entreprise demande une analyse, Spring Boot envoie le texte du CV et celui de l'offre au service **FastAPI**.
5. FastAPI renvoie le score et les compétences ; Spring Boot transmet le résultat à React pour l'affichage.

---

## Prérequis d'installation

Installez les outils suivants, puis vérifiez-les avec la commande indiquée dans un terminal.

| Outil | Utilité | Vérification | Téléchargement |
|---|---|---|---|
| **Git** | Gérer le code et travailler en équipe | `git --version` | https://git-scm.com/downloads |
| **Node.js** (avec npm) | Lancer le frontend React | `node -v` puis `npm -v` | https://nodejs.org |
| **Java JDK** (17 ou plus) et **Maven** | Lancer le backend Spring Boot | `java -version` puis `mvn -v` | https://adoptium.net |
| **Python 3** (avec pip) | Lancer le micro-service IA FastAPI | `python --version` puis `pip --version` | https://www.python.org/downloads |
| **Docker Desktop** (avec Docker Compose) | Lancer PostgreSQL et tous les services ensemble | `docker --version` puis `docker compose version` | https://www.docker.com/products/docker-desktop |


