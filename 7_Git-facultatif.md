# Git pour GCH3545 (optionnel)
<p style="margin-top: -1.2em;">
Auteurs : Bruno Blais & Fabian Denner (Polytechnique Montréal)<br>
Licence : CC BY-SA 4.0
</p>

## Pourquoi ce guide ?

Dans le cadre du projet de GCH3545, vous allez développer du code Python, produire des graphiques et probablement modifier vos fichiers à plusieurs reprises.

Vous n'avez pas besoin d'utiliser Git pour réussir le cours.

Cependant, Git peut être un outil très utile pour :

- conserver l'historique de votre projet ;
- revenir à une version précédente ;
- travailler à plusieurs ;
- expérimenter de nouvelles idées sans risquer de perdre une version fonctionnelle.

Ce guide présente uniquement les concepts et commandes les plus utiles pour démarrer.

---

# 1. Le problème que Git cherche à résoudre

Considérez le dossier suivant :

```text
Projet/
├── modele.py
├── modele_final.py
├── modele_final_v2.py
├── modele_final_v2_corrige.py
├── modele_final_v2_corrige_final.py
├── modele_final_v2_corrige_final_VRAIMENT_FINAL.py
```

Après quelques semaines, plusieurs questions apparaissent :

- Quelle est la bonne version ?
- Quelles modifications ont été apportées ?
- Quand ces modifications ont-elles été faites ?
- Peut-on revenir à une version précédente ?
- Comment puis-je partager cela avec un membre de mon équipe ?

Git a été conçu pour résoudre ce problème.

---

# 2. Qu'est-ce que Git ?

Git est un système de contrôle de versions. Il permet d'enregistrer l'évolution d'un projet au fil du temps.

Avec Git, il est possible de :

- enregistrer des modifications ;
- consulter l'historique ;
- revenir à une version antérieure ;
- travailler à plusieurs ;
- créer des branches pour tester de nouvelles idées.

On peut voir Git comme une machine à remonter le temps pour un projet informatique.

---

# 3. Dépôt local et dépôt distant

Un dépôt (*repository*) est un dossier suivi par Git.

On distingue généralement :

- le dépôt local : sur votre ordinateur ;
- le dépôt distant : sur GitHub ou Gitlab.

```text
Votre ordinateur  ←→  GitHub/Gitlab
```

Le dépôt distant sert principalement à :

- **sauvegarder** le projet ;
- **partager** le projet ;
- **collaborer** avec d'autres personnes.

---

# 4. Workflow minimal

Il n'est pas indispensable d'utiliser Git dans le cadre de ce cours pour réussir. Toutefois, si vous décidez de l'utiliser, le workflow simple décrit ci-dessous suffit :

```text
Modifier un fichier
        ↓
    git add
        ↓
   git commit
        ↓
    git push
```

Pour récupérer les changements effectués sur GitHub :

```text
git pull
```

# 5. Utiliser un dépôt Git existant (aucun compte requis)

La manière la plus simple de commencer à utiliser Git consiste à récupérer un dépôt existant. Il existe, par exemple, d'innombrables logiciels et outils open source disponibles sur GitHub, que vous pouvez immédiatement cloner.

Par exemple, vous pourriez vouloir :

- télécharger le matériel du cours ;
- récupérer un projet open source ;
- consulter le code d'une bibliothèque Python ;
- récupérer le dépôt d'un projet partagé par un collègue.

Dans cette situation, vous n'avez pas besoin de créer votre propre dépôt ni même de posséder un compte GitHub.

### Cloner un dépôt

Ouvrez un terminal et accédez au dossier dans lequel vous souhaitez télécharger le dépôt. Ensuite, la commande suivante crée une copie complète du dépôt sur votre ordinateur :

```bash
git clone https://github.com/utilisateur/projet.git
```

Après l'exécution de cette commande, un nouveau dossier apparaît sur votre ordinateur. Vous pouvez ensuite ouvrir ce dossier dans VS Code et explorer son contenu comme n'importe quel autre projet.

### Mettre à jour le dépôt

Si de nouvelles modifications sont ajoutées au dépôt distant, vous pouvez les récupérer avec :

```bash
git pull
```

### Important

Pour ces opérations :

```text
✓ Aucun compte GitHub n'est nécessaire
✓ Aucune configuration Git n'est nécessaire
✓ Aucun commit n'est créé
```

À ce stade, Git est essentiellement utilisé comme un outil de téléchargement avancé.

---

# 6. Créer son propre dépôt Git

Si vous souhaitez suivre l'évolution de votre projet ou collaborer avec d'autres personnes, vous pouvez créer votre propre dépôt Git.

L'objectif est alors différent :

- enregistrer l'historique du projet ;
- conserver les différentes versions ;
- expérimenter de nouvelles idées ;
- faciliter le travail en équipe.

### Créer un dossier de projet

```bash
mkdir mon_projet
cd mon_projet
```

### Initialiser Git

```bash
git init
```

Cette commande indique à Git que ce dossier doit désormais être suivi. À partir de ce moment, Git pourra enregistrer les modifications apportées aux fichiers du projet.

---

# 7. Créer un compte GitHub

Git fonctionne parfaitement sur votre ordinateur sans GitHub.

Cependant, GitHub offre plusieurs avantages :
- sauvegarde du projet en ligne ;
- partage avec d'autres personnes ;
- collaboration au sein d'une équipe ;
- accès au projet depuis plusieurs ordinateurs.

Si vous souhaitez utiliser GitHub, vous devrez :
1. créer un compte ;
2. créer un dépôt sur GitHub ;
3. associer votre dépôt local au dépôt distant ;
4. envoyer vos modifications vers GitHub.

La création d'un compte sur GitHub et l'utilisation de ses fonctionnalités standard sont gratuites.

Dans le cadre de GCH3545, GitHub est particulièrement utile pour les projets réalisés en équipe. Outre GitHub, il existe d'autres solutions Git, telles que GitLab, qui peuvent également être hébergées en local ou sur votre propre serveur.

---

# 8. Configurer son identité Git

Cette étape n'est nécessaire que si vous souhaitez créer des commits.

Git utilise ces informations pour enregistrer l'auteur des modifications.

```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@polymtl.ca"
```

Vous pouvez vérifier votre configuration avec :

```bash
git config --list
```

Cette configuration n'a généralement besoin d'être effectuée qu'une seule fois.

---

# 9. Enregistrer des modifications

Supposons que vous ayez modifié un ou plusieurs fichiers du projet.

Git n'enregistre pas automatiquement ces changements.

Le processus comporte deux étapes.

### Vérifier l'état du projet

```bash
git status
```

Cette commande indique :

- quels fichiers ont été modifiés ;
- quels fichiers sont suivis ;
- quels fichiers sont prêts à être enregistrés.

C'est probablement la commande Git la plus utile lorsque vous débutez.

### Ajouter les modifications

Pour ajouter un fichier particulier :

```bash
git add modele.py
```

Pour ajouter tous les fichiers modifiés :

```bash
git add .
```

Cette étape prépare les fichiers pour le prochain commit.

### Créer un commit

```bash
git commit -m "Ajout du modèle de refroidissement"
```

Un commit peut être vu comme une photographie de l'état du projet à un instant donné.

Plus tard, il sera possible de revenir à un commit antérieur ou d'examiner l'historique du projet.

---

# 10. Utiliser Git dans VS Code

Même si Git peut être utilisé dans un terminal, la plupart des étudiants préféreront probablement utiliser l'interface graphique intégrée à VS Code.

VS Code permet d'effectuer la majorité des opérations courantes sans avoir à mémoriser les commandes Git.

### Voir les fichiers modifiés

*(Insérer ici une capture d'écran de l'onglet Source Control.)*

L'onglet **Source Control** affiche les fichiers modifiés depuis le dernier commit.

Il permet de répondre rapidement à des questions telles que :

- Quels fichiers ai-je modifiés ?
- Quels fichiers sont prêts à être enregistrés ?
- Ai-je oublié une modification importante ?

### Créer un commit

*(Insérer ici une capture d'écran du champ de message de commit.)*

Après avoir ajouté vos modifications, saisissez un message de commit descriptif puis cliquez sur **Commit**.

### Synchroniser avec GitHub

*(Insérer ici une capture d'écran du bouton Synchronize Changes ou Push/Pull.)*

VS Code permet d'envoyer et de récupérer des modifications directement depuis son interface.

### Changer de branche

*(Insérer ici une capture d'écran du sélecteur de branche.)*

Le sélecteur de branche permet de basculer rapidement entre différentes versions du projet.

---

# 11. Rédiger de bons messages de commit

Un bon message de commit explique clairement ce qui a été modifié.

Exemples :

```text
Ajout du modèle de refroidissement

Ajout de tests pour temperature_sphere

Correction d'une erreur dans le calcul de la température

Ajout d'une étude paramétrique sur k
```

Évitez autant que possible :

```text
Update

Fix

Test

Modifications
```

Ces messages ne donnent pratiquement aucune information sur les changements effectués.

---

# 12. Les branches

Les branches permettent de développer ou tester des idées sans modifier la version principale du projet.

On peut représenter la situation suivante :

```text
main
 \
  nouvelle_idee
```

La branche `main` contient généralement la version stable du projet.

La branche `nouvelle_idee` sert à tester un développement particulier.

Par exemple :

- une nouvelle méthode numérique ;
- un nouveau graphique ;
- une nouvelle fonctionnalité ;
- une idée proposée par un outil d'IA.

### Créer une branche

```bash
git checkout -b nouvelle_idee
```

Vous pouvez ensuite travailler librement dans cette branche sans affecter la version principale.

---

# 13. Pourquoi les branches sont utiles

Supposons que vous disposiez d'une version fonctionnelle du projet. Vous souhaitez essayer une modification importante.

### Option 1 : modifier directement la version principale

```text
Version fonctionnelle
        ↓
Modification importante
        ↓
Le projet ne fonctionne plus
```

Dans ce cas, revenir en arrière peut être difficile.

### Option 2 : créer une branche

```text
main
 \
  nouvelle_idee
```

La version stable reste disponible pendant que vous expérimentez.

C'est généralement l'approche recommandée.

---

# 14. Git et l'IA générative

Supposons qu'un outil d'IA vous propose une nouvelle implémentation :

```python
def nouveau_modele(...):
    ...
```

Faut-il remplacer immédiatement la version fonctionnelle ? Probablement pas.

Une approche plus prudente consiste à :

1. créer une branche ;
2. intégrer les modifications ;
3. exécuter les tests ;
4. vérifier les résultats ;
5. conserver uniquement les changements pertinents.

Git permet ainsi d'expérimenter avec davantage de sécurité.

---

# 15. Utilisation recommandée pour le projet en équipe

Une structure simple pourrait ressembler à :

```text
Projet/
│
├── src/
├── tests/
├── results/
└── README.md
```

Cette organisation sépare clairement :

- le code source ;
- les tests ;
- les résultats.

Une branche principale :

```text
main
```

peut être utilisée pour la version stable du projet.

Des branches supplémentaires peuvent être créées pour des développements particuliers :

```text
feature/nouveau_modele
feature/nouveaux_tests
feature/visualisation
```

Cette structure est largement suffisante pour un projet étudiant.

---

# 16. À retenir

Git ne rend pas un programme correct, ne remplace pas les tests et ne remplace pas la vérification. Cependant, Git facilite énormément la gestion des modifications et le travail collaboratif.

On peut résumer les bonnes pratiques vues dans ce bootcamp ainsi :

```text
Code lisible
+
Tests
+
Contrôle de versions
=
Projet plus robuste
```
