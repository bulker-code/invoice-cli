# INVOICE CLI

A command line invoice management tool for sole traders. Manage clients, create and send professional PDF invoices, track payments, and calculate revenue of a given time period. 

## Features

Client management - Add and remove clients with automatic unique client ids to keep them distinct and separate. 
Line-item invoices - Line items with a date, quantity, and rate. 
PDF generation - Professionally formatted PDFs generated automatically when an invoice is added.
Invoice codes - Unique codes generated based on client name and number of invoices sent to them. 
Revenue filtering by date range - Calculates revenue of invoices paid within date range (inclusive).
Financial year folder organisation - Auto-creates folder path to categorise invoices by financial year. 

Requirements: Python 3.x, pip install reportlab tabulate

Setup: 
Clone the repo from github. 
Copy the config_example.py and rename it config.py, and fill in your business details. 

Usage: one block per command showing the actual command and what it does



File structure: what invoice_cli.py, database_functions.py, pdf_generator.py each do
