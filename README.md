# INVOICE CLI

A command line invoice management tool for sole traders. Manage clients, create and send professional PDF invoices, track payments, and calculate revenue of a given time period. 

## Features

- **Client management** - Add and remove clients with automatic unique client ids to keep them distinct and separate
- **Line-item invoices** - Line items with a date, quantity, and rate
- **PDF generation** - Professionally formatted PDFs generated automatically when an invoice is added
- **Invoice codes** - Unique codes generated based on client name and number of invoices sent to them
- **Revenue filtering by date range** - Calculates revenue of invoices paid within date range (inclusive)
- **Financial year folder organisation** - Auto-creates folder path in destination to categorise invoices by financial year


## Requirements: 
- Python 3.x
- pip install reportlab tabulate

## Setup: 
- Clone the repo from github. 
- Copy the config_example.py and rename it config.py, and fill in your business details.

## Usage

**add-client** - Add a new client

```
python invoice_cli.py add-client --name "Jane Smith" --email jane@example.com --phone 0412345678 --address "123 Main St"
```

**remove-client** - Remove a client and all associated invoices

```
python invoice_cli.py remove-client --client-id 1
```

**show-clients** - Shows table of all current clients

```
python invoice_cli.py show-clients
```

**add-invoice-with-items**

```
python invoice_cli.py add-invoice-with-items --client-id 1 --issue-date 2026-07-09
```
## Usage: 
The following are commands:

**add-client** - Add a new client

python invoice_cli.py add-client --name "Jane Smith" --email jane@example.com --phone 0412345678 --address "123 Main St"
- **add-client** - Takes the client details --name --email --address --phone and creates a new client storing it in SQLite, with a unique client_id (an integer)
- **remove-client** - Takes the --client-id and removes the corresponding client with a delete cascade removing all invoices and invoice items addressed to that client.


one block per command showing the actual command and what it does



File structure: what invoice_cli.py, database_functions.py, pdf_generator.py each do
