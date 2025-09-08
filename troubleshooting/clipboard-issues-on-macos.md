# Clipboard Issues on macOS

**If you notice missing special characters or the clipboard is empty after copying data on macOS:**

#### Why does this happen?

* When exporting to the clipboard on macOS, XLPrompt removes special characters by design. This is to prevent errors with the macOS clipboard, which does not handle these characters well.
* If you copy a very large range, the clipboard may be empty. This is a limitation of macOS.

#### What to do:

* **Use “Write to File”**:\
  Switch the output mode to **File** to save your data as a JSON file instead of copying to clipboard. This keeps all characters and works with large datasets.
* _Note:_ On macOS, “Write to File” is available in the free version.
