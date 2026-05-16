# MEMORY.md - Mémoire Vive & Journal de Bord

> **Statut :** Dynamique et persistant. Ce fichier est l'outil principal de l'IA pour maintenir le contexte, acter les décisions architecturales et éviter la répétition d'erreurs d'une session à l'autre.

---

## 🚀 Séquence d'Initialisation (À exécuter au début de CHAQUE session)

Avant de traiter la demande de l'humain ou de modifier le code, l'IA doit impérativement lire les trois fichiers de contexte dans l'ordre suivant :
1. **`AGENTS.md`** : S'aligner sur sa posture de collaborateur critique et sur les doctrines techniques.
2. **`HUMAN.md`** : Prendre connaissance du profil de l'utilisateur, de ses préférences et de ses contraintes OPSEC.
3. **`MEMORY.md`** : Analyser l'état actuel du projet, les derniers blocages et l'historique récent (lire du haut vers le bas).

---

## 🛠️ Règles d'Exécution Critiques (Karpathy Style)

1. **Ask, don't guess** : Lever toute ambiguïté avant d'écrire la moindre ligne de code. Poser une question fait gagner du temps ; une mauvaise hypothèse en fait perdre.
2. **Minimum code** : Préférer 50 lignes bien pensées à 200 lignes complexes. Le code non écrit n'a pas de bug et ne demande aucune maintenance.
3. **Surgical changes** : Les modifications doivent être ciblées. Pas de dommages collatéraux sur l'existant.
4. **Log before fix** : Ne jamais tenter de corriger un bug "à l'aveugle". Placer des logs, reproduire le comportement, analyser, puis corriger de manière chirurgicale.

---

## 📌 Rappels Architecturaux & Contraintes du Projet
*(À compléter et enrichir par l'IA au fil du projet)*

* **Gestion du statut/auth :** Avant d'ajouter une abstraction (proxy, middleware), valider sa compatibilité avec le système existant.
* **Code mort :** Avant de déclarer un composant ou une fonction comme "code mort", vérifier l'intégralité des appels (*grep*) à travers tout le projet.
* **Vérification des impacts :** Relire attentivement le *diff* final pour s'assurer qu'aucune dépendance cachée n'a été rompue.

---

## 👤 Contexte Utilisateur (Philosophie de Travail)

* **Qualité > Vitesse :** Ne jamais sacrifier la sécurité ou la propreté du code pour aller plus vite.
* **Esprit Système :** Vision globale des interconnexions plutôt que focus isolé sur un composant.
* **OPSEC Fort :** Pas de confiance aveugle envers les services tiers. Protection stricte des données privées.
* **Partenariat Honnête :** Valorise les retours directs, la critique constructive et le débat logique.

---

## 📅 Journal des Sessions (Ordre Chronologique Inversé)

### [AAAA-MM-JJ] - Nom de la Session / Objectif Principal
* **Ce qui a été fait :**
  - Item 1
  - Item 2
* **Erreurs rencontrées & Solutions :**
  - *Erreur :* Description du problème.
  - *Solution / Leçon :* Comment cela a été résolu et ce qu'il faut retenir pour l'avenir.
* **État actuel & Prochaines étapes :**
  - Statut du projet.
  - Ce qui reste à faire lors de la prochaine session.

---
*(Modèle à dupliquer au-dessus pour chaque nouvelle session)*
