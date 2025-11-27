# Projekt HiH — Hipertekst i Hipermedia

## Model XML: _Hobby czytelnicze_

Projekt wykonany na potrzeby przedmiotu **Hipertekst i Hipermedia**. Repozytorium prezentuje kompletny przykład modelowania informacji w XML, wraz z walidacją w oparciu o **DTD** i **XML Schema (XSD)**.  
Przykład opisuje _hobby czytelnicze_ autora oraz zestaw książek wzbogacony o elementy multimedialne i strukturę hipertekstową.

---

## 📂 Zawartość repozytorium

- **`ksiazki.xml`** – główny dokument XML opisujący hobby czytelnicze:

  - dane o autorze (metadane),
  - podsumowanie i statystyki czytelnicze,
  - ulubione gatunki wraz z autorami,
  - lista książek z:
    - pełnymi danymi bibliograficznymi,
    - odwołaniami do elementów multimedialnych,
    - linkami (hipertekst) do recenzji / filmów,
    - atrybutami oceny, statusu itd.

- **`ksiazki.dtd`** – definicja DTD opisująca dopuszczalną strukturę:

  - model dokumentu i elementów,
  - typy zawartości,
  - wymagane oraz opcjonalne elementy i atrybuty.

- **`ksiazki.xsd`** – schemat XML Schema 1.0:
  - dokładne typowanie danych (np. liczby, daty, jednostki),
  - walidacja struktur zagnieżdżonych,
  - definicje przestrzeni nazw.

---

## 🌐 Przestrzenie nazw i walidacja

Dokument XML używa przestrzeni nazw:

- `xmlns="http://example.org/hobby"` – główna przestrzeń dla wszystkich elementów,
- `xmlns:h="http://example.org/hobby"` – alias używany np. przy atrybucie `h:jezyk`,
- `xsi:schemaLocation` wskazuje powiązanie ze schematem XSD.

W dokumencie zastosowano:

- **walidację przez XSD** (główna),
- **zgodność z DTD** (strukturalna).

---

## 🧩 Cechy projektu

- Zaawansowana struktura XML obejmująca:

  - zagnieżdżone metadane (np. statystyki roczne, formaty czytania),
  - strukturę semantyczną (gatunki, autorzy, książki),
  - odwołania hipertekstowe (linki do stron i materiałów),
  - elementy multimedialne (okładki, recenzje wideo),
  - atrybuty kontrolujące semantykę (np. `status`, `ocena`, `jezyk`, `rola`).

- Zastosowanie:
  - przestrzeni nazw (XML namespaces),
  - walidacji typów danych w XSD,
  - atrybutów złożonych i enumeracji,
  - pełnej walidacji za pomocą pliku `.xsd`.

---

## ▶️ Jak uruchomić i zweryfikować XML

### 1. Walidacja XSD (np. `xmllint`)

```bash
xmllint --noout --schema ksiazki.xsd ksiazki.xml
```
