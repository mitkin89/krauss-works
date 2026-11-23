# Samuel Krauss – digital edition

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24465261.svg)](https://doi.org/10.5281/zenodo.24465261)

**English** · [Deutsch](README.de.md)

Two works of Samuel Krauss (1866–1948) on the language and material culture of the Talmud, transcribed from the printed volumes:

| Work | Content |
| --- | --- |
| *Griechische und lateinische Lehnwörter im Talmud, Midrasch und Targum*, part II (Berlin 1899), with notes by Immanuel Löw | the dictionary of Greek and Latin loanwords: 6,329 entries, abbreviations explained, references to Bible, Mishnah, Tosefta, Talmud and Midrash resolved – as JSON and as DSL dictionary |
| *Talmudische Archäologie*, vols. I–III (Leipzig 1910–1912) | the full text, §§ 1–300 and the *Nachträge und Berichtigungen*, with all 8,657 notes and 75 figures; the index of vol. III (11,727 entries) as a dictionary linked to the paragraphs; the bibliography of the works Krauss cites |

The data were prepared for the free desktop library [Safran](https://github.com/mitkin89/Safran), where the *Archäologie* is part of the library and both registers work as dictionaries.

## Contents

| Path | Content |
| --- | --- |
| `lehnwoerter/krauss-lehnwoerter-2.json` | `{"title", "entries": [{"heads", "html", "text"}]}` |
| `lehnwoerter/krauss-lehnwoerter-2.dsl` | the same as a DSL dictionary (UTF-8 with BOM) |
| `lehnwoerter/abbreviations.json` | the list of sources and abbreviations (Löw), with additions marked |
| `talmudische-archaeologie/talmudische-archaeologie.json` | `{"title", "sections": [{"section", "title", "paragraphs": [html, …]}]}` – section = the printed paragraph number (§ 1–300; the last section holds the addenda) |
| `talmudische-archaeologie/talmudische-archaeologie.md` | the same as Markdown, notes as footnotes `[^§.n]` |
| `talmudische-archaeologie/figures/` | the figures of the print |
| `talmudische-archaeologie/register.json`, `register.dsl` | the index of vol. III; links point to `Talmudische Archäologie <section>:<paragraph>` |
| `talmudische-archaeologie/bibliography.json` | short titles of the cited literature with the full title |

### HTML markup

- `<abbr class="gab" data-t="…">` – an abbreviation (or a short title, class `kbib`) with its expansion.
- `<a class="dsrc" data-sref="…">` – a reference resolved to a [Sefaria](https://www.sefaria.org)-style reference.
- In the *Archäologie*, a note is `<sup class="footnote-marker">n</sup><i class="footnote">…</i>` at the place of the note number.
- In the dictionaries, `<div class="dl" style="margin-left:Nem">` is one paragraph of the entry.

## Method and reliability

- The pages were transcribed with Claude (Anthropic, 2026) from page images in eScriptorium (*Archäologie*: digitizations of the Getty Research Institute on the Internet Archive); abbreviations, short titles and references were marked by script.
- This is a working transcription, **not a critical edition**; it has not been proofread completely against the print. Please report errors as an issue, with headword or paragraph.

## License

- Samuel Krauss (†1948) and Immanuel Löw (†1944): the printed works are in the **public domain**.
- The transcriptions, the structured data, the DSL files, the figures as extracted and the lists: **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**, see [LICENSE.md](LICENSE.md).

## Citation

Itkin, Igor Mendel (ed.): *Samuel Krauss – digital edition*, version 1.0.0, 2026. https://doi.org/10.5281/zenodo.24465261

See [CITATION.cff](CITATION.cff). Each release is archived on Zenodo with its own DOI.
