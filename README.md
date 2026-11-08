# Buggy Rush : Turbo Édition

Portage expérimental du jeu HTML vers C++ avec Raylib, accompagné d'une configuration Android/Gradle et d'une compilation APK par GitHub Actions.

## État du projet

- Le portage C++ est un prototype : il ne reproduit pas encore toutes les fonctionnalités ni tous les graphismes du jeu HTML original.
- Le projet Android et le workflow de compilation doivent être validés par une vraie exécution CI avant de considérer l'APK comme prêt.
- Aucun APK compilé n'est publié pour le moment.

## Sources du projet

Le paquet de travail préparé précédemment contient les sources C++, les fichiers Android/Gradle et le workflow. Il doit être ajouté à ce dépôt avant de lancer la compilation.

## Compilation

Une fois les sources présentes à la racine du dépôt, le workflow Android pourra être lancé depuis l'onglet **Actions**. Le fichier APK de débogage sera alors fourni comme artefact si la compilation réussit.
