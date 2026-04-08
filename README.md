#Library management system

A menu-driven python application for managing a library's catalogue, members, and borrowing records.

#project purpose

The system allows library staff to:
- Maintain a searchable book catalogue
- Register and manage member accounts
- Process borrow and return transactions
- Track due dates and ientify overdue loans

All data is persisted automatically to CSV files so state is retained between sessions.

## Installation

**Requirements:** Python 3.8 or higher. No external packages are needed.

#Usage

### 1. seed the database with sample data

```bash
python seed_data.py
```

### 2. Launch the main application

```bash
python main.py
```

You will be presented with a numbered menu. Enter the corresponding number and follow the prompts.

### Example Session

```
Welcome to Gisma Library!

  Gisma Library — Main Menu
  [1]  List all books
  [2]  Search books
  [3]  Add a book
  ...
  [0]  Exit
  Enter option: 7

  Member ID: M001
  Book ISBN: 978-0-06-112008-4
  ✓ Borrow recorded. Due date: 2026-03-22
```
 ## key Features 

| Feature | Description |
|---|---|
| Book catalogue | Add, remove, and search books by title, author, or genre |
| Member management | Register members, view details and borrowing history |
| Borrow/return | Full transaction lifecycle with due date calculation |
| Overdue detection | Identify all currently overdue loans |
| CSV persistence | All data saved automatically to `data/` on every change |
| Error handling | Graceful messages for missing records, limit breaches, etc. |

## Project structure

```
library-management-system/
│
├── main.py              # Entry point — menu-driven CLI
├── seed_data.py         # Populate sample data
│
├── modules/
│   ├── __init__.py
│   ├── book.py          # Book class
│   ├── member.py        # Member class
│   ├── transaction.py   # Transaction class
│   └── library.py       # Library class (central controller + file I/O)
│
├── data/                # Auto-generated CSV data files
│   ├── books.csv
│   ├── members.csv
│   └── transactions.csv
│
└── README.md
