# Book sources

The app fetches public-domain books from the sources listed below. None of
them require a user-bound API key; the only authentication some endpoints
accept is a server-side rate-limit token shipped via CI secrets.

| Source | Endpoint | Auth | Notes |
|--------|----------|------|-------|
| Feedbooks (public) | `https://catalog.feedbooks.com/catalog/public_domain.atom` | none | OPDS catalog |
| Project Gutenberg mirror | `https://www.gutenberg.org/ebooks/...` | none | HTML scraping |
| Internet Archive Bookreader | `https://archive.org/details/...` | none | OAuth optional for higher rate limits |
| Standard Ebooks | `https://standardebooks.org/feeds/atom/all` | none | Atom feed |

If you add a new source, append a row above and update the test fixture in
`test/services/source_fixtures_test.dart`.
