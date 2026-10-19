# Contributing a pack

1. Fork this repository and add `packs/<id>.json` (see the README for the shape). An `id` is
   lowercase words joined by hyphens, usually the title's.
2. Put full names in `strong` (they blur alone) and bare first names or surnames in `weak` (they
   blur only beside the title or a strong term). Never a plot event as a sentence: the linter
   refuses "X dies", and so would a reader.
3. Add `first_appearance` for any term whose first episode you know, as `S2E5`. A wrong, too-early
   episode would show a name to someone who has not met it yet; leave a term out when unsure.
4. Name yourself, and anyone who helped, in `credit`.
5. Open a pull request. The check runs on it; fix what it reports. A maintainer reviews the terms
   and merges, and the next daily build publishes the pack.

By contributing you agree that your pack is published under CC BY-SA 4.0.
