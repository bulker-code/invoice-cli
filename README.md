# INVOICE CLI

A command line invoice management tool for sole traders. Manage clients, create and send professional PDF invoices, track payments, and calculate revenue of a given time period. 

## Features

- **Client management** - Add and remove clients with automatic unique client ids to keep them distinct and separate
- **Line-item invoices** - Line items with a date, quantity, and rate
- **PDF generation** - Professionally formatted PDFs generated automatically when an invoice is added
- **Invoice codes** - Unique codes generated based on client name and number of invoices sent to them
- **Revenue filtering by date range** - Calculates revenue of invoices paid within date range (inclusive)
- **Financial year folder organisation** - Auto-creates folder path in destination to categorise invoices by financial year


## Requirements
- Python 3.x
- pip install reportlab tabulate

## Setup
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

**remove-invoice**

```
python invoice_cli.py remove-invoice --invoice-id 1
```

**show-all-invoices**

```
python invoice_cli.py show-all-invoices
```

**show-unpaid-invoices**

```
python invoice_cli.py show-unpaid-invoices
```

**show-invoice-items**

```
python invoice_cli.py show-invoice-items --invoice-id 1
```

**mark-paid**

```
python invoice_cli.py mark-paid --invoice-code 001JS
```

**calculate-revenue**

```
python invoice_cli.py calculate-revenue --from-date 2025-07-01 --to-date 2026-06-30
```




## File structure
**invoice_cli.py** - primary python file holding cli commands. Run this file to use the tool.
**database_functions.py** - stores all functions where direct interaction with the SQLite database is required
**pdf_generator.py** - holds function required to generate pdfs
**config.py** - stores business details for invoices. 
