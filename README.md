# CascadiaGame

Projet Java de simulation du jeu Cascadia (mode terminal et mode graphique), avec gestion du score, scenarios et succes.

## 1. Contenu du projet

Le code principal est situe dans:

- `CascadiaGame-main/src/`
- `CascadiaGame-main/build.xml`
- `CascadiaGame-main/lib/` (dependances)
- `CascadiaGame-main/data/` et `CascadiaGame-main/hex/` (ressources visuelles)

## 2. Fonctionnalites

- Jeu de 1 a 4 joueurs.
- Tuiles carrees et tuiles hexagonales.
- Choix de variantes de score.
- Mode terminal et mode graphique.
- Gestion de succes/scenarios.

## 3. Prerequis

- JDK 23 (le build Ant active `--enable-preview -source 23`).
- Apache Ant.
- Bibliotheque `zen-6.0.jar` dans `CascadiaGame-main/lib/`.

## 4. Installation

```bash
cd CascadiaGame/CascadiaGame-main
ant compile
ant jar
```

## 5. Lancement

```bash
java -jar Cascadia.jar
```

## 6. Commandes utiles

```bash
ant clean
ant compile
ant jar
ant javadoc
```

## 7. Organisation technique

Paquets principaux:

- `fr.uge.cascadia`: logique jeu
- `fr.uge.cascadia.board`: plateau et placement
- `fr.uge.cascadia.cachroller`: controleurs
- `fr.uge.cascadia.score`: calcul des scores
- `fr.uge.cascadia.view`: rendu graphique

## 8. Points d'attention

- Le projet depend du JDK 23 preview.
- Le nom du package `cachroller` semble volontaire dans le code; ne pas renommer sans refactor global.
