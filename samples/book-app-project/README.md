# Book Collection App

*(This README is intentionally rough so you can improve it with GitHub Copilot CLI)*

A Python app for managing books you have or want to read.
It can add, remove, list, and search books. It can also mark them as read.

---

## Current Features

* Reads books from a JSON file (our database)
* Search by author or by a publication year range
* Input checking is weak in some areas
* Some tests exist but probably not enough

---

## Files

* `book_app.py` - Main CLI entry point
* `books.py` - BookCollection class with data logic
* `utils.py` - Helper functions for UI and input
* `data.json` - Sample book data
* `tests/test_books.py` - Starter pytest tests

---

## Running the App

```bash
python3 book_app.py list
python3 book_app.py add
python3 book_app.py mark-read
python3 book_app.py find
python3 book_app.py search-year
python3 book_app.py remove
python3 book_app.py export-csv books.csv
python3 book_app.py help
```

### Search by Year

Use the `search-year` command to find books published between two years.

```bash
python3 book_app.py search-year
```

The app will then prompt you for:

- `Start year`
- `End year`

It shows books published within that inclusive range, so entering `1960` and `1980` includes books from both 1960 and 1980.

## Running Tests

```bash
python3 -m pytest tests/
```

---

## Notes

* Not production-ready (obviously)
* Some code could be improved
* Could add more commands later
