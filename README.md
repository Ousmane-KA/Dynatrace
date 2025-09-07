---

---

<img width="3982" height="1828" alt="image" src="https://github.com/user-attachments/assets/0ef1efd1-eed4-4cc3-94c2-e6901289fd9c" />


---

---

# / ) INTRODUCTION

### a) Qu’est-ce que Dynatrace ?

Dynatrace est une plateforme **tout-en-un** qui permet de :

- Surveiller les **applications** (code, performance, erreurs).
- Suivre l’**infrastructure** (serveurs, containers, cloud, VM).
- Observer les **utilisateurs réels** (RUM – Real User Monitoring).
- Offrir de l’**AIOps** (détection automatique de problèmes et suggestion de résolution grâce à l’IA Davis).
- Gérer la **sécurité applicative** (Application Security).

### b) Composants clés :

**OneAgent**

- Petit agent installé sur les serveurs/applications.
- Collecte automatiquement les métriques, traces et logs.
- Pas besoin de beaucoup de configuration manuelle.

**Smartscape**

- Vue topologique dynamique.
- Montre comment chaque service, application et composant est lié.
- Aide à comprendre les dépendances.

**Davis (IA intégrée)**

- Analyse automatiquement les anomalies.
- Fournit des causes racines (Root Cause Analysis).
- Aide à gagner du temps en troubleshooting.

**Dashboards & Metrics**

- Tableaux personnalisés pour visualiser la performance.
- Intégration avec logs, traces et événements.

### c) Les piliers de l’observabilité dans Dynatrace

- **Metrics** → CPU, mémoire, latence, trafic, etc.
- **Logs** → Messages système et applicatifs.
- **Traces** → Suivi des transactions d’un bout à l’autre (distributed tracing).
- **Events** → Alertes, anomalies, changements détectés.

### d) Types de monitoring dans Dynatrace

- **APM (Application Performance Monitoring)** : surveille la performance applicative.
- **Infrastructure Monitoring** : serveurs, containers, Kubernetes, cloud.
- **RUM (Real User Monitoring)** : expérience utilisateur réelle sur site/app.
- **Synthetic Monitoring** : tests automatisés (simulateurs de navigation).
- **Security Monitoring** : vulnérabilités au niveau applicatif.

### e) Deux façons d’utiliser Dynatrace en local

**Dynatrace Managed**

- C’est la version **on-premise** de Dynatrace.
- Tu installes un **Cluster Node** (serveur Dynatrace) dans ton datacenter ou ta machine.
- Tu ajoutes ensuite des **OneAgents** sur les machines/applications à surveiller.
- Recommandé pour des environnements d’entreprise.

**Dynatrace SaaS + OneAgent sur ton PC/VM**

- Dynatrace propose un **compte d’essai gratuit (15 jours)**.
- Tu n’as rien à installer côté serveur, seulement le **OneAgent** sur ton poste ou tes VM.
- C’est plus simple pour apprendre.

# //) PHASE PRATIQUE DE DYNATRACE

## 1 ) Utilisation de Dynatrace SAAS :

- On va sur le site :  https://www.dynatrace.com/
- On choisit la version free trial : Une utilisation de 15 Jours
- On met les informations pour la souscription au compte
- On choisit la zone ou on veut déployer la solution car on est dans le cas d’une solution SAAS
- On se connecte avec nos information d’identification

<img width="1131" height="521" alt="image" src="https://github.com/user-attachments/assets/d4a8ad2c-5345-46aa-9a4b-41c7d59a1610" />


## 2 ) Exploitation de Dynatrace :

### a) Déploiement de OneAgent sur notre VM local Debian 11

- On a une machine Virtual en local avec comme OS Debian 11
- On se connecte sur notre Console Dynatrace  dans  **Discovery & Coverage**

<img width="1793" height="770" alt="image" src="https://github.com/user-attachments/assets/6ef682b1-6553-4c9a-bbee-e2c997b29b0e" />


- On télécharge l’agent sur notre VM

<img width="1186" height="357" alt="image" src="https://github.com/user-attachments/assets/052d469e-6b45-4216-91b9-5212fc4033d8" />


- On installe Dynatrace

<img width="1191" height="351" alt="image" src="https://github.com/user-attachments/assets/c794668f-4f66-418b-a63f-eb795cffcb72" />


### b) Exploitation des application de Dynatrace :

<img width="1233" height="816" alt="image" src="https://github.com/user-attachments/assets/ef00ae11-525a-4d14-9d68-3158dbe1e1c9" />


<img width="1239" height="819" alt="image" src="https://github.com/user-attachments/assets/5e862e85-43d4-499c-a6a5-96735dc3de25" />


### c) Utilisation de l’application Hosts de dynatrace

- On va voir l’application Hosts qui permet d’avoir des information sur la machine

<img width="1870" height="761" alt="image" src="https://github.com/user-attachments/assets/b2f61a63-9c77-4675-8aed-40274d44666c" />


- On peut avoir des information sur les métriques :

<img width="1755" height="697" alt="image" src="https://github.com/user-attachments/assets/5f474e57-80c3-4ec8-85d6-4ef05c51e36d" />


### d) Utilisation de l’appliction infrastructure & Operations

<img width="1172" height="363" alt="image" src="https://github.com/user-attachments/assets/89a5a1a8-e194-4fad-bf5f-f78be2f387bc" />


- Une Fonctionnalité qui permet d’avoir plus d’information sur les ressources :

<img width="1379" height="871" alt="image" src="https://github.com/user-attachments/assets/d08a5ef2-2f5e-46d8-88d5-a5557d83aaa3" />

<img width="1698" height="807" alt="image" src="https://github.com/user-attachments/assets/594efcd4-3c25-44bf-867a-9eae9c900482" />


### e) On va faire un test avec l’application Front de dynatrace pour la gestion des application

- On va déployer notre page HTML sur la VM

<img width="998" height="125" alt="image" src="https://github.com/user-attachments/assets/25fceb8e-cb9b-4010-942f-e60effa047be" />


<img width="1435" height="482" alt="image" src="https://github.com/user-attachments/assets/ee1ee9e9-9cfc-4fd7-ad04-dff66aedfa35" />


- On va voir  comment fonctionne l’application

<img width="1912" height="457" alt="image" src="https://github.com/user-attachments/assets/c2745c16-8ee5-4733-8d51-2accf40b50da" />


Ce que permet l’application Front (Frontend dans Dynatrace) :

**Surveiller l’expérience utilisateur réelle (RUM) :**

Temps de chargement des pages (HTML, JS, CSS, images).

Mesures Core Web Vitals (Largest Contentful Paint, Cumulative Layout Shift, etc.).

Actions utilisateur (clics, navigation, formulaires).

Performance par **pays, navigateur, OS, type d’appareil**.

**Suivi des sessions utilisateur** 

**Analyse des erreurs & performance**

Détection des **erreurs JavaScript** côté client.

Analyse des temps de chargement par **ressource** (CDN, API externes).

Segmentation : navigateur (Chrome, Firefox, Safari), OS (Windows, iOS, Android).

<img width="1720" height="740" alt="image" src="https://github.com/user-attachments/assets/f7600738-4248-43d1-a5e1-ba7b54d162f0" />


<img width="1699" height="810" alt="image" src="https://github.com/user-attachments/assets/dc719245-7ae5-4f11-8044-542f6e9665dc" />


### f) Utilisation de l’application métriques et data export pour la création de notre dashboard

- On va sur l’application **metrics classic** pour voir le type de metrics qu’on veut visualiser

<img width="1897" height="768" alt="image" src="https://github.com/user-attachments/assets/d4870c8e-98df-43d2-bce1-09e827944f7c" />


On clique sur **create chart**

<img width="1440" height="520" alt="image" src="https://github.com/user-attachments/assets/04929685-9cf7-4497-8435-55f8e995b0ae" />


On tombe sur l’application **data Explorer** : 

<img width="1712" height="848" alt="image" src="https://github.com/user-attachments/assets/c31e06e1-61e8-4117-bd67-214e547b5f20" />


**Remarque :** On peut le faire aussi depuis l’application data explorer ne pas passer par metrics classic

On clique sur Pin to dashboard pour créer notre dashboard

<img width="1877" height="812" alt="image" src="https://github.com/user-attachments/assets/6dfb19db-a322-49e5-874e-955bffd2d547" />


<img width="1592" height="692" alt="image" src="https://github.com/user-attachments/assets/6893fe2a-58f7-48eb-8b66-f9ff5e8f1ca9" />


<img width="1597" height="805" alt="image" src="https://github.com/user-attachments/assets/82370b3e-a4ab-4cbd-a059-4c27d0d1f5e6" />


- On peut voir le dashboard qu’on a crée dans l’application **Dashboard classic**

<img width="1509" height="739" alt="image" src="https://github.com/user-attachments/assets/07558eb1-a2ff-44aa-82c7-01dd258d4a83" />


---
---

