# Publishing Dashboard

This page is designed to work especially well with the **Dataview** community plugin.

## Concepts by status

```dataview
TABLE status, domain, confidence, youtube, instagram, newsletter, website, book
FROM "02 - Foundations" OR "03 - Mind & Human Nature" OR "04 - Thinking & Rationality" OR "05 - Society & Civilization" OR "06 - Living Well" OR "07 - Practice"
WHERE type = "concept"
SORT importance DESC, file.name ASC
```

## Concepts missing social content

```dataview
TABLE status, domain, file.link
FROM "02 - Foundations" OR "03 - Mind & Human Nature" OR "04 - Thinking & Rationality" OR "05 - Society & Civilization" OR "06 - Living Well" OR "07 - Practice"
WHERE type = "concept" AND instagram = false
SORT importance DESC
```

## Concepts missing YouTube

```dataview
TABLE status, domain, file.link
FROM "02 - Foundations" OR "03 - Mind & Human Nature" OR "04 - Thinking & Rationality" OR "05 - Society & Civilization" OR "06 - Living Well" OR "07 - Practice"
WHERE type = "concept" AND youtube = false
SORT importance DESC
```

If you do not want community plugins, simply use the folders, links, and built-in graph/backlinks.
