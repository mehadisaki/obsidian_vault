
```
pip install PyMuPDF=1.16.14
```
 

 importing required modules
```python 
from PyPDF2 import PdfReader 
```
  
Creating a pdf reader object

```python 
reader = PdfReader('example.pdf')
  
# printing number of pages in pdf file
print(len(reader.pages))
  
# getting a specific page from the pdf file
page = reader.pages[0]
  
# extracting text from page
text = page.extract_text()
print(text)
```


# By fitz

```Python 

import fitz
doc = fitz.open('sample.pdf')
text = ""
for page in doc:
   text+=page.get_text()
print(text)
```
