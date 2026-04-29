# 🗄️ Base de données de gestion des rendez-vous – Access & SQL

## 📌 Contexte

Conception d'une base de données relationnelle sous Microsoft Access pour gérer
les rendez-vous entre patientes et sages-femmes. L'objectif est de centraliser
les informations, assurer la cohérence des données et permettre une analyse
de l'activité via des requêtes SQL.

---

## 🎯 Objectifs

- Modéliser une base de données relationnelle adaptée au suivi d'activité médicale
- Assurer l'intégrité référentielle via des relations entre tables
- Créer des requêtes SQL pour l'analyse de l'activité
- Développer des formulaires et états pour la saisie et la consultation des données

---

## 🛠️ Technologies utilisées

![Access](https://img.shields.io/badge/Microsoft-Access-red?logo=microsoft)
![SQL](https://img.shields.io/badge/SQL-Requêtes-blue)

- **Outil :** Microsoft Access
- **Langage :** SQL

---

## 🗂️ Structure de la base de données

### Tables

| Table | Clé primaire | Description |
|---|---|---|
| PATIENT | ID_patient | Nom, prénom, adresse, téléphone, date de naissance |
| SF | ID_SF | Nom, prénom, téléphone |
| RDV | ID_rdv | Date, heure, motif, statut, type, clés étrangères |

### Relations
- **PATIENT → RDV** : relation 1–N (une patiente, plusieurs rendez-vous)
- **SF → RDV** : relation 1–N (une sage-femme, plusieurs rendez-vous)

---

## 🔍 Requêtes SQL réalisées

| Requête | Type | Description |
|---|---|---|
| RDV_SF | JOIN | Rendez-vous par sage-femme |
| RDV_patient | JOIN | Rendez-vous par patiente |
| NB_RDV_Type | GROUP BY + COUNT | Nombre de RDV par type (Cabinet/Domicile) |
| DateHeure_RDV | Champ calculé | Combinaison date + heure en un seul champ |
| NB_RDV_SF | GROUP BY + COUNT | Nombre de RDV par sage-femme |

---

## 📋 Formulaires

- **F_PATIENT** : gestion des patientes
- **F_SF** : gestion des sages-femmes
- **F_RDV** : gestion des rendez-vous
- **F_PATIENT_RDV** : fiche patient avec sous-formulaire RDV associés
- **F_RDV_SF** : fiche sage-femme avec sous-formulaire RDV associés
- **F_ACCUEIL** : formulaire de navigation principal avec macros

---

## 📄 États (rapports imprimables)

- RDV_Domicile
- RDV_Réalisé
- SF (liste des sages-femmes)

---

## 👩‍💻 Auteure

**Noor Seba** – Étudiante en Master Épidémiologie, Données de Santé & Biostatistique
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Noor%20Seba-blue?logo=linkedin)](https://www.linkedin.com/in/noor-seba-260685369)
