# Plot Armor community packs

Spoiler packs written by people who know a show, for [Plot Armor](https://nickharder.github.io/plot-armor-site/privacy.html)
(a placeholder name). A pack lists the names and words that spoil a title; the extension blurs
them on the pages a person reads. Packs here are reviewed by pull request, checked automatically,
and, once merged, carried in the extension's signed daily file with a **Community** badge.

## What a pack looks like

One JSON file per title in `packs/`, named after the pack's `id`, in the
pack schema (below, and in `schema.json` here):

```json
{
  "schema_version": 1,
  "id": "harbor-lights",
  "title": "Harbor Lights",
  "quality": "community",
  "aliases": ["Harbor Lights"],
  "triggers": ["Harbor Lights", "#HarborLights"],
  "strong": ["Ottoline Varga", "Brannock Hale"],
  "weak": ["Varga"],
  "require_context_for": [],
  "exclude_phrases": [],
  "first_appearance": { "Ottoline Varga": "S1E1" },
  "credit": "Your name or handle, and anyone who helped"
}
```

The popup can write one for you: add your own terms, then "Export your own terms as a pack".

## The rules a pack must pass

Every pull request runs the same check the daily build runs before signing:

- the file is named after its `id`, its `quality` is `community`, and `credit` names its authors;
- its `id` is not one of the extension's curated packs;
- it passes the schema, and the linters: no common English word as a strong term, no term that
  reads as a spoiler sentence, no slur, no link or markup;
- its terms blur at most 1% of a corpus of ordinary pages;
- a new version keeps at least four fifths of the strong terms of the version already published.

A maintainer then reviews the terms and merges. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Licence

Everything here is under [CC BY-SA 4.0](LICENSE): anyone may use and adapt the packs, crediting
their authors (the `credit` field) and sharing adaptations under the same licence.
