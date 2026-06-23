# Ceneo Web Scraper

Prosty projekt w Pythonie do pobierania opinii o produkcie z serwisu Ceneo.

## Funkcjonalności

Skrypt pobiera informacje o opiniach, m.in.:

* identyfikator opinii,
* autora,
* ocenę,
* rekomendację,
* treść opinii,
* zalety i wady,
* liczbę głosów „pomocna” / „niepomocna”,
* datę publikacji i czas użytkowania produktu.

Dane są zapisywane do pliku `opinions.json`.

## Wymagania

Projekt korzysta z bibliotek:

```bash
pip install requests beautifulsoup4
```

## Uruchomienie

1. Otwórz plik notebooka `.ipynb` w Visual Studio Code lub Jupyter Notebook.
2. Zainstaluj wymagane biblioteki.
3. W komórce z konfiguracją ustaw identyfikator produktu:

```python
product_id = "124893467"
```

4. Uruchom notebook kolejno od pierwszej komórki.
5. Po zakończeniu działania w folderze projektu pojawi się plik:

```text
opinions.json
```

## Struktura danych

Każda opinia jest zapisana jako obiekt JSON, np.:

```json
{
    "opinion_id": "17657913",
    "author": "l...z",
    "recommendation": "Polecam",
    "stars": "5/5",
    "content": "Treść opinii...",
    "pros": [],
    "cons": [],
    "helpful": "0",
    "unhelpful": "0",
    "publish_date": "3 lata temu,",
    "purchase_date": "po 3 tygodniach"
}
```

## Uwagi

Projekt ma charakter edukacyjny. Scraper pobiera opinie dostępne na stronie produktu w momencie wysłania zapytania. Nie należy umieszczać w kodzie plików cookies, tokenów ani innych prywatnych danych.
