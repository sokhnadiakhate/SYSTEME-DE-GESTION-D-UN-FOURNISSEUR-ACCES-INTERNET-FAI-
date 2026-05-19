# Système de Gestion d'un Fournisseur d'Accès Internet (FAI) — Modélisation UML

Ce dépôt contient l'ensemble des travaux de modélisation UML pour l'architecture logicielle et la gestion d'un Fournisseur d'Accès Internet (FAI) inspiré des standards de grands opérateurs (comme Orange, Maroc Telecom, etc.). 

L'objectif de cette modélisation est de concevoir une infrastructure robuste, sécurisée et évolutive capable de piloter la gestion commerciale, l'authentification réseau, la maintenance technique et l'administration des équipements.

---

## 🏗️ Architecture Globale du Système

Le système est l'association de **4 blocs fonctionnels clés** :
1. **Gestion Commerciale :** Inscription, catalogue d'offres, souscription d'abonnements et facturation automatisée.
2. **Accès Réseau :** Authentification sécurisée des box internet et attribution dynamique des configurations IP.
3. **Maintenance & Support :** Signalement instantané des incidents par les clients et console de résolution pour les techniciens.
4. **Administration Système :** Surveillance de la santé du réseau en temps réel et alertes automatiques en cas de panne critique.

---

## 📊 Présentation des Diagrammes UML

Le projet est modélisé à travers différentes vues complémentaires. Les exports visuels de chaque diagramme sont présentés ci-dessous :

### 1. Diagramme de Cas d'Utilisation (Use Case Diagram)
Ce diagramme cartographie les interactions entre les acteurs (Client, Technicien, Administrateur, Système de Facturation) et les fonctionnalités métiers du système.
* **Éléments inclus :** Relations d'inclusion (`<<include>>`) pour les étapes obligatoires (comme la facturation ou l'attribution d'IP) et d'extension (`<<extend>>`) pour les cas conditionnels (comme le blocage de compte ou les alertes de panne).

![Diagramme de Cas d'Utilisation] <img width="807" height="840" alt="image" src="https://github.com/user-attachments/assets/df24160a-cde4-4d61-8f16-76d051c8ca83" />


### 2. Diagramme de Classes (Class Diagram)
Ce diagramme représente la structure statique du système en listant les classes, leurs attributs, leurs méthodes ainsi que les relations qui les unissent.
* **Éléments inclus :** Modélisation des entités principales (Client, Box, Facture, TicketIncident, Offre), des règles de multiplicité (ex: un client peut avoir plusieurs factures) et des concepts d'héritage.

![Diagramme de Classes] <img width="1575" height="787" alt="image" src="https://github.com/user-attachments/assets/db0d4a46-f2af-41ca-92a0-fed68f2364cd" />


### 3. Diagramme de Séquence (Sequence Diagram)
Ce diagramme formalise l'échange chronologique de messages entre les différents objets du système pour des scénarios précis, comme le parcours d'authentification réseau ou le tunnel d'achat sécurisé.
* **Éléments inclus :** Lignes de vie, messages synchrones/asynchrones, boucles de répétition (`loop`) et blocs alternatifs (`alt`) pour la gestion des erreurs.

![Diagramme de Séquence] <img width="1352" height="762" alt="image" src="https://github.com/user-attachments/assets/d64d3930-4eb7-4d38-85ef-28b990ae1305" />


### 4. Diagramme d'Activité (Activity Diagram)
Il décrit le comportement dynamique du système sous forme de flux de contrôle (Workflow), détaillant étape par étape le traitement logique d'une demande de maintenance ou le routage d'un ticket.
* **Éléments inclus :** Actions, nœuds de décision, barres de synchronisation (fork/join) et couloirs d'activité (`Swimlanes`) par acteur.

![Diagramme d'Activité] <img width="1338" height="757" alt="image" src="https://github.com/user-attachments/assets/65c71704-c051-47fa-b39d-d99700181f9d" />


### 5. Diagramme d'État-Transition (State Machine Diagram)
Ce diagramme suit le cycle de vie et les changements d'états des entités cruciales du système au cours du temps.
* **Éléments inclus :** Suivi des états de la Box Internet (Déconnectée, En cours d'authentification, Connectée, Bloquée) et du Ticket d'incident (Ouvert, En cours, Résolu, Clôturé) en fonction des événements reçus.

![Diagramme d'État-Transition] <img width="1351" height="766" alt="image" src="https://github.com/user-attachments/assets/c6d7b22b-4b23-4725-be01-05e1edd1479c" />


---

## 🛠️ Comment exploiter ce dépôt ?

1. **Visualisation rapide :** L'ensemble des modélisations graphiques est consultable directement depuis ce fichier ou dans le dossier `images/`.
2. **Édition :** Les fichiers sources correspondants peuvent être importés et modifiés dans n'importe quel logiciel de modélisation compatible UML (tel que le logiciel Astah).

---
*Projet réalisé dans le cadre du module d'Analyse et Conception Orientée Objet (UML).*
