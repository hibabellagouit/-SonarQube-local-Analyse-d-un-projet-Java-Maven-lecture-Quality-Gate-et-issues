# SonarQube (local) — Analyse d’un projet Java Maven, lecture Quality Gate et issues

## Objectif de l’activité

Mettre en place SonarQube en local (Docker), créer un projet, générer un token, lancer l’analyse d’un projet Java Maven, puis interpréter les résultats (Quality Gate, bugs, odeurs de code, vulnérabilités, couverture…).

---

## Prérequis

•Docker Desktop (ou Docker Engine)

•Navigateur Web

•JDK installé (selon ton projet)

•Maven (ou Maven Wrapper mvnw)

•Un projet Java Maven (présence de pom.xml)

---

## Démarrer SonarQube en local (Docker)


### Créer les volumes Docker (persistance)

<img width="805" height="289" alt="image" src="https://github.com/user-attachments/assets/9cdc5d07-3124-4e1e-83ed-71290632fc9a" />

### Lancer SonarQube

<img width="929" height="501" alt="Capture d&#39;écran 2025-12-11 001346" src="https://github.com/user-attachments/assets/15880835-9eb0-4ca3-a74d-ab325eadfa14" />

<img width="933" height="502" alt="Capture d&#39;écran 2025-12-11 001741" src="https://github.com/user-attachments/assets/bcae1935-6eb4-4845-be66-ac9751250b04" />

### Vérifier l’accès web

<img width="932" height="503" alt="Capture d&#39;écran 2025-12-11 001828" src="https://github.com/user-attachments/assets/72b2a6ea-d544-4041-a57b-0956ab3d6d7d" />

---

## Comprendre l’écran “Overview” et le Quality Gate

<img width="932" height="505" alt="Capture d&#39;écran 2025-12-11 001842" src="https://github.com/user-attachments/assets/c0c9a948-9dbe-4e79-9c46-11e4d4f81e4b" />

<img width="924" height="502" alt="Capture d&#39;écran 2025-12-11 002007" src="https://github.com/user-attachments/assets/6b0107ee-3878-40b7-8319-4da67a014c64" />

<img width="930" height="499" alt="Capture d&#39;écran 2025-12-11 002037" src="https://github.com/user-attachments/assets/f8c6ef6d-19e7-4fa0-a6ce-b08fc8dd8b65" />

<img width="930" height="505" alt="Capture d&#39;écran 2025-12-11 002145" src="https://github.com/user-attachments/assets/62626054-ba24-49a6-b40c-2a4a6adfabe2" />

---

## Créer un projet SonarQube (mode manuel / local)

### Ouvrir “Projects”

<img width="923" height="148" alt="image" src="https://github.com/user-attachments/assets/f5c7d854-e875-4620-9eb3-4501fd2b3a8b" />

### Cliquer sur “Create Project”

<img width="928" height="158" alt="image" src="https://github.com/user-attachments/assets/43b19933-0f73-495d-8c53-5a2da1969021" />

### Menu “Create Project” (choix Manually)

<img width="928" height="158" alt="image" src="https://github.com/user-attachments/assets/43b19933-0f73-495d-8c53-5a2da1969021" />

### Choisir “Manually” (projet local)

<img width="929" height="478" alt="image" src="https://github.com/user-attachments/assets/3f644d98-4d75-4810-8145-2b4d6edfe8d8" />


### Écran alternatif : connexion DevOps (GitHub/GitLab…)

<img width="930" height="499" alt="Capture d&#39;écran 2025-12-11 002037" src="https://github.com/user-attachments/assets/30c1e21f-23e8-473b-8e51-385606fe31b7" />

### Renseigner “Project display name” et “Project key”

<img width="925" height="494" alt="Capture d&#39;écran 2025-12-11 002430" src="https://github.com/user-attachments/assets/c52272fb-3dcf-47f4-90d0-6d5fcfd2dfa1" />

---

## Choisir “Analyser localement”

<img width="926" height="509" alt="Capture d&#39;écran 2025-12-11 002517" src="https://github.com/user-attachments/assets/c448da54-990d-4d14-a389-a7cacd2be12c" />

## Générer un token (obligatoire)

### Générer un “project token”

<img width="925" height="500" alt="Capture d&#39;écran 2025-12-11 002705" src="https://github.com/user-attachments/assets/1b0f7eda-0eff-4c3e-aefd-fb519a08aefe" />

### Récupérer le token généré

![WhatsApp Image 2025-12-11 à 01 23 37_fd5dc853](https://github.com/user-attachments/assets/e58db35a-f944-4c31-ba2c-0892e94f8386)

---

## Choisir le scanner Maven et exécuter l’analyse

### SonarQube propose la commande selon le build (Maven/Gradle/…)

<img width="924" height="495" alt="Capture d&#39;écran 2025-12-11 002903" src="https://github.com/user-attachments/assets/76d3acce-d705-47c8-bd58-293637bacc22" />

### Copier la commande Maven SonarScanner

![WhatsApp Image 2025-12-11 à 01 25 53_8f98b07e](https://github.com/user-attachments/assets/6e9e71ed-50a1-4d96-9916-ca867c8e09dd)

### Se placer dans le dossier du projet Maven

<img width="198" height="353" alt="image" src="https://github.com/user-attachments/assets/39d801b6-0fee-4e4f-9471-c460b2eafb79" />

### Lancer la commande d’analyse

<img width="934" height="495" alt="Capture d&#39;écran 2025-12-11 010237" src="https://github.com/user-attachments/assets/297d7690-16fb-446d-9808-e7d6808ad5cb" />

---

## Consulter les résultats dans SonarQube

### Ouvrir le projet

<img width="929" height="503" alt="Capture d&#39;écran 2025-12-11 010408" src="https://github.com/user-attachments/assets/5acb6a37-53b2-4aef-85f2-3c7b569db2fd" />

### Lire les sections principales

•Overview : résumé + Quality Gate

•Issues : liste détaillée (Bugs, Code Smells…)

•Security Hotspots : points à valider (revue sécurité)

•Measures : métriques (duplication, complexité…)

•Code : code annoté + explications règle par règle

•Activity : historique des analyses

<img width="923" height="506" alt="Capture d&#39;écran 2025-12-11 010350" src="https://github.com/user-attachments/assets/232b5e47-8fa4-46e2-ab35-0e8f02aefee9" />

---

## Docker 

<img width="957" height="401" alt="image" src="https://github.com/user-attachments/assets/05e74e48-a027-45c9-9e2d-34362a2f0e6d" />


---

##Auteur

**Nom :** JARDI Siham

**Cours :** Architecture Microservices : Conception, Déploiement et Orchestration

**Date :** Decembre 2025

**Encadré par :** Pr.Mohamed LACHGHAR



