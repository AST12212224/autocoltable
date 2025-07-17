# autocoltable – Automatic Multi-Column Table Formatting for LaTeX

## Overview

**autocoltable** is an open-source LaTeX package under development to make large tables more readable and manageable in academic documents, presentations, and reports.

When tables contain many rows, it’s often desirable to display them in **multiple vertical columns**, each with a **fixed maximum number of rows**. Standard LaTeX provides the `multicols` environment (for balancing text), but it does **not** natively support splitting a table’s rows into multiple tabular environments that automatically “wrap” after a certain number of rows.

This package aims to provide a **user-friendly interface** for auto-splitting tables into multi-column layouts—with minimal manual work.

---

## Problem Statement

### The Issue

* **LaTeX lacks built-in logic for auto-wrapping table rows into multiple columns.**
* `multicols` only balances paragraphs/text, not table rows.
* Currently, users must manually split their tables and copy-paste into several `tabular` environments, using `\columnbreak` between each—tedious and error-prone, especially for large or changing data.

### Example Scenario

You have a table of 100 items (e.g., parameter values and results), and you want to show it in 4 columns, with each column having no more than 25 rows.
**Standard LaTeX cannot do this automatically.**
If your data changes, you must manually adjust the columns every time.

---

## Solution: autocoltable

The **goal** of this package is to let users specify:

* The number of columns (e.g., 4)
* The maximum number of rows per column (e.g., 25)
* The table data (as a LaTeX list, CSV, or similar)

…and let the package do the rest: split the table into multiple tabulars, insert column breaks, and render a professional multi-column table.

---

## Planned Features

* **Simple, clear syntax**:
  Example:

  ```latex
  \begin{autocoltable}[columns=4, maxrows=25]
    % Data as comma-separated values or key-value pairs
    1, value1
    2, value2
    ...
    100, value100
  \end{autocoltable}
  ```
* **CSV file import** or inline data support
* **Automatic splitting** into N columns, each with max M rows
* **Configurable column headers and formatting**
* **Full support for booktabs, tabularx, or other environments**
* **Good error handling** for missing data or uneven splits

---

## Why is this needed?

* **Reduces manual table splitting**—no more tedious copying/pasting or worrying about row counts when your data updates.
* **Saves time** for scientific and academic authors.
* **Keeps documents clean and maintainable**.
* **Supports reproducibility**: changes in data only require a recompile, not a complete reformat.

---

## Project Status

* **Currently in planning/development phase**.
* **Feedback, feature suggestions, and contributions are welcome!**
* Interested in collaborating? Open an issue or pull request.

---

## How to Get Involved

* **Fork or star** the repository
* Open an **issue** to suggest features or report bugs
* Submit a **pull request** if you’d like to contribute code
* Contact the author for collaboration or testing

---

## Long-term Vision

This package aims to become the “go-to” tool for auto-wrapping LaTeX tables across columns, making large datasets easier to read and papers easier to format.

**Join us to make LaTeX tables easier for everyone!**

---

*Inspired by a common pain point for researchers, authors, and anyone with big tables in LaTeX.*

