# HiH Project — Hypertext and Hypermedia

## XML Model: _Reading Hobby_

Project created for the **Hypertext and Hypermedia** course. This repository presents a complete example of information modeling in XML, featuring validation based on **DTD** and **XML Schema (XSD)**.
The example describes the author's _reading hobby_ and a collection of books, enriched with multimedia elements and hypertext structure.

---

## 📂 Repository Contents

- **`ksiazki.xml`** – the main XML document describing the reading hobby:
  - author data (metadata),
  - reading summary and statistics,
  - favorite genres along with authors,
  - a list of books containing:
    - full bibliographic data,
    - references to multimedia elements,
    - links (hypertext) to reviews / videos,
    - attributes for rating, status, etc.

- **`ksiazki.dtd`** – DTD definition describing the permissible structure:
  - document and element model,
  - content types,
  - required and optional elements and attributes.

- **`ksiazki.xsd`** – XML Schema 1.0 definition:
  - precise data typing (e.g., numbers, dates, units),
  - validation of nested structures,
  - namespace definitions.

---

## 🌐 Namespaces and Validation

The XML document uses namespaces:

- `xmlns="http://example.org/hobby"` – the main namespace for all elements,
- `xmlns:h="http://example.org/hobby"` – an alias used, for example, with the `h:jezyk` attribute,
- `xsi:schemaLocation` indicates the link to the XSD schema.

The document employs:

- **XSD validation** (primary),
- **DTD compliance** (structural).

---

## 🧩 Project Features

- Advanced XML structure covering:
  - nested metadata (e.g., annual statistics, reading formats),
  - semantic structure (genres, authors, books),
  - hypertext references (links to pages and materials),
  - multimedia elements (covers, video reviews),
  - attributes controlling semantics (e.g., `status`, `ocena`, `jezyk`, `rola`).

- Usage of:
  - XML namespaces,
  - data type validation in XSD,
  - complex attributes and enumerations,
  - full validation using the `.xsd` file.

---

## ▶️ How to Run and Verify XML

### 1. XSD Validation (e.g., via `xmllint`)

```bash
xmllint --noout --schema ksiazki.xsd ksiazki.xml
