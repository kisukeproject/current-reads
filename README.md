# 📖 currently-reading

A lightweight, automated JSON datastore tracking current reading progress. 

This repository acts as a headless, read-only data layer. Rather than exposing a live backend to the public web, state updates are committed directly here, allowing static frontends to safely fetch the data.

## ⚙️ The Pipeline

1. **Recap:** A daily recap takes place.
2. **Extraction:** Kisuke parses the active reading status.
3. **Commit:** Kisuke pushes an updated JSON payload to this repo.
4. **Fetch:** Client-side applications request the raw file.

## 🌐 Consumers

This data is actively pulled by:

* **[alxhdd.com](https://alxhdd.com)** *(Personal Portfolio)*
* **[kisukeproject.pl](https://kisukeproject.pl)** *(System Hub)*

## 📄 Data Shape 

```json
{
  "title": "Book Title",
  "author": "Author Name",
  "link": "url",
  "last_updated": "YYYY-MM-DD"
}
