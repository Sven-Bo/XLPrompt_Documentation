---
description: >-
  XLPrompt gives you control over how your Excel data is converted and exported.
  Here’s a quick overview of the main settings.
---

# How to configure XLPrompt settings

#### 1. JSON Format

* **Format Options:**
  * **Object Format**: Exports each row as an object (default).
  * **Array Format**: Exports all data as a raw array.
  * **Table Format** _(PRO)_: Exports headers and data separately for easier table import.
  * **Cell Format** _(PRO)_: Exports each cell with its address as key-value pairs.
* **Extra Options:**
  * Add workbook name, worksheet name, or range address to the output.
  * Add row and column count.
  * Remove blank cells.
  * Choose whether to use the first row as headers.

**Example:**

| Month | Sales |
| ----- | ----- |
| Jan   | 100   |
| Feb   |       |
| Mar   | 110   |

**Object Format Output:**

```json
{
  "data": [
    {"Month": "Jan", "Sales": 100},
    {"Month": "Feb", "Sales": null},
    {"Month": "Mar", "Sales": 110}
  ]
}
```

**Array Format Output:**

```json
{
  "data": [
    ["Month", "Sales"],
    ["Jan", 100],
    ["Feb", null],
    ["Mar", 110]
  ]
}
```

**Table Format Output (PRO):**

```json
{
  "headers": ["Month", "Sales"],
  "data": [
    ["Jan", 100],
    ["Feb", null],
    ["Mar", 110]
  ]
}
```

**Cell Format Output (PRO):**

```json
{
  "data": {
    "A1": "Month", "B1": "Sales",
    "A2": "Jan",   "B2": 100,
    "A3": "Feb",   "B3": null,
    "A4": "Mar",   "B4": 110
  }
}
```

***

#### 2. Context

* **Custom AI Prompt**: Add a prompt for the AI (PRO).
* **Context**: Add workbook, sheet, or range info using tokens.
  * Example:\
    `This data comes from Excel workbook: '{WORKBOOK_NAME}', sheet: '{SHEET_NAME}', range: '{RANGE_ADDRESS}'`

***

#### 3. Output

* **Output Mode**:
  * _Clipboard_: Copies JSON to clipboard.
  * _File_: Saves JSON to a file (PRO on Windows, free on Mac due to clipboard limits).
* **Note for Mac users**:
  * Special characters may be lost when copying to clipboard.
  * Large selections may result in an empty clipboard. Use “File” mode if you hit this limit.
* **Other Options**:
  * Pretty print output for readability.
  * Show notifications after export.

***

#### 4. Advanced Settings

* **Connection Mode**: Leave as default unless you need to troubleshoot.
* **Timeout**: Adjust only if you have connection delays.

***

#### Tips

* Save changes with **Save & Close**.
* **Reset to Defaults** if you need to start over.
* Locked features are marked with an asterisk (\*) if you’re using the free version.
