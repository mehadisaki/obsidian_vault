Need to install Tesseract, is an open source [text recognition (OCR)](https://en.wikipedia.org/wiki/Optical_character_recognition) Engine,

Packages for over 130 languages and over 35 scripts

[Various types of training data](https://tesseract-ocr.github.io/tessdoc/Data-Files) can be found on [GitHub](https://github.com/tesseract-ocr/.md). Unpack and copy the .traineddata file into a ‘tessdata’ directory. The exact directory will depend both on the type of training data, and your Linux distribution. Possibilities are 

``` bash
/usr/share/tesseract-ocr/tessdata` 
or
- `/usr/share/tessdata` 
 or
-`/usr/share/tesseract-ocr/4.00/tessdata`.
```

For McOS You can install Tesseract using either [MacPorts](https://www.macports.org/) or [Homebrew](http://brew.sh/).

1. Install homebrew 
    ``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
	 ```
2.  if come # Error: Fetching /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core failed! #30917

4. 
To install Tesseract run this command:

```bash
brew install tesseract
```

5. 
The tesseract directory can then be found using 
```bash
brew info tesseract
```
e.g. `/usr/local/Cellar/tesseract/3.05.02/share/tessdata/`.

6. Use pytesseract.pytesseract.tesseract_cmd to add tessdata directory 
   to find the executable link run in terminal
```bash
which tesseract
    ``` 
 use the link in bellow python code
```python
pytesseract.pytesseract.tesseract_cmd = (r'  ')
```

7. [Errno 13] Permission denied: '/opt/homebrew/Cellar/tesseract/5.3.0_1/share/tessdata/'
 to find the executable link run in terminal

setup
```python

#esseract path

pytesseract.pytesseract.tesseract_cmd = (r'/opt/homebrew/bin/tesseract')
```

 
  '/opt/homebrew/bin/tesseract'

