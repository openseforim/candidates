# Open Seforim: candidate works

Works that could become new [Open Seforim](https://openseforim.org/) readers: source text from page scans,
checked against the scans, with an English translation.

The list is shown on the site at **[openseforim.org/next/](https://openseforim.org/next/)**, which is built
from the files in [`candidates/`](candidates/).

**Suggest a work:** [open a suggestion](https://github.com/openseforim/candidates/issues/new?template=suggest-a-work.yml).
Corrections and information about a listed work (a better scan, an existing translation, a copyright question)
are welcome as an issue too.

## One file per work

Each file in `candidates/` starts with a header of `key: value` lines between `---` marks, then free notes.

| Key | Meaning |
|---|---|
| `title` | Author, *Title* (book titles between asterisks, shown in italics) |
| `title_he` | Hebrew title, if any |
| `author`, `published`, `language` | Author with dates; editions and places; languages and scripts in the text |
| `status` | `proposed` (not checked yet), `researched` (scans and existing work checked), `started` (now a reader), `set-aside` (with a `reason`) |
| `reader` | The reader's URL, when `status: started` |
| `added`, `checked` | Dates as DD-Mon-YYYY; `checked` says what was checked |
| `why` | Why the work is useful, in one or two sentences |
| `scans` | Where the page scans are (links) |
| `existing` | Existing transcriptions and translations (links) |
| `reason` | Why a work is set aside |

Text in the header and notes can use `*italics*`, `**bold**` and `[links](https://...)`.

## Before work starts on any of these

- **Public domain (rough rule):** EU = the author died 70 or more years ago; US = published before 1931.
  A modern edition of an old text can still be in copyright.
- **Check existing projects first:** Sefaria (texts and dictionaries), Ben-Yehuda, Wikisource (he, de), the
  Frankfurt and Halle digital collections (scans only, no usable OCR so far), HathiTrust full text, and the
  Dicta and Bar-Ilan corpora.
- Frankfurt's scans of Löw's Flora have no OCR text layer (checked 31-Oct-2026). Check other scans the same way.
- **Cost of one full work** (Nov-2026 prices): about 500 pages per volume × about $0.10 per page for OCR and
  about $0.08 per page for translation with Claude Opus 5.5 through OpenRouter.
- **OCR at no cost per page:** for works mostly in one script (Hebrew, Syriac, Latin and the like), the
  open-source [Kraken](https://kraken.re/) OCR engine with a ready model can do the OCR locally, at no cost per page.
  On a rented GPU it is much faster (best for a long work or for fine-tuning a model). It worked on the Emden
  (Hebrew) and Barhebraeus (Syriac, about 95% of words matched) readers. Works that mix scripts on one line
  (German or Latin with Hebrew, Greek and Arabic, as in Löw or Bochart) still need a vision model, or Kraken
  with a second pass. Check a few pages by hand either way.

The list started in the Löw reader's repository (`TARGETS.md`, 31-Oct-2026) and moved here on 23-Nov-2026.

## Licence

The text of this repository: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
