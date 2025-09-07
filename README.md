---

---

![image.png](attachment:6872da20-eb84-4fbe-85b2-de0cd263906a:image.png)

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

![image.png](attachment:7108c5ba-2588-4b02-a831-8e3bab83225d:image.png)

## 2 ) Exploitation de Dynatrace :

### a) Déploiement de OneAgent sur notre VM local Debian 11

- On a une machine Virtual en local avec comme OS Debian 11
- On se connecte sur notre Console Dynatrace  dans  **Discovery & Coverage**

![image.png](attachment:3d3d3695-6ff6-4ee3-9d5b-6a41a023a887:image.png)

- On télécharge l’agent sur notre VM

![image.png](attachment:56aaaff7-b2e8-4f71-89e7-e940b69b59de:image.png)

- On installe Dynatrace

![image.png](attachment:30a9c8c4-94e5-4cd0-8923-f8a81dc22186:image.png)

### b) Exploitation des application de Dynatrace :

![image.png](attachment:5f1f0778-c868-4cbd-8e4f-c38db144199c:image.png)

![image.png](attachment:06495d6f-0674-48ea-85af-bc139c16979c:image.png)

### c) Utilisation de l’application Hosts de dynatrace

- On va voir l’application Hosts qui permet d’avoir des information sur la machine

![image.png](attachment:075a65bc-685c-4aea-8507-c40538d2d3cf:image.png)

- On peut avoir des information sur les métriques :

![image.png](attachment:48bf911a-2e98-470d-9b22-8a611246ecf9:image.png)

### d) Utilisation de l’appliction infrastructure & Operations

![image.png](attachment:5701cfb1-5575-4fb2-8dd7-c674b765984d:image.png)

- Un Fonctionnalité qui permet d’avoir plus d’information sur les ressources :

![image.png](attachment:38493408-dce9-4122-8673-c1813f522dbd:image.png)

![image.png](attachment:f5988477-2c00-4ef8-9031-ff3ce59b8a60:image.png)

### e) On va faire un test avec l’application Front de dynatrace pour la gestion des application

- On va déployer notre page HTML sur la VM

![image.png](attachment:9b0017e9-67d0-477a-9f1a-1bd7535d8073:image.png)

![image.png](attachment:2a93536c-5db5-4a2f-8315-cb1548071991:image.png)

- On va voir  comment fonctionne l’application

![image.png](attachment:4f603d04-4521-4682-aad5-d648e8170f27:image.png)

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

![image.png](attachment:3b947011-a914-457a-af22-ea5d01acf70b:image.png)

![image.png](attachment:80689957-db7d-4add-8828-7e4731cd6a38:image.png)

### f) Utilisation de l’application métriques et data export pour la création de notre dashboard

- On va sur l’application **metrics classic** pour voir le type de metrics qu’on veut visualiser

![image.png](attachment:0abc09fa-5ca5-4bc1-97d6-2b70b5a25f74:image.png)

On clique sur **create chart**

![image.png](attachment:fa4cb58e-5a7a-451d-8de4-5b64fc2be523:image.png)

On tombe sur l’application **data Explorer** : 

![image.png](attachment:b913d111-9436-4d58-a118-6da630d06ca8:image.png)

**Remarque :** On peut le faire aussi depuis l’application data explorer ne pas passer par metrics classic

On clique sur Pin to dashboard pour créer notre dashboard

![image.png](attachment:6f84b00e-9975-4554-8b78-0f9a45de5ec7:image.png)

![image.png](attachment:295af8c5-fffd-486b-a9dc-c316f24d2267:image.png)

![image.png](attachment:8ba1a34a-fde7-48c9-aced-b838d9a7f296:image.png)

- On peut voir le dashboard qu’on a crée dans l’application **Dashboard classic**

![image.png](attachment:4aaf1ab9-50c3-4a84-bc31-b44a0a14f38e:image.png)

**Remarque :** On peut avoir des informations sur les journaux de log : 

---

| **Catégorie** | **Exemples de journaux** | **Utilité principale** |
| --- | --- | --- |
| **Système d’exploitation** | - Linux : `/var/log/messages`, `/var/log/syslog`, `/var/log/secure`, `/var/log/dmesg`   - Windows : *System logs*, *Application logs*, *Security logs* (Event Viewer) | Suivi de l’état du système, démarrages, pannes, authentifications, sécurité |
| **Middleware – Serveurs applicatifs** | - WebLogic : `AdminServer.log`, `ManagedServer.log`, `access.log`  - JBoss/WildFly : `server.log`  - Tomcat : `catalina.out`, `localhost.log`  - WebSphere : `SystemOut.log`, `SystemErr.log` | Suivi du fonctionnement des serveurs applicatifs, erreurs Java, transactions |
| **Middleware – Serveurs web** | - Apache : `access_log`, `error_log`  - Nginx : `access.log`, `error.log` | Suivi du trafic, erreurs HTTP, indisponibilités |
| **Middleware – Messagerie / ESB** | - Kafka : `server.log`, `controller.log`, `state-change.log`  - ActiveMQ : `activemq.log`  - IBM MQ : `AMQERR01.LOG`, `qmgrs/<QMGR_NAME>/errors/` | Suivi des échanges de messages, files d’attente, pertes ou blocages |
| **Applicatifs** | - Logs applicatifs (via Log4j, Logback, etc.)  - Exceptions, transactions métier | Débogage et suivi des erreurs fonctionnelles ou exceptions |
| **Sécurité** | - Logs d’authentification (SSH, RDP)  - Middleware : erreurs SSL/TLS, accès refusés  - Journaux centralisés SIEM (Splunk, ELK, Dynatrace Logs) | Détection d’intrusions, gestion des certificats, conformité |
| **Performance / JVM** | - `gc.log` (Garbage Collector)  - Thread dumps  - Heap dumps | Diagnostic de performance, fuite mémoire, blocages applicatifs |

**Exemple :**
