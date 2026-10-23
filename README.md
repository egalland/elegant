# Élégant — Sculptures de données

Atelier de visualisation 3D en pixels, réalisé avec Emmanuel Galland pour le mot **Élégant**, jour 23 d’Inktober 2026.

- [Ouvrir l’application](https://egalland.github.io/elegant/)
- [Calendrier Inktober](https://egalland.github.io/)

## Utiliser

Télécharger `index.html` et l’ouvrir dans un navigateur moderne. Ce fichier contient le style, le JavaScript et la favicon : aucune installation, dépendance ou compilation nécessaire.

Importer un CSV, TSV, tableau Excel collé, JSON ou une API JSON publique. Associer le libellé et la valeur ; X, Y et Z sont facultatifs pour la constellation. Choisir ensuite une représentation sans réimporter les données.

## Représentations

Filaments souples en 3D, colonnes isométriques, ruban en relief, radar, anneau et constellation X/Y/Z. Rotation par glisser, zoom à la molette ou avec les boutons ; navigation clavier sur le graphique (flèches, +/−, Origine). Les valeurs sont accessibles par survol, toucher et liste d’observations.

Les longueurs et hauteurs représentent les valeurs ; les secteurs de l’anneau représentent les parts du total. Les directions des filaments, la grille des colonnes et la profondeur du ruban sont décoratives, sans variable supplémentaire implicite. Sans X/Y/Z associés, la constellation est illustrative.

## Données et limites

1 à 200 observations ; intensités positives ou nulles ; X/Y/Z peuvent être négatifs. Import brut limité à 2 Mo. Les données et réglages sont conservés dans le stockage local du navigateur, sans compte ni serveur applicatif. Changer de navigateur, de fichier ou d’origine web sépare ces stockages.

L’appel à une API est déclenché manuellement, en HTTPS et sans identifiants ; le serveur source doit autoriser CORS. L’URL API n’est pas sauvegardée. Ne pas fournir de clé secrète. Export PNG intégré. Les données initiales sont explicitement marquées comme démonstration.

## Organisation

- `index.html` : application autonome prête à ouvrir ou héberger.
- `src/` : sources HTML, CSS et JavaScript lisibles.
- `scripts/build.py` : assemble les sources dans `index.html` avec Python standard.
- `docs/creation.json` : fiche de création, périmètre, estimations et provenance.
- `docs/historique.md` : correspondance des étapes importées.
- `docs/source-history.json` : identifiants et dates des versions source.

Pour reconstruire : `python3 scripts/build.py`. Aucune bibliothèque tierce : rendu WebGL avec repli Canvas, projection 3D et particules calculées dans le navigateur.

## Historique et temps

Les cinq versions source ont été réimportées dans l’ordre sous le compte **egalland**. Les commits GitHub datent de l’import ; les identifiants et dates source sont conservés dans `docs/`. Les fichiers de configuration d’hébergement privé sont exclus.

Conception/prompt : **15 min estimées** ; réalisation assistée, corrections et publication : **75 min estimées** ; total Vibe Coding : **90 min estimées**. Développement manuel équivalent : **32 h estimées**, fourchette **24–48 h**. Ces durées ne sont pas des mesures de temps actif ; voir la méthode et les limites dans la fiche de création.
