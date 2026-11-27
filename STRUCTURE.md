# Structure du dépôt / Repository layout

Les textes sont rangés par nature puis par année, en français (les noms que cherchent les juristes centrafricains). Un
dossier par texte, un fichier par article. Aucun dossier ne compte plus de 1 000 entrées.

Texts are filed by kind, then by year, with French names. One folder per text, one file per article. No folder holds
more than 1,000 entries.

```
constitution/                       Constitution du 30 août 2023 (préambule, un fichier par article)
constitution/anterieures/<année>-<texte>/   textes constitutionnels antérieurs (Charte de transition 2013, ...)
codes/<code>/                       les codes : codes/code-penal/, codes/code-du-travail/, codes/code-procedure-penale/,
                                    codes/code-minier/, codes/code-forestier/, ...
  art-001.md ... art-NNN.md         un fichier par article
  visas.md                          visas et préambule du texte qui adopte le code
  README.md                         source, date, couche texte, nombre d'articles
lois/<année>/<numéro>-<objet>/      lois et lois organiques (lois/2006/06-001-portant-.../)
ordonnances/<année>/<numéro>-<objet>/
decrets/<année>/<numéro>-<objet>/
arretes/<année>/<numéro>-<objet>/
decisions/<année>/<numéro>-<objet>/
cemac/<type>/<année>/<numéro>-<objet>/   droit communautaire CEMAC applicable en Centrafrique (traite/, reglements/,
                                    reglements-execution/, directives/, actes-additionnels/, actes/, decisions/)
corpus.json                         la liste de tous les textes (cf/national/acts)
```

- `<numéro>` reprend les groupes de chiffres du numéro officiel (`06.001` donne `06-001`) ; `<objet>` est tiré de
  l'intitulé.
- Un texte dont aucun article n'a été repéré est un seul fichier, `texte-integral.md`.
- Un code adopté à nouveau (par exemple le Code forestier de 1990 puis celui de 2008) reste dans le même dossier
  `codes/<code>/` : la nouvelle version est un nouveau commit qui remplace les fichiers de l'ancienne.
- Les décrets et arrêtés de nomination, d'affectation ou de promotion ne sont pas repris.
- Les décisions de justice (OHADA) sont dans un dépôt séparé et privé.
