# GCH3545 – Bootcamp Python

**Auteurs :** Bruno Blais & Fabian Denner (Polytechnique Montréal)

Bienvenue au bootcamp de **GCH3545 – Modélisation numérique en ingénierie**.

Ce bootcamp a été conçu pour vous préparer aux travaux dirigés et au projet du cours. Il constitue un rappel des bases de Python scientifique, introduit quelques bonnes pratiques de programmation et présente les outils qui seront utilisés tout au long du trimestre. Ce dépôt contient l'ensemble du matériel du bootcamp.

L'objectif du bootcamp est de vous préparer aux travaux dirigés et au projet du cours en vous familiarisant avec :

- l'environnement Python utilisé dans le cours ;
- les bases de la programmation scientifique ;
- les bonnes pratiques de développement ;
- la vérification des programmes ;
- l'utilisation responsable de l'intelligence artificielle pour la programmation.

Le matériel est organisé sous la forme de guides Markdown (`.md`) et de notebooks Jupyter (`.ipynb`).


L'objectif n'est pas de devenir expert en Python en quelques heures. 

L'objectif est de vous permettre de démarrer le cours avec un environnement fonctionnel et une base commune de connaissances.

# Organisation et utilisation du dépôt

Ce bootcamp se compose de six parties sous forme de notebooks Python interactifs (`.ipynb`) qui vous présentent les principaux logiciels et concepts de programmation dont vous aurez besoin pour la modélisation numérique. Le bootcamp comprend également un guide d'installation de Python, si celui-ci n'est pas encore installé sur votre ordinateur, ainsi qu'une brève introduction à Git, un système de gestion de versions. 

Vous pouvez consulter toutes ces ressources directement ici. Toutefois, pour utiliser les exemples de code contenus dans les notebooks, vous devrez les exécuter sur votre ordinateur ou via un autre outil dans votre navigateur, comme expliqué ci-dessous.

## Contenu du dépôt

| Fichier | Description |
|---|---|
| `images/` | Dossier contenant les images et les captures d'écran que vous voyez dans le bootcamp |
| `.gitignore` | Liste des fichiers que Git ne doit pas enregistrer |
| `0_Installation-Python.md` | Guide d'installation de l'environnement Python (au besoin) |
| `1_Introduction.ipynb` | Introduction au bootcamp et prise en main de l'environnement |
| `2_Rappel-Python.ipynb` | Rappel des bases de Python scientifique |
| `3_Premier-Modèle.ipynb` | Construction d'un premier modèle numérique |
| `4_Qualité-Lisibilité.ipynb` | Qualité du code et bonnes pratiques |
| `5_Tests-Vérification.ipynb` | Tests automatisés et vérification |
| `6_Utilisation-IA.ipynb` | Utilisation responsable de l'IA générative |
| `7_Git-facultatif.md` | Introduction à Git *(facultatif)* |
| `LICENSE`| Le fichier contenant la licence open source de ce dépôt. |
| `README.md` | Ce fichier, qui donne un aperçu du dépôt |
| `requirements.txt` | Liste des bibliothèques nécessaires au bootcamp |

### Qu'est-ce que `requirements.txt` ?

Le fichier `requirements.txt` indique quelles bibliothèques Python sont nécessaires pour exécuter les notebooks du bootcamp.

Il peut notamment être utilisé pour installer automatiquement les dépendances avec :

```bash
pip install -r requirements.txt
```

Il est également utilisé par des services comme Binder pour préparer automatiquement l'environnement d'exécution des notebooks dans votre navigateur.

### Qu'est-ce que `.gitignore` ?

Le fichier `.gitignore` indique à Git quels fichiers ou dossiers ne doivent pas être enregistrés dans le dépôt.

Il peut par exemple exclure :

- des fichiers temporaires ;
- des caches Python ;
- des fichiers générés automatiquement ;
- des environnements virtuels ;
- certains fichiers propres au système d'exploitation.

Vous n'avez normalement pas besoin de modifier ce fichier pour réaliser le bootcamp.


# Comment accéder au matériel ?

Plusieurs options sont possibles.

### Option 1 — Lire le matériel directement sur GitHub

Les guides (`.md`) et notebooks Jupyter (`.ipynb`) peuvent être consultés directement dans votre navigateur.

Il suffit de cliquer sur le fichier souhaité.

Cette option est pratique si vous souhaitez :

- parcourir rapidement le contenu du bootcamp ;
- consulter une explication ;
- relire une section sans exécuter le code.

Les notebooks sont affichés dans le navigateur, mais ils ne sont pas exécutables directement dans l'interface standard de GitHub.

*(Insérer ici une capture d'écran.)*

---

### Option 2 — Télécharger un fichier individuel

Si vous souhaitez travailler localement sur un seul notebook ou guide, vous pouvez télécharger le fichier correspondant.

1. Ouvrez le fichier dans GitHub.
2. Cliquez sur le bouton **Download**.
3. Enregistrez le fichier sur votre ordinateur.

*(Insérer ici une capture d'écran du bouton Download.)*

Un notebook téléchargé peut ensuite être ouvert et exécuté dans VS Code, à condition d'avoir suivi le guide d'installation.

---

### Option 3 — Télécharger l'ensemble du dépôt

Si vous souhaitez réaliser l'ensemble du bootcamp sur votre ordinateur, il est généralement plus simple de télécharger tout le dépôt.

1. Cliquez sur le bouton **Code**.
2. Sélectionnez **Download ZIP**.
3. Enregistrez l'archive sur votre ordinateur.
4. Décompressez le fichier ZIP dans le dossier de votre choix.
5. Ouvrez le dossier décompressé dans VS Code.

*(Insérer ici une capture d'écran du bouton Code et de l'option Download ZIP.)*

Cette approche est recommandée pour la majorité des étudiants. Elle permet de conserver tous les fichiers du bootcamp dans un même dossier et de travailler localement dans VS Code.

---

### Option 4 — Cloner le dépôt avec Git

Si vous utilisez déjà Git, ou si vous souhaitez apprendre à l'utiliser, vous pouvez cloner le dépôt avec :

```bash
git clone ADRESSE_DU_DEPOT
```

Cette commande crée une copie complète du dépôt sur votre ordinateur.

L'avantage principal du clonage est qu'il devient ensuite facile de récupérer les mises à jour avec :

```bash
git pull
```

Une courte introduction à Git est disponible dans [7_Git-facultatif.md](7_Git-facultatif.md). 

Il n'est pas nécessaire de posséder un compte GitHub pour cloner un dépôt public.

---

### Option 5 — Exécuter les notebooks dans votre navigateur avec Binder

Les notebooks peuvent également être exécutés directement dans votre navigateur grâce à [Binder](https://mybinder.org). Binder prépare automatiquement un environnement Python à partir du dépôt et du fichier `requirements.txt`.

Aucune installation locale n'est nécessaire.

Cette option peut être utile si :

- vous souhaitez explorer rapidement le bootcamp ;
- vous utilisez un ordinateur sur lequel Python n'est pas installé ;
- vous rencontrez temporairement un problème avec votre installation locale.

Cependant, quelques limites doivent être connues :

- le démarrage peut prendre plusieurs minutes ;
- les performances sont généralement inférieures à une exécution locale ;
- les modifications ne sont pas conservées automatiquement ;
- la session peut être interrompue après une période d'inactivité.

Si vous souhaitez conserver votre travail effectué dans Binder, téléchargez les notebooks modifiés avant de fermer la session.

---

## Quelle option choisir ?

Pour la majorité des étudiants, nous recommandons le workflow suivant.

### Avant le premier TD

1. Suivez le guide :

   ```text
   0_Installation-Python.md
   ```

2. Installez Python, VS Code et les bibliothèques nécessaires.
3. Téléchargez l'ensemble du dépôt au format ZIP ou clonez-le avec Git.
4. Ouvrez le dossier du bootcamp dans VS Code.

### Pendant le bootcamp

Travaillez dans l'ordre suivant :

```text
1_Configuration.ipynb
2_Rappel-Python.ipynb
3_Premier-Modèle.ipynb
4_Qualité-Lisibilité.ipynb
5_Tests-Vérification.ipynb
6_Utilisation-IA.ipynb
```

La dernière partie est facultative :

```text
7_Git-facultatif.md
```

### Si vous souhaitez simplement consulter le matériel

Vous pouvez lire directement les fichiers sur GitHub.

### Si vous ne pouvez pas installer Python immédiatement

Vous pouvez utiliser [Binder](https://mybinder.org) pour exécuter les notebooks dans votre navigateur.


# Comment travailler dans les notebooks ?

Tout au long du bootcamp, vous rencontrerez les sections suivantes :

- 🎯 **Objectif** : ce que vous devriez apprendre ;
- ▶️ **À faire** : une action à réaliser ;
- ✍️ **Exercice** : un travail à effectuer vous-même ;
- ⚠️ **Vérification** : comment vérifier votre résultat ;
- 💡 **À retenir** : les idées importantes.

L'idée est simple : **Lire → Exécuter → Modifier → Observer → Vérifier**

Ne vous contentez pas d'exécuter les cellules sans les lire.

Essayez toujours de comprendre :

- ce que fait le code ;
- ce que vous vous attendez à obtenir ;
- si le résultat est plausible ;
- pourquoi une vérification réussit ou échoue.

Une grande partie de l'apprentissage de la programmation scientifique passe par l'expérimentation, les erreurs et leur correction.

# Quelques conseils

### Ne copiez pas simplement le code

Essayez toujours de comprendre :
- ce que fait le programme ;
- pourquoi il fonctionne ;
- ce que vous vous attendez à observer avant de l'exécuter.

### Vérifiez vos résultats

Un programme qui s'exécute sans erreur n'est pas nécessairement correct.

La vérification des résultats constitue une partie essentielle du travail d'ingénierie.

### Posez des questions

Si quelque chose ne fonctionne pas ou n'est pas clair, demandez de l'aide à l'équipe d'encadrement.

### Utilisation de l'intelligence artificielle

La responsabilité de vérifier un résultat appartient toujours à l'ingénieur, peu importe l'origine du code.

# Licence

Le contenu de ce dépôt est mis à disposition sous licence
**Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

Vous êtes libre de :

- partager ce matériel ;
- le copier et le redistribuer ;
- le modifier et l'adapter ;

à condition :

- d'en citer la source ;
- de redistribuer toute version modifiée sous la même licence.

Pour plus d'informations :

https://creativecommons.org/licenses/by-sa/4.0/deed.fr

# Besoin d'aide ?

Consultez d'abord `0_Installation-Python.md`.

Si le problème persiste, apportez votre ordinateur au TD et l'équipe d'encadrement pourra vous aider.

Bon bootcamp !