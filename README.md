# Alfred Workflow OCR
Take a snapshot and recognize text

[![alfred-ocr.png](./alfred-ocr.png)](./alfred-ocr.png)

## Installation

1. [Install `tesseract` on your system](https://github.com/tesseract-ocr/tesseract/wiki#macos): `sudo port install tesseract` or `brew install tesseract --with-all-languages`
2. Download the [workflow](https://github.com/nicooprat/alfred-ocr/blob/master/OCR.alfredworkflow)
3. Double click to install it in Alfred

## Usage

Use the keywork `OCR`, take a screenshot, wait for the notification, paste the text.

[![Capture-d-e-cran-2018-11-09-a-10-06-07.png](https://i.postimg.cc/jdsggtDc/Capture-d-e-cran-2018-11-09-a-10-06-07.png)](https://postimg.cc/5jRSjcqQ)

## What's inside?

Three lines of code:

```bash
export PATH=/usr/local/bin/:$PATH

screencapture -i /tmp/ocr_snapshot.png

tesseract /tmp/ocr_snapshot.png stdout 2>&1
```

## Known issues

Taking a snapshot from a different monitor than your main one with a different resolution will make the script buggy. You'll get a warning like this `[ERROR: action.script] Warning. Invalid resolution 0 dpi. Using 70 instead.` which leads to poor results of text recognition. Ideas welcome on this one!

## Credits

Inspired by the work of https://github.com/oott123/alfred-clipboard-ocr
