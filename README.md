# US trademark mirror (live marks)

A compact, searchable copy of the live US trademarks in USPTO's public trademark data, for automated name screening.

- **Source:** USPTO Trademark Full Text XML (annual set plus daily files), downloaded through USPTO's official
  Open Data Portal API. USPTO data is public domain. This mirror is not affiliated with or endorsed by USPTO.
- **What's in it:** only marks USPTO lists as live, with mark text, serial number, registration number, status code,
  international classes and owner. Owners who are individuals are shown as "an individual"; addresses, attorneys and
  goods/services text are left out.
- **Layout:** `meta.json` (build date, data dates, counts) and `shards/<xx>.json`, where `xx` is the first two letters
  or digits of the mark with everything except a-z and 0-9 removed and lowercased. Each shard maps that normalized
  mark to `[[mark, serial, registration, status, [classes], owner], ...]`.
- **Updates:** rebuilt weekly from USPTO's daily files.
- **Not legal advice.** This is screening, not a clearance search; check USPTO's official records
  (https://tmsearch.uspto.gov) and a trademark attorney before relying on a name.
