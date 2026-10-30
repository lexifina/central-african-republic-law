# Central African Republic: law history in git

The Constitution of the Central African Republic of 30 August 2023 and core statutes (listed below) as a git repository: one file per article, one paragraph per line, so `git blame` and `git diff` work line by line.

**Language: French**, the official language of the text. No official English text exists.

**What this repository is not, yet: a history.** The Constitution was approved by referendum on 30 July 2023 and promulgated on 30 August 2023 (published in the Journal officiel on 4 September 2023). It is one version, credited to the Constitution itself and dated by its promulgation. Earlier constitutions (2016, 2004) and most statutes are not in this repository: the state publishes no official online legal database. Each statute here is one version, as enacted.

**Where the text comes from.** The Central African Republic publishes no official online copy of the Constitution. The text is a third-party copy: the Digithèque MJP (Université de Perpignan), which cites the Journal officiel as its source. It may be published because the Bangui Agreement (OAPI), Annex VII, Article 6(i), which applies in the Central African Republic, excludes official texts of a legislative nature from copyright protection. The clause is quoted in [`LICENSE`](LICENSE). Spelling and typographical slips of the printed text are kept as they are. Titles, chapters and sections headings are not kept as separate files.

## What it holds

| Folder | Text | Versions |
| --- | --- | ---: |
| `constitution/` | Constitution de la VIIe République (30 août 2023): preamble and Articles 1 to 186 | 1 |
| `code-penal/` | Code pénal (loi n° 10.001 du 6 janvier 2010): Articles 1 to 447, as enacted | 1 |
| `code-du-travail/` | Code du travail (loi n° 09.004 du 29 janvier 2009): Articles 1 to 398, as enacted | 1 |
| `code-procedure-penale/` | Code de procédure pénale (loi n° 10.002 du 6 janvier 2010): Articles 1 to 504, as enacted | 1 |

## Dates

Each commit is dated at noon, Africa/Bangui. The Constitution is dated 30 August 2023, the day it was promulgated. The Code pénal and the Code de procédure pénale are dated 6 January 2010, the date of lois n° 10.001 and 10.002, and the Code du travail 29 January 2009, the date of loi n° 09.004; each law only orders its publication in the Journal officiel, so the law's own date is used. Later amendments to the statutes are not applied. The day is in the `In-force:` trailer.

## Source and licence

Source: Digithèque MJP, [mjp.univ-perp.fr/constit/cf2023.htm](https://mjp.univ-perp.fr/constit/cf2023.htm), retrieved 2026-10-30. The Code pénal comes from the copy held by WIPO Lex (record CF003), [wipolex-res.wipo.int/edocs/lexdocs/laws/fr/cf/cf003fr.pdf](https://wipolex-res.wipo.int/edocs/lexdocs/laws/fr/cf/cf003fr.pdf), retrieved 2026-10-30. The source marks no paragraph breaks inside an article, so each article is one paragraph, with its numbered items inline as printed. The Code du travail comes from the Journal officiel de la République centrafricaine, special edition of 7 September 2010, in the copy held by FAO FAOLEX, [faolex.fao.org/docs/pdf/caf158592.pdf](https://faolex.fao.org/docs/pdf/caf158592.pdf), retrieved 2026-10-30; its paragraphs are rebuilt from the layout of the two-column print. The Code de procédure pénale comes from the transcription of the Journal officiel special edition of 15 January 2010 published by Equipo Nizkor, [derechos.org/intlaw/doc/caf2.html](https://www.derechos.org/intlaw/doc/caf2.html), retrieved 2026-10-30. See [`LICENSE`](LICENSE).
