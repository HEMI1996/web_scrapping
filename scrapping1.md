

```python
from bs4 import BeautifulSoup
import requests
```


```python
url = requests.get('http://quotes.toscrape.com/')
```


```python
print(url)
```

    <Response [200]>
    


```python
print(url.text)
```

    <!DOCTYPE html>
    <html lang="en">
    <head>
    	<meta charset="UTF-8">
    	<title>Quotes to Scrape</title>
        <link rel="stylesheet" href="/static/bootstrap.min.css">
        <link rel="stylesheet" href="/static/main.css">
    </head>
    <body>
        <div class="container">
            <div class="row header-box">
                <div class="col-md-8">
                    <h1>
                        <a href="/" style="text-decoration: none">Quotes to Scrape</a>
                    </h1>
                </div>
                <div class="col-md-4">
                    <p>
                    
                        <a href="/login">Login</a>
                    
                    </p>
                </div>
            </div>
        
    
    <div class="row">
        <div class="col-md-8">
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”</span>
            <span>by <small class="author" itemprop="author">Albert Einstein</small>
            <a href="/author/Albert-Einstein">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="change,deep-thoughts,thinking,world" /    > 
                
                <a class="tag" href="/tag/change/page/1/">change</a>
                
                <a class="tag" href="/tag/deep-thoughts/page/1/">deep-thoughts</a>
                
                <a class="tag" href="/tag/thinking/page/1/">thinking</a>
                
                <a class="tag" href="/tag/world/page/1/">world</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“It is our choices, Harry, that show what we truly are, far more than our abilities.”</span>
            <span>by <small class="author" itemprop="author">J.K. Rowling</small>
            <a href="/author/J-K-Rowling">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="abilities,choices" /    > 
                
                <a class="tag" href="/tag/abilities/page/1/">abilities</a>
                
                <a class="tag" href="/tag/choices/page/1/">choices</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“There are only two ways to live your life. One is as though nothing is a miracle. The other is as though everything is a miracle.”</span>
            <span>by <small class="author" itemprop="author">Albert Einstein</small>
            <a href="/author/Albert-Einstein">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="inspirational,life,live,miracle,miracles" /    > 
                
                <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
                
                <a class="tag" href="/tag/life/page/1/">life</a>
                
                <a class="tag" href="/tag/live/page/1/">live</a>
                
                <a class="tag" href="/tag/miracle/page/1/">miracle</a>
                
                <a class="tag" href="/tag/miracles/page/1/">miracles</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid.”</span>
            <span>by <small class="author" itemprop="author">Jane Austen</small>
            <a href="/author/Jane-Austen">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="aliteracy,books,classic,humor" /    > 
                
                <a class="tag" href="/tag/aliteracy/page/1/">aliteracy</a>
                
                <a class="tag" href="/tag/books/page/1/">books</a>
                
                <a class="tag" href="/tag/classic/page/1/">classic</a>
                
                <a class="tag" href="/tag/humor/page/1/">humor</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“Imperfection is beauty, madness is genius and it&#39;s better to be absolutely ridiculous than absolutely boring.”</span>
            <span>by <small class="author" itemprop="author">Marilyn Monroe</small>
            <a href="/author/Marilyn-Monroe">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="be-yourself,inspirational" /    > 
                
                <a class="tag" href="/tag/be-yourself/page/1/">be-yourself</a>
                
                <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“Try not to become a man of success. Rather become a man of value.”</span>
            <span>by <small class="author" itemprop="author">Albert Einstein</small>
            <a href="/author/Albert-Einstein">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="adulthood,success,value" /    > 
                
                <a class="tag" href="/tag/adulthood/page/1/">adulthood</a>
                
                <a class="tag" href="/tag/success/page/1/">success</a>
                
                <a class="tag" href="/tag/value/page/1/">value</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“It is better to be hated for what you are than to be loved for what you are not.”</span>
            <span>by <small class="author" itemprop="author">André Gide</small>
            <a href="/author/Andre-Gide">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="life,love" /    > 
                
                <a class="tag" href="/tag/life/page/1/">life</a>
                
                <a class="tag" href="/tag/love/page/1/">love</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“I have not failed. I&#39;ve just found 10,000 ways that won&#39;t work.”</span>
            <span>by <small class="author" itemprop="author">Thomas A. Edison</small>
            <a href="/author/Thomas-A-Edison">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="edison,failure,inspirational,paraphrased" /    > 
                
                <a class="tag" href="/tag/edison/page/1/">edison</a>
                
                <a class="tag" href="/tag/failure/page/1/">failure</a>
                
                <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
                
                <a class="tag" href="/tag/paraphrased/page/1/">paraphrased</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“A woman is like a tea bag; you never know how strong it is until it&#39;s in hot water.”</span>
            <span>by <small class="author" itemprop="author">Eleanor Roosevelt</small>
            <a href="/author/Eleanor-Roosevelt">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="misattributed-eleanor-roosevelt" /    > 
                
                <a class="tag" href="/tag/misattributed-eleanor-roosevelt/page/1/">misattributed-eleanor-roosevelt</a>
                
            </div>
        </div>
    
        <div class="quote" itemscope itemtype="http://schema.org/CreativeWork">
            <span class="text" itemprop="text">“A day without sunshine is like, you know, night.”</span>
            <span>by <small class="author" itemprop="author">Steve Martin</small>
            <a href="/author/Steve-Martin">(about)</a>
            </span>
            <div class="tags">
                Tags:
                <meta class="keywords" itemprop="keywords" content="humor,obvious,simile" /    > 
                
                <a class="tag" href="/tag/humor/page/1/">humor</a>
                
                <a class="tag" href="/tag/obvious/page/1/">obvious</a>
                
                <a class="tag" href="/tag/simile/page/1/">simile</a>
                
            </div>
        </div>
    
        <nav>
            <ul class="pager">
                
                
                <li class="next">
                    <a href="/page/2/">Next <span aria-hidden="true">&rarr;</span></a>
                </li>
                
            </ul>
        </nav>
        </div>
        <div class="col-md-4 tags-box">
            
                <h2>Top Ten tags</h2>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 28px" href="/tag/love/">love</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 26px" href="/tag/inspirational/">inspirational</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 26px" href="/tag/life/">life</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 24px" href="/tag/humor/">humor</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 22px" href="/tag/books/">books</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 14px" href="/tag/reading/">reading</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 10px" href="/tag/friendship/">friendship</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 8px" href="/tag/friends/">friends</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 8px" href="/tag/truth/">truth</a>
                </span>
                
                <span class="tag-item">
                <a class="tag" style="font-size: 6px" href="/tag/simile/">simile</a>
                </span>
                
            
        </div>
    </div>
    
        </div>
        <footer class="footer">
            <div class="container">
                <p class="text-muted">
                    Quotes by: <a href="https://www.goodreads.com/quotes">GoodReads.com</a>
                </p>
                <p class="copyright">
                    Made with <span class='sh-red'>❤</span> by <a href="https://scrapinghub.com">Scrapinghub</a>
                </p>
            </div>
        </footer>
    </body>
    </html>
    


```python
soup = BeautifulSoup(url.text, 'lxml')
```


```python
print(soup)
```

    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="utf-8"/>
    <title>Quotes to Scrape</title>
    <link href="/static/bootstrap.min.css" rel="stylesheet"/>
    <link href="/static/main.css" rel="stylesheet"/>
    </head>
    <body>
    <div class="container">
    <div class="row header-box">
    <div class="col-md-8">
    <h1>
    <a href="/" style="text-decoration: none">Quotes to Scrape</a>
    </h1>
    </div>
    <div class="col-md-4">
    <p>
    <a href="/login">Login</a>
    </p>
    </div>
    </div>
    <div class="row">
    <div class="col-md-8">
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”</span>
    <span>by <small class="author" itemprop="author">Albert Einstein</small>
    <a href="/author/Albert-Einstein">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="change,deep-thoughts,thinking,world" itemprop="keywords"/>
    <a class="tag" href="/tag/change/page/1/">change</a>
    <a class="tag" href="/tag/deep-thoughts/page/1/">deep-thoughts</a>
    <a class="tag" href="/tag/thinking/page/1/">thinking</a>
    <a class="tag" href="/tag/world/page/1/">world</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“It is our choices, Harry, that show what we truly are, far more than our abilities.”</span>
    <span>by <small class="author" itemprop="author">J.K. Rowling</small>
    <a href="/author/J-K-Rowling">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="abilities,choices" itemprop="keywords"/>
    <a class="tag" href="/tag/abilities/page/1/">abilities</a>
    <a class="tag" href="/tag/choices/page/1/">choices</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“There are only two ways to live your life. One is as though nothing is a miracle. The other is as though everything is a miracle.”</span>
    <span>by <small class="author" itemprop="author">Albert Einstein</small>
    <a href="/author/Albert-Einstein">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="inspirational,life,live,miracle,miracles" itemprop="keywords"/>
    <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
    <a class="tag" href="/tag/life/page/1/">life</a>
    <a class="tag" href="/tag/live/page/1/">live</a>
    <a class="tag" href="/tag/miracle/page/1/">miracle</a>
    <a class="tag" href="/tag/miracles/page/1/">miracles</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid.”</span>
    <span>by <small class="author" itemprop="author">Jane Austen</small>
    <a href="/author/Jane-Austen">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="aliteracy,books,classic,humor" itemprop="keywords"/>
    <a class="tag" href="/tag/aliteracy/page/1/">aliteracy</a>
    <a class="tag" href="/tag/books/page/1/">books</a>
    <a class="tag" href="/tag/classic/page/1/">classic</a>
    <a class="tag" href="/tag/humor/page/1/">humor</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“Imperfection is beauty, madness is genius and it's better to be absolutely ridiculous than absolutely boring.”</span>
    <span>by <small class="author" itemprop="author">Marilyn Monroe</small>
    <a href="/author/Marilyn-Monroe">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="be-yourself,inspirational" itemprop="keywords"/>
    <a class="tag" href="/tag/be-yourself/page/1/">be-yourself</a>
    <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“Try not to become a man of success. Rather become a man of value.”</span>
    <span>by <small class="author" itemprop="author">Albert Einstein</small>
    <a href="/author/Albert-Einstein">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="adulthood,success,value" itemprop="keywords"/>
    <a class="tag" href="/tag/adulthood/page/1/">adulthood</a>
    <a class="tag" href="/tag/success/page/1/">success</a>
    <a class="tag" href="/tag/value/page/1/">value</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“It is better to be hated for what you are than to be loved for what you are not.”</span>
    <span>by <small class="author" itemprop="author">André Gide</small>
    <a href="/author/Andre-Gide">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="life,love" itemprop="keywords"/>
    <a class="tag" href="/tag/life/page/1/">life</a>
    <a class="tag" href="/tag/love/page/1/">love</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“I have not failed. I've just found 10,000 ways that won't work.”</span>
    <span>by <small class="author" itemprop="author">Thomas A. Edison</small>
    <a href="/author/Thomas-A-Edison">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="edison,failure,inspirational,paraphrased" itemprop="keywords"/>
    <a class="tag" href="/tag/edison/page/1/">edison</a>
    <a class="tag" href="/tag/failure/page/1/">failure</a>
    <a class="tag" href="/tag/inspirational/page/1/">inspirational</a>
    <a class="tag" href="/tag/paraphrased/page/1/">paraphrased</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“A woman is like a tea bag; you never know how strong it is until it's in hot water.”</span>
    <span>by <small class="author" itemprop="author">Eleanor Roosevelt</small>
    <a href="/author/Eleanor-Roosevelt">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="misattributed-eleanor-roosevelt" itemprop="keywords"/>
    <a class="tag" href="/tag/misattributed-eleanor-roosevelt/page/1/">misattributed-eleanor-roosevelt</a>
    </div>
    </div>
    <div class="quote" itemscope="" itemtype="http://schema.org/CreativeWork">
    <span class="text" itemprop="text">“A day without sunshine is like, you know, night.”</span>
    <span>by <small class="author" itemprop="author">Steve Martin</small>
    <a href="/author/Steve-Martin">(about)</a>
    </span>
    <div class="tags">
                Tags:
                <meta class="keywords" content="humor,obvious,simile" itemprop="keywords"/>
    <a class="tag" href="/tag/humor/page/1/">humor</a>
    <a class="tag" href="/tag/obvious/page/1/">obvious</a>
    <a class="tag" href="/tag/simile/page/1/">simile</a>
    </div>
    </div>
    <nav>
    <ul class="pager">
    <li class="next">
    <a href="/page/2/">Next <span aria-hidden="true">→</span></a>
    </li>
    </ul>
    </nav>
    </div>
    <div class="col-md-4 tags-box">
    <h2>Top Ten tags</h2>
    <span class="tag-item">
    <a class="tag" href="/tag/love/" style="font-size: 28px">love</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/inspirational/" style="font-size: 26px">inspirational</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/life/" style="font-size: 26px">life</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/humor/" style="font-size: 24px">humor</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/books/" style="font-size: 22px">books</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/reading/" style="font-size: 14px">reading</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/friendship/" style="font-size: 10px">friendship</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/friends/" style="font-size: 8px">friends</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/truth/" style="font-size: 8px">truth</a>
    </span>
    <span class="tag-item">
    <a class="tag" href="/tag/simile/" style="font-size: 6px">simile</a>
    </span>
    </div>
    </div>
    </div>
    <footer class="footer">
    <div class="container">
    <p class="text-muted">
                    Quotes by: <a href="https://www.goodreads.com/quotes">GoodReads.com</a>
    </p>
    <p class="copyright">
                    Made with <span class="sh-red">❤</span> by <a href="https://scrapinghub.com">Scrapinghub</a>
    </p>
    </div>
    </footer>
    </body>
    </html>
    


```python
quote = soup.find('div', {'class' : 'quote'})
print(quote.text)
```

    
    “The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”
    by Albert Einstein
    (about)
    
    
                Tags:
                
    change
    deep-thoughts
    thinking
    world
    
    
    


```python
quote = soup.find('span', {'class' : 'text'})
print(quote)
```

    <span class="text" itemprop="text">“The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”</span>
    


```python
print(quote.text)
```

    “The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”
    


```python
quote = soup.find_all('div', {'class' : 'quote'})
```


```python
for q in quote:
    msg = q.find('span', {'class' : 'text'})
    print(msg.text)
```

    “The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”
    “It is our choices, Harry, that show what we truly are, far more than our abilities.”
    “There are only two ways to live your life. One is as though nothing is a miracle. The other is as though everything is a miracle.”
    “The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid.”
    “Imperfection is beauty, madness is genius and it's better to be absolutely ridiculous than absolutely boring.”
    “Try not to become a man of success. Rather become a man of value.”
    “It is better to be hated for what you are than to be loved for what you are not.”
    “I have not failed. I've just found 10,000 ways that won't work.”
    “A woman is like a tea bag; you never know how strong it is until it's in hot water.”
    “A day without sunshine is like, you know, night.”
    


```python
for q in quote:
    author = q.find('small')
    print(author.text)
```

    Albert Einstein
    J.K. Rowling
    Albert Einstein
    Jane Austen
    Marilyn Monroe
    Albert Einstein
    André Gide
    Thomas A. Edison
    Eleanor Roosevelt
    Steve Martin
    


```python
for q in quote:
    author = q.find('small', {'class' : 'author'})
    print(author.text)
```

    Albert Einstein
    J.K. Rowling
    Albert Einstein
    Jane Austen
    Marilyn Monroe
    Albert Einstein
    André Gide
    Thomas A. Edison
    Eleanor Roosevelt
    Steve Martin
    


```python
for q in quote:
    msg = q.find('span') # if we have only one class it's an optional to write class 
    print(msg.text)
```

    “The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”
    “It is our choices, Harry, that show what we truly are, far more than our abilities.”
    “There are only two ways to live your life. One is as though nothing is a miracle. The other is as though everything is a miracle.”
    “The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid.”
    “Imperfection is beauty, madness is genius and it's better to be absolutely ridiculous than absolutely boring.”
    “Try not to become a man of success. Rather become a man of value.”
    “It is better to be hated for what you are than to be loved for what you are not.”
    “I have not failed. I've just found 10,000 ways that won't work.”
    “A woman is like a tea bag; you never know how strong it is until it's in hot water.”
    “A day without sunshine is like, you know, night.”
    

# Practice


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = requests.get('https://www.seedrs.com/tanorganic')
```


    ---------------------------------------------------------------------------

    TimeoutError                              Traceback (most recent call last)

    ~\Anaconda3\lib\site-packages\urllib3\connection.py in _new_conn(self)
        140             conn = connection.create_connection(
    --> 141                 (self.host, self.port), self.timeout, **extra_kw)
        142 
    

    ~\Anaconda3\lib\site-packages\urllib3\util\connection.py in create_connection(address, timeout, source_address, socket_options)
         82     if err is not None:
    ---> 83         raise err
         84 
    

    ~\Anaconda3\lib\site-packages\urllib3\util\connection.py in create_connection(address, timeout, source_address, socket_options)
         72                 sock.bind(source_address)
    ---> 73             sock.connect(sa)
         74             return sock
    

    TimeoutError: [WinError 10060] A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond

    
    During handling of the above exception, another exception occurred:
    

    NewConnectionError                        Traceback (most recent call last)

    ~\Anaconda3\lib\site-packages\urllib3\connectionpool.py in urlopen(self, method, url, body, headers, retries, redirect, assert_same_host, timeout, pool_timeout, release_conn, chunked, body_pos, **response_kw)
        594             if is_new_proxy_conn:
    --> 595                 self._prepare_proxy(conn)
        596 
    

    ~\Anaconda3\lib\site-packages\urllib3\connectionpool.py in _prepare_proxy(self, conn)
        815 
    --> 816         conn.connect()
        817 
    

    ~\Anaconda3\lib\site-packages\urllib3\connection.py in connect(self)
        283         # Add certificate verification
    --> 284         conn = self._new_conn()
        285 
    

    ~\Anaconda3\lib\site-packages\urllib3\connection.py in _new_conn(self)
        149             raise NewConnectionError(
    --> 150                 self, "Failed to establish a new connection: %s" % e)
        151 
    

    NewConnectionError: <urllib3.connection.VerifiedHTTPSConnection object at 0x0000025254064D30>: Failed to establish a new connection: [WinError 10060] A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond

    
    During handling of the above exception, another exception occurred:
    

    MaxRetryError                             Traceback (most recent call last)

    ~\Anaconda3\lib\site-packages\requests\adapters.py in send(self, request, stream, timeout, verify, cert, proxies)
        439                     retries=self.max_retries,
    --> 440                     timeout=timeout
        441                 )
    

    ~\Anaconda3\lib\site-packages\urllib3\connectionpool.py in urlopen(self, method, url, body, headers, retries, redirect, assert_same_host, timeout, pool_timeout, release_conn, chunked, body_pos, **response_kw)
        638             retries = retries.increment(method, url, error=e, _pool=self,
    --> 639                                         _stacktrace=sys.exc_info()[2])
        640             retries.sleep()
    

    ~\Anaconda3\lib\site-packages\urllib3\util\retry.py in increment(self, method, url, response, error, _pool, _stacktrace)
        387         if new_retry.is_exhausted():
    --> 388             raise MaxRetryError(_pool, url, error or ResponseError(cause))
        389 
    

    MaxRetryError: HTTPSConnectionPool(host='www.seedrs.com', port=443): Max retries exceeded with url: /tanorganic (Caused by ProxyError('Cannot connect to proxy.', NewConnectionError('<urllib3.connection.VerifiedHTTPSConnection object at 0x0000025254064D30>: Failed to establish a new connection: [WinError 10060] A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond',)))

    
    During handling of the above exception, another exception occurred:
    

    ProxyError                                Traceback (most recent call last)

    <ipython-input-2-c60aed2b92d7> in <module>()
    ----> 1 url = requests.get('https://www.seedrs.com/tanorganic')
    

    ~\Anaconda3\lib\site-packages\requests\api.py in get(url, params, **kwargs)
         70 
         71     kwargs.setdefault('allow_redirects', True)
    ---> 72     return request('get', url, params=params, **kwargs)
         73 
         74 
    

    ~\Anaconda3\lib\site-packages\requests\api.py in request(method, url, **kwargs)
         56     # cases, and look like a memory leak in others.
         57     with sessions.Session() as session:
    ---> 58         return session.request(method=method, url=url, **kwargs)
         59 
         60 
    

    ~\Anaconda3\lib\site-packages\requests\sessions.py in request(self, method, url, params, data, headers, cookies, files, auth, timeout, allow_redirects, proxies, hooks, stream, verify, cert, json)
        506         }
        507         send_kwargs.update(settings)
    --> 508         resp = self.send(prep, **send_kwargs)
        509 
        510         return resp
    

    ~\Anaconda3\lib\site-packages\requests\sessions.py in send(self, request, **kwargs)
        616 
        617         # Send the request
    --> 618         r = adapter.send(request, **kwargs)
        619 
        620         # Total elapsed time of the request (approximately)
    

    ~\Anaconda3\lib\site-packages\requests\adapters.py in send(self, request, stream, timeout, verify, cert, proxies)
        500 
        501             if isinstance(e.reason, _ProxyError):
    --> 502                 raise ProxyError(e, request=request)
        503 
        504             if isinstance(e.reason, _SSLError):
    

    ProxyError: HTTPSConnectionPool(host='www.seedrs.com', port=443): Max retries exceeded with url: /tanorganic (Caused by ProxyError('Cannot connect to proxy.', NewConnectionError('<urllib3.connection.VerifiedHTTPSConnection object at 0x0000025254064D30>: Failed to establish a new connection: [WinError 10060] A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond',)))

