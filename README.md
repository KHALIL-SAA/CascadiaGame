# CascadiaGame

Simulation Java du jeu Cascadia avec interface terminal et interface graphique.

## Resume

Ce projet implemente les mecaniques principales du jeu Cascadia: placement de tuiles habitats, gestion des jetons animaux, scoring selon cartes de score, et gestion de scenarios/succes.

## Fonctionnalites

- Partie multi-joueurs.
- Variantes de score pour les animaux.
- Gestion des habitats et connexites.
- Mode terminal pour tests rapides.
- Mode graphique pour jeu interactif.
- Scenarios et systeme de succes.

## Structure du projet

```text
src/fr/uge/cascadia/
	animal/        # jetons, types, cartes animaux
	board/         # plateau, shelf, placement
	controller/    # logique de controle terminal/graphique
	score/         # strategies de scoring
	success/       # gestion des succes/scenarios
	tile/          # definitions des tuiles
	view/          # rendu graphique

data/            # ressources images animales
hex/             # ressources tuiles hexagonales
docs/doc/        # javadocs generees
build.xml        # build Ant
```

## Prerequis

- Java JDK 23 (preview active dans le build Ant).
- Apache Ant.
- Bibliotheque `lib/zen-6.0.jar`.

## Build

```bash
ant clean
ant compile
ant jar
```

Jar genere: `Cascadia.jar`

## Lancement

```bash
java -jar Cascadia.jar
```

## Documentation technique

Generer la javadoc:

```bash
ant javadoc
```

Sortie dans `docs/doc/`.

## Donnees et fichiers utiles

- `Scenarios.txt`: definition des scenarios.
- `successNormal.txt`: succes standards.
- `initialTiles.txt`: tuiles de depart.
- `hexagoTilesFile.txt`: configurations hexagonales.

## Limitations connues

- Le build depend de `--enable-preview` et `-source 23`.
- Projet pense pour environnement Java desktop (pas web).

## Pistes d'amelioration

- Ajout de tests unitaires systematiques.
- Sauvegarde/reprise de partie.
- IA de suggestion de coups.
- Packaging multiplateforme.
