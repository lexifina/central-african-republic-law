# How this repository was made (Central African Republic)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Digithèque MJP (Jean-Pierre Maury, Université de Perpignan): Centrafrique, Constitution de 2023 | <https://mjp.univ-perp.fr/constit/cf2023.htm> | 2026-10-30 | Official legislative texts are not protected by copyright: Bangui Agreement (OAPI), Annex VII, Article 6(i) |
| WIPO Lex: Loi n° 10.001 du 6 janvier 2010 portant Code pénal centrafricain (CF003) | <https://wipolex-res.wipo.int/edocs/lexdocs/laws/fr/cf/cf003fr.pdf> | 2026-10-30 | text of law, not protected by copyright (Bangui Agreement, Annex VII, art. 6(i)); WIPO Lex terms: CC BY 4.0 for WIPO content |
| Journal officiel de la République centrafricaine, édition spéciale du 7 septembre 2010: Loi portant Code du travail (PDF held by FAOLEX) | <https://faolex.fao.org/docs/pdf/caf158592.pdf> | 2026-10-30 | official text, not protected by copyright (Bangui Agreement, Annex VII, art. 6(i)) |
| Equipo Nizkor / Derechos Human Rights: Loi n° 10.002 portant Code de procédure pénale centrafricain (transcription of the JORCA special edition of 15 January 2010) | <https://www.derechos.org/intlaw/doc/caf2.html> | 2026-10-30 | official text, not protected by copyright (Bangui Agreement, Annex VII, art. 6(i)); the host cites fair use for its copy |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Constitution de la VIIe République (30 août 2023) | 1 | 2023-08-30 to 2023-08-30 |
| `code-penal` | Loi n° 10.001 du 6 janvier 2010 portant Code pénal centrafricain | 1 | 2010-01-06 to 2010-01-06 |
| `code-du-travail` | Loi n° 09.004 du 29 janvier 2009 portant Code du travail de la République centrafricaine | 1 | 2009-01-29 to 2009-01-29 |
| `code-procedure-penale` | Loi n° 10.002 du 6 janvier 2010 portant Code de procédure pénale centrafricain | 1 | 2010-01-06 to 2010-01-06 |

The build made 4 commits:

| Commits | Kind |
| ---: | --- |
| 4 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 1 laws in the record.
- 5 tags.

## Dates

Each commit is dated at noon (Africa/Bangui) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: The 2023 Constitution was adopted by referendum on 30 July 2023 and promulgated on 30 August 2023; it was published in the Journal officiel (JORCA ES no 9) on 4 September 2023. It is dated by its promulgation. https://mjp.univ-perp.fr/constit/cf2023.htm

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `445ffb25ccba9638d456f19bc1f6ab1d8bc3e51e474ba0a4bd4efc655dfd7f0f` (977326 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

4 versions of 4 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

A second build from the same corpus into an empty folder gave identical hashes for all 4 history commits and 5 tags (history tip `91e2489a0ac4a46d1f1a90877a54177bac2c0020`).

## Decisions made by hand

- French is built: it is the official language of the text. No official English text exists.
- The Central African Republic publishes no official online copy of the Constitution. The text is a third-party copy: the Digithèque MJP HTML page, which states that its source is the JORCA ES no 9 of 4 September 2023. The host is credited as the source of the bytes.
- The Bangui Agreement (OAPI) Annex VII, Article 6(i), in force in the Central African Republic as an OAPI member, excludes "textes officiels de nature legislative, administrative ou judiciaire" from copyright protection; that is why the copy may be published.
- The version is dated by the promulgation (30 August 2023), the day the Constitution was enacted; the publication in the Journal officiel was on 4 September 2023.
- Titles, chapters and sections headings are not kept as files; articles keep their number. Obvious typographical errors in the printed text (for example "existnce", "sels Centrafricains") are kept as printed.
- Code pénal: one version, the Code as enacted (first_law null, oldest version available), dated 2010-01-06, the date of loi n° 10.001; its article 447 only orders publication in the Journal officiel (reported as the issue of 15 January 2010, not seen), so the law date is used. Later amendments are not applied.
- Code pénal units: one per article (art-001 to art-447); the source marks no paragraph breaks inside an article, so each article is one paragraph, with its enumerations inline as printed; Titre, Chapitre and Section headings, the promulgation formula and the signature are left out.
- Code du travail: one version, the Code as enacted (first_law null, oldest version available), dated 2009-01-29, the date of loi n° 09.004; its article 398 only orders publication in the Journal officiel, and the copy read is the special edition of 7 September 2010, so the law date is used. Later amendments are not applied.
- Code du travail units: one per article (art-001 to art-398); paragraphs and list items are rebuilt from the vertical gaps of the two-column print; Titre, Chapitre, Section and Sous-section headings, the table of contents, the running heads, the promulgation formula and the signature are left out.
- Code de procédure pénale: one version, the Code as enacted (first_law null, oldest version available), dated 2010-01-06, the date of loi n° 10.002; its article 504 only orders publication in the Journal officiel (special edition of 15 January 2010, per the host), so the law date is used. Later amendments are not applied.
- Code de procédure pénale units: one per article (art-001 to art-504); paragraphs and list items follow the HTML paragraphs and line breaks of the transcription; centred Titre, Chapitre and Section headings, the table of contents, the promulgation formula and the signature are left out. The ICC Legal Tools copy of the Journal officiel is a scanned image with a machine-read text layer and was not used.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code wrote the parser and chose the source; it did not write or alter any legal text.
- Claude Code wrote the code and chose the source; it did not write or alter any legal text. The code is deterministic and runs no model.
- Claude Code wrote the code and chose the source; it did not write or alter any legal text. The code is deterministic and runs no model.
- Claude Code wrote the code and chose the source; it did not write or alter any legal text. The code is deterministic and runs no model.
