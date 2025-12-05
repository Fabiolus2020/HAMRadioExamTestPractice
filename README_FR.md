# 📡 Entraîneur d'examen radioamateur (Canada) — Application bilingue

Un outil HTML gratuit, prêt à être utilisé hors ligne, pour vous aider à pratiquer les examens **de base et avancé** de radioamateur d’ISDE (Canada).

- 🇨🇦 Basé sur les banques de questions officielles d’ISDE
- 🇬🇧🇫🇷 Interface entièrement bilingue (anglais et français)
- 📱 Mise en page adaptée au mobile (PWA prête)
- 🧠 Plusieurs modes d’étude, y compris les structures d’examen officielles
- 🧾 Banque CSV optionnelle avec explications

Créé par **Fabien Clermont**.  
Sous licence **CC BY-NC-SA 4.0** (non commercial, attribution, partage dans les mêmes conditions).

---

## ✨ Fonctionnalités

### 📚 Prise en charge des deux banques de questions officielles d’ISDE

L’application peut charger les fichiers TXT délimités officiels publiés par ISDE :

- `amat_basic_quest_delim2025.txt` (Base)
- `amat_adv_quest_delim2025.txt` (Avancé)

Vous pouvez :

- Les charger **directement depuis GitHub** via les boutons intégrés, ou  
- Les télécharger vous-même et utiliser **« Choisir un fichier »** pour charger une copie locale.

Avec une banque officielle chargée, l’application :

- Respecte la **répartition réelle des catégories d’examen** :
  - Base : 100 questions (8 catégories, nombre de questions fixe)
  - Avancé : 50 questions (7 catégories, nombre de questions fixe)
- Affiche des **statistiques par catégorie** et détecte les **points faibles**.

> 🔎 Les banques officielles d’ISDE **ne contiennent pas** d’explications — seulement des questions et réponses.

---

## 🧾 Banque CSV optionnelle avec explications

En plus des fichiers TXT officiels, l’application prend en charge un **format CSV personnalisé** qui permet à vous (ou à tout utilisateur) d’ajouter :

- Des **explications détaillées** pour chaque question  
- Des **trucs de mémoire** et astuces pédagogiques  
- Du texte formaté compatible HTML (pour l’affichage dans l’application)  
- Vos propres améliorations ou clarifications

Un exemple de CSV est fourni dans le dépôt, par exemple :

- `BankQuestionJuly2025.csv`

Vous pouvez :

1. Télécharger le fichier CSV depuis GitHub.  
2. L’ouvrir dans Excel, Google Sheets ou LibreOffice.  
3. Modifier ou ajouter des explications, aides-mémoire ou reformulations plus claires.  
4. Le sauvegarder en CSV et le charger à l’aide du bouton **« Choisir un fichier (local) »** dans l’application.

Lorsque qu’un CSV compatible est chargé :

- L’application affiche une section **Explication** sous chaque question après avoir cliqué sur **« Vérifier la réponse »**.
- L’explication provient directement de la colonne `explanation` du CSV.
- Ce mode est idéal pour les étudiants qui veulent comprendre *pourquoi* la réponse est correcte, plutôt que seulement mémoriser la lettre à choisir.

> 💡 Remarque : les banques TXT officielles du gouvernement ne contiennent pas d’explications.  
> La banque d’explications au format CSV est un **complément créé par l’utilisateur**. Je (Fabien) travaille activement à l’améliorer et à l’enrichir, mais chaque utilisateur peut personnaliser son propre CSV pour son étude personnelle.

### 📁 Structure recommandée du CSV

Une ligne type dans le CSV ressemble à ceci (les colonnes peuvent légèrement varier) :

- `question` — Énoncé de la question  
- `optionA`, `optionB`, `optionC`, `optionD` — Choix de réponses  
- `correctOption` — Réponse correcte (`A`, `B`, `C` ou `D`)  
- `explanation` — Texte d’explication compatible HTML (affiché après vérification de la réponse)  
- `BankQuestionID` — ID optionnel correspondant à la banque officielle (par exemple `B-001-001-002`)

L’application est flexible, mais cette structure est recommandée pour de meilleurs résultats.

---

## 🧪 Modes d’étude et d’examen

L’application propose plusieurs modes pour s’adapter à différents styles d’apprentissage :

### 🎯 Mode examen (structure officielle)

- **Base :** 100 questions selon la répartition officielle des catégories.
- **Avancé :** 50 questions selon la répartition officielle des catégories.
- Affiche :
  - Score final et pourcentage
  - **Réussite / Échec / Distinction (honours)** selon le seuil
  - Répartition par catégorie (règlementation, exploitation, électronique, etc.)
  - **Points faibles** signalés si le pourcentage est inférieur à 70 %
  - Boutons « **Pratiquer uniquement cette catégorie** »
  - Bouton « **Reprendre seulement les mauvaises réponses** »

### 🔄 Mode aléatoire

- Tire des questions au hasard dans la banque chargée.
- Utile pour des sessions rapides et une révision générale.

### ♻️ Mode sans répétition

- Parcourt toutes les questions **sans répétition** jusqu’à épuisement de la banque.
- Idéal pour couvrir toutes les questions au moins une fois.

### 🧩 Entraînement par catégorie (par thème)

- Permet de choisir une ou plusieurs catégories à cibler (par exemple uniquement « Propagation », uniquement « Antennes », etc.).
- Très utile pour travailler spécifiquement sur vos faiblesses.

### 🔁 Refaire uniquement les mauvaises réponses

- Après un examen, vous pouvez lancer une session contenant **uniquement les questions auxquelles vous avez mal répondu**.
- L’application construit une nouvelle séquence à partir de vos erreurs.

---

## 📊 Progression et retour d’information

- Le **score** est toujours affiché sous le bouton « Vérifier la réponse ».
- L’application suit :
  - Le nombre total de questions répondues
  - Le nombre de bonnes réponses
  - Le pourcentage global
- Le mode examen affiche un **rapport final** avec :
  - Le pourcentage global
  - Réussite / Échec / Distinction (80 % et plus)
  - Résultats détaillés par catégorie
  - Signalement des **catégories faibles** (moins de 70 %)

---

## 🌐 Interface bilingue (EN / FR)

Dès l’**Étape 1**, l’utilisateur choisit :
- 🇬🇧 **English**
- 🇫🇷 **Français**

Les éléments suivants changent de langue :

- Tous les libellés et instructions (étapes, boutons, messages)
- Noms de catégories et titres de rapports
- Libellés Réussite / Échec / Distinction
- Contenu de la carte « À propos / Support »
- Mention de licence et texte du pied de page

Vous pouvez changer de langue **à tout moment** ; l’interface est mise à jour immédiatement.

---

## 📱 Adapté au mobile et prêt pour PWA

- Application HTML monopage (aucun serveur backend requis)
- Mise en page réactive avec un mode **optimisé pour le mobile**
- Fonctionne bien dans un navigateur ou comme **Progressive Web App (PWA)** lorsqu’elle est hébergée (GitHub Pages, etc.)
- Utilisable sur téléphones, tablettes et ordinateurs de bureau

---

## 🧭 Utilisation de base (aperçu des étapes)

1. **Choisir la langue (EN/FR).**  
2. **Charger une banque de questions :**
   - Banque officielle Base / Avancé depuis GitHub, ou
   - Fichier TXT / CSV local via « Choisir un fichier ».
3. **Sélectionner un mode de questions :**
   - Aléatoire / Sans répétition / Examen / Entraînement par catégorie.
4. **Cliquer sur « Question suivante »** pour commencer, puis « Vérifier la réponse » pour voir si la réponse est correcte (et pour afficher l’explication si vous utilisez un CSV).

Vous pouvez utiliser le bouton **Réinitialiser** (à côté de « Question suivante ») pour remettre complètement l’application à zéro et revenir à l’Étape 1.

---

## 💬 À propos et support

Cet entraîneur d’examen radioamateur bilingue a été créé pour aider les étudiants à se préparer avec des questions de style réel, des structures d’examen officielles et des statistiques par catégorie. Il est sous licence **CC BY-NC-SA 4.0** (non commercial, attribution, partage dans les mêmes conditions). Vous pouvez l’utiliser et le partager pour un usage personnel ou éducatif, mais **pas** le revendre ni l’inclure dans des produits ou services payants.

Si cette application vous aide et que vous souhaitez soutenir les futures améliorations :

- ☕ Buy Me a Coffee : https://buymeacoffee.com/fabiolus  
- 💻 GitHub : https://github.com/Fabiolus2020/HamExamTrainer2025

---

## 📜 Licence (résumé)

Ce projet est sous licence :

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**

Vous êtes autorisé à :

- Partager — copier et redistribuer le matériel sur tout support ou format  
- Adapter — remixer, transformer et créer à partir du matériel  

Sous les conditions suivantes :

- **Attribution** — Vous devez créditer **Fabien Clermont**, fournir un lien vers la licence et indiquer si des modifications ont été apportées.
- **NonCommercial** — Vous ne pouvez **pas** utiliser ce matériel à des fins commerciales.
- **ShareAlike** — Si vous modifiez, transformez ou adaptez ce matériel, vous devez diffuser vos contributions sous la **même licence**.

Texte juridique complet : https://creativecommons.org/licenses/by-nc-sa/4.0/

