Voici **un fichier Markdown prêt à l’emploi**, que tu peux déposer tel quel dans un repo ou une doc (`mermaid-diagrams-reference.md`).
Il couvre **tous les types de diagrammes Mermaid courants**, avec pour chacun : nom, utilité claire, et un exemple minimal fonctionnel.

---

````markdown
# Référence complète des diagrammes Mermaid

Ce document présente les principaux types de diagrammes supportés par Mermaid.
Pour chaque type :

- ce que c’est
- quand l’utiliser
- un exemple minimal fonctionnel

---

## 1. Flowchart

### Description

Diagramme de flux logique. C’est le plus utilisé.  
Il sert à représenter un processus, une suite d’étapes ou une logique conditionnelle.

### Cas d’usage

- workflow métier
- pipeline de traitement
- logique conditionnelle
- algorithme simple

### Exemple

```mermaid
flowchart TD
    A[Début] --> B{Condition ?}
    B -->|Oui| C[Action A]
    B -->|Non| D[Action B]
    C --> E[Fin]
    D --> E
```
````

---

## 2. Sequence Diagram

### Description

Diagramme temporel montrant les échanges entre acteurs, dans l’ordre chronologique.

### Cas d’usage

- appels API
- échanges client / serveur
- scénarios utilisateurs
- protocoles

### Exemple

```mermaid
sequenceDiagram
    participant U as Utilisateur
    participant A as Application
    participant S as Serveur

    U->>A: Action utilisateur
    A->>S: Requête API
    S-->>A: Réponse
    A-->>U: Résultat affiché
```

---

## 3. Class Diagram

### Description

Diagramme orienté objet.
Il décrit des classes, leurs attributs, méthodes et relations.

### Cas d’usage

- conception logicielle
- modélisation de données
- documentation technique

### Exemple

```mermaid
classDiagram
    class User {
        +id: int
        +email: string
        +login()
    }

    class Order {
        +id: int
        +date: Date
        +total: float
    }

    User "1" --> "n" Order
```

---

## 4. State Diagram

### Description

Diagramme d’états finis.
Il montre les états possibles d’un système et les transitions.

### Cas d’usage

- machine à états
- workflow avec statuts
- logique métier complexe

### Exemple

```mermaid
stateDiagram-v2
    [*] --> Brouillon
    Brouillon --> Validé
    Validé --> Publié
    Publié --> Archivé
```

---

## 5. Entity Relationship Diagram (ERD)

### Description

Diagramme de relations entre entités de base de données.

### Cas d’usage

- modélisation de schéma SQL
- conception de bases de données
- documentation data

### Exemple

```mermaid
erDiagram
    CLIENT ||--o{ COMMANDE : passe
    COMMANDE ||--|{ LIGNE_COMMANDE : contient
    PRODUIT ||--o{ LIGNE_COMMANDE : reference
```

---

## 6. Gantt

### Description

Diagramme de planification temporelle.

### Cas d’usage

- gestion de projet
- roadmap
- planning de développement

### Exemple

```mermaid
gantt
    title Planning projet
    dateFormat YYYY-MM-DD

    section Analyse
        Spécifications :done, a1, 2026-02-01, 2d

    section Développement
        Implémentation :active, a2, after a1, 4d
        Tests : a3, after a2, 2d
```

---

## 7. Pie Chart

### Description

Diagramme circulaire de répartition.

### Cas d’usage

- répartition de coûts
- statistiques simples
- ratios

### Exemple

```mermaid
pie
    title Répartition du budget
    "Développement" : 50
    "Infrastructure" : 30
    "Marketing" : 20
```

---

## 8. Journey Diagram

### Description

Diagramme de parcours utilisateur avec ressenti.

### Cas d’usage

- UX
- expérience client
- parcours utilisateur

### Exemple

```mermaid
journey
    title Parcours client
    section Découverte
      Visite site web : 5
      Lecture contenu : 4
    section Achat
      Demande devis : 3
      Paiement : 2
```

---

## 9. Requirement Diagram

### Description

Diagramme de gestion des exigences (inspiré SysML).

### Cas d’usage

- cahier des charges
- exigences fonctionnelles
- traçabilité

### Exemple

```mermaid
requirementDiagram
    requirement Req1 {
        id: R-001
        text: Le système doit être sécurisé
        risk: high
        verifymethod: test
    }
```

---

## 10. Git Graph

### Description

Visualisation de l’historique Git.

### Cas d’usage

- documentation Git
- stratégie de branches
- formation

### Exemple

```mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit
    checkout main
    merge develop
```

---

## 11. Mindmap

### Description

Carte mentale hiérarchique.

### Cas d’usage

- brainstorming
- structuration d’idées
- réflexion stratégique

### Exemple

```mermaid
mindmap
  root((Projet))
    Technique
      Backend
      Frontend
    Métier
      Clients
      Facturation
```

---

## 12. Timeline

### Description

Ligne du temps événementielle.

### Cas d’usage

- historique
- roadmap stratégique
- chronologie

### Exemple

```mermaid
timeline
    title Historique du projet
    2024 : Idée initiale
    2025 : Prototype
    2026 : Mise en production
```

---

## 13. C4 Diagram (niveau supporté par Mermaid)

### Description

Diagrammes d’architecture logicielle simplifiés (inspirés du modèle C4).

### Cas d’usage

- architecture applicative
- documentation système
- vision macro

### Exemple

```mermaid
flowchart LR
    User --> WebApp
    WebApp --> API
    API --> Database
```

---

## Notes importantes

- Mermaid est interprété par GitHub, GitLab, Obsidian, MkDocs, Docusaurus, etc.
- Tous les exemples sont volontairement simples et robustes.
- Évite les diagrammes trop complexes dans un seul bloc : découpe.

---

## Référence officielle

[https://mermaid.js.org](https://mermaid.js.org)

```

---

Si tu veux, je peux maintenant :
- te faire **une version orientée “architecture logicielle” uniquement**,
- ou **une version orientée “process métier / organisation”**,
- ou **un repo Git minimal avec ce fichier + exemples validés GitHub**.
```
