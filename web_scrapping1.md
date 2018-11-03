

```python
import urllib
from bs4 import BeautifulSoup
```


```python
# Specify the url
quote_page = 'https://www.bloomberg.com/quote/SPX:IND'
```


```python
# query the website and return the html to the variable ‘page’
page = urllib.urlopen(quote_page)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-3-43f18998e49f> in <module>()
          1 # query the website and return the html to the variable ‘page’
    ----> 2 page = urllib.urlopen(quote_page)
    

    AttributeError: module 'urllib' has no attribute 'urlopen'



```python
from urllib import request
```


```python
page = urllib.request.urlopen(quote_page)
```


```python
# parse the html using beautiful soup and store in variable `soup`
soup = BeautifulSoup(page.read(), 'html.parser')
```


```python
# Take out the <div> of name and get its value
name_box = soup.find('h1', attrs={'class':'companyName__99a4824b'})
```


```python
name_box.text
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-37-266662a7f7ba> in <module>()
    ----> 1 name_box.text
    

    AttributeError: 'NoneType' object has no attribute 'text'



```python
print(name_box.text)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-24-1aad3ac69fa7> in <module>()
    ----> 1 print(name_box.text)
    

    AttributeError: 'NoneType' object has no attribute 'text'



```python
name = name_box.text.strip() # strip() is used to remove starting and trailing
print(name)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-12-d366de9b9379> in <module>()
    ----> 1 name = name_box.text.strip() # strip() is used to remove starting and trailing
          2 print(name)
    

    AttributeError: 'NoneType' object has no attribute 'text'



```python
from bs4 import BeautifulSoup
import urllib
from urllib import request
url="https://www.seedrs.com/tanorganic"
page = urllib.request.urlopen(url)
soup = BeautifulSoup(page.read(), "html.parser")
target = soup.find("dl", class_="investment_sought")
print(target.text)

```

    
    
    Investment
    
    sought:
    
    £70,004
    
    


```python
from bs4 import BeautifulSoup
import urllib
from urllib import request
url="https://www.bloomberg.com/quote/SPX:IND"
page = urllib.request.urlopen(url)
soup = BeautifulSoup(page.read(), "html.parser")
target = soup.find("dl", class_="companyName__99a4824b")
print(target.text)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-41-f8af7a0ad816> in <module>()
          6 soup = BeautifulSoup(page.read(), "html.parser")
          7 target = soup.find("dl", class_="companyName__99a4824b")
    ----> 8 print(target.text)
    

    AttributeError: 'NoneType' object has no attribute 'text'

