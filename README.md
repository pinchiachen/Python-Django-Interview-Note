# Python Django Interview Note

Prepare interview for Python and Django.

## Python

### What is Python?

- Python 是一種直譯語言，與 C 語言和 C 的衍生語言不同，Python 程式碼在運行之前不需要編譯。其他直譯語言還包括 JavaScript、PHP 和 Ruby。

- Python 是動態類型語言，也就是在宣告變數時，不需要說明變數的類型。

- Python 非常適合物件導向 (OOP)，因為它支持通過組合 (composition) 與繼承 (inheritance) 的方式定義類別 (class)。 Python 中也沒有存取規格符 (access specifier，類似 C++ 中的 public 和 private)。

- 在 Python 中，函數是第一類對象 (first-class objects)。這指的是它們可以被指定給變數，函數既能返回函數類型，也可以接受函數作為輸入。類別 (class) 也是第一類對象。

- Python 程式碼編寫快，但是運行速度通常比編譯語言慢。不過 Python 允許加入基於 C 語言編寫的擴展，因此能夠優化程式碼。 numpy 就是一個很好的例子，它的運行速度非常快，因其很多算術運算並非通過 Python 所實現。

- [Ref](http://codingpy.com/article/essential-python-interview-questions/)

### Zen of Python 

- [Ref](http://wiki.python.org.tw/The%20Zen%20Of%20Python)

### PEP8

- [Ref](https://cflin.com/wordpress/603/pep8-python%E7%B7%A8%E7%A2%BC%E8%A6%8F%E7%AF%84%E6%89%8B%E5%86%8A)

### PyLint

- 以 PEP8 為依據的 Python 代碼風格檢查工具。

### 可變 (Mutable) vs 不可變 (Immutable)

- [Ref](https://zhuanlan.zhihu.com/p/34395671)

- Mutable：list、set、dict 

- Immutable：int、float、bool、str、tuple、unicode、frozenset


### List vs Tuple

- Tuple 是不可修改的。

- Tuple 不可修改當中元素值。

- Tuple 不可增加元素，但可以將兩個 Tuple 相加。

- Tuple 不可刪除當中元素，但可以直接用 del 刪除整個 Tuple。

### OOP (Object Oriented Programming)

> 繼承 (Inheritance)

- 支援多重繼承，當子類別繼承 (inheritance) 超過一個來源的時候，會以寫在最左邊的父類別優先繼承。

> 封裝 (Encapsulation)

> 多型 (Polymorphism)

- 不支援以下用法
```Python
def calculator(a):
    do_something
        
def calculator(a, b):
    do_something
```

### `foo_` vs `_foo` vs `__foo` vs `__foo__`

- [Ref](https://aji.tw/python%E4%BD%A0%E5%88%B0%E5%BA%95%E6%98%AF%E5%9C%A8__%E5%BA%95%E7%B7%9A__%E4%BB%80%E9%BA%BC%E5%95%A6/)

### `if __name__ == '__main__'`

- `__name__ == '__main__'` ：假如你叫小明.py，在朋友眼中，你是小明 `__name__ == '小明'`；在你自己眼中，你是你自己 `__name__ == '__main__'`。

- `if __name__ == '__main__'` 的用法是：當 .py 文件被直接運行時，此時你是你自己 `__name__ == '__main__'`，所以 `if __name__ == '__main__'` 之下的程式碼將被運行；當 .py 文件以模組形式被導入時，此時你是小明 `__name__ == '小明'`，所以 `if __name__ == '__main__'` 之下的程式碼不被運行。

- [Ref](https://blog.csdn.net/yjk13703623757/article/details/77918633)

- [Example](https://blog.castman.net/%E6%95%99%E5%AD%B8/2018/01/27/python-name-main.html)

### `*args` and `**kwargs`

> `*args`

- 可變的位置參數 (Positional Arguments)，表示任何多個無名參數，在你不知道參數個數時使用，其本質為 Tuple，可以跟 `**kwargs` 同時使用，但 `*args` 必須保持在前。

> `**kwargs`

- 可變的關鍵字參數 (Keyword Argument)，表示任何多個 Key-Value 參數，其本質為 Dict。

### Copy

### Static Type vs Dynamic Type

### Pass by Value vs Pass by Reference

- 「Pass by value」意味著這個函數參數的 value 被 copy 進內存中的另一個位置，當在函數中訪問或修改這個變數時，只有這個 copy 複製品被操作了，而原始的 value 沒有被接觸到，如果想要函數傳回一個單值，使用「Pass by value」。

- 「Pass by reference」是指變數的儲存地址（一個內存位置的指針）被傳遞到函數中，如果想要函數傳回兩個以上單值，使用「Pass by reference」。

- Python 使用的不是以上兩者，Python 使用的是「Pass by object reference」。

### GIL (Global Interpreter Lock)

- [Ref](http://cenalulu.github.io/python/gil-in-python/)

### Coroutine

* * *

## Django

### What is Django?

### Django 生命週期

- 當使用者在瀏覽器中輸入 url 時，瀏覽器會生成請求頭和請求體發給伺服器端，請求頭和請求體中會包含瀏覽器的動作 (action)，這個動作通常為 get 或者post，體現在 url 之中。

- url 經過 Django 中的 wsgi，再經過 Django 的中間件，最後 url 到過路由映射表，在路由中一條一條進行匹配，一旦其中一條匹配成功就執行對應的視圖 (view) 函數，後面的路由就不再繼續匹配了。

- 視圖函數根據用戶端的請求查詢相應的數據，傳回給 Django，然後 Django 把用戶端想要的數據做為一個字符串傳回給用戶端。

- 用戶端瀏覽器接收到傳回的數據，經過渲染 (render) 後顯示給用戶。

### RESTful API

- [Ref](http://www.ruanyifeng.com/blog/2018/10/restful-api-best-practices.html)

### MTV

### Model - SQL vs NoSQL

### Template - Tags vs Filters

### View - FBV (function base views) vs CBV (class base views)

- 使用 fbv 模式，在url匹配成功之後會直接執行對應的視圖函數；使用 cbv 模式，在url匹配成功之後會找到視圖函數中對應的類別，然後這個類別回到請求頭中找到對應的 Request Method。

- 用戶發送 url 請求，Django 會依次遍歷路由映射表中的所有記錄，一旦路由映射表其中的一條匹配成功了，就執行視圖函數中對應的函數名，這是 fbv 的執行流程。

- 當伺服器端使用 cbv 模式的時候，用戶發給伺服器端的請求包含 url 和 method，這兩個訊息都是字符串類型。伺服器端通過路由映射表匹配成功後會自動去找 dispatch 方法，然後 Django 會通過 dispatch 反射的方式找到類別中對應的方法並執行。類別中的方法執行完畢之後，會把用戶端想要的數據傳回給 dispatch 方法，由 dispatch 方法把數據傳回至用戶端。

### Wsgi

- 描述 web server 如何與 web application 通訊的一種規範，WSGI 協議主要包括 server 和 application 兩部分
    
    - WSGI server 負責從客戶端接收請求，將 request 轉傳給 application，將 application 傳回的 response 傳回給客戶端。
    
    - WSGI application 接收由 server 轉傳的 request，處理請求，並將處理結果傳回給 server。

- Application 中可以包括多個棧式的中間件 (middlewares)，這些中間件需要同時實現 server 與 application，因此可以在 WSGI server與 WSGI applicatio 之間起調節作用：對 server 來說，中間件扮演 application，對 application 來說，中間件扮演 server。

### Nginx

### Apache

### Middleware

- 在 Django 中，中間件其實就是一個類別，在請求到來和結束後，Django 會根據自己的規則在合適的時機執行中間件中相應的方法。

- 在 Django 的 settings 模組中，有一個 MIDDLEWARE_CLASSES 變數，其中每一個元素就是一個中間件。

- 常見用法 
```Python
# 方法在請求到來的時候調用
process_request(self,request)

# 在本次將要執行的 View 函數被調用前調用本函數
process_view(self, request, callback, callback_args, callback_kwargs)

# 需使用 render() 方法才會執行 process_template_response
process_template_response(self,request,response)

# View 函數在拋出異常時該函數被調用，得到的 exception 參數是實際上拋出的異常實例。通過此方法可以進行很好的錯誤控制，提供友好的用戶界面。
process_exception(self, request, exception)

# 在執行完 View 函數準備將響應發到客戶端前被執行
process_response(self, request, response)
```

### QuerySet

- 從資料庫中查詢出來的結果一般是一個集合，這個集合叫做 QuerySet。

### ORM

### Request vs Response

- 當請求一個頁面時，Django 創建一個 HttpRequest 對象，該對象包含 request 的元數據，然後 Django 調用相應的 view 函數，HttpRequest 對象自動傳遞給該 view 函數作為第一個參數，每一個 view 負責傳回一個 HttpResponse 對象。

- requests 的元數據包括 path、get、put 等方法以及 cookies、user 等等。

### Aggregate vs Annotate

### Select_Related vs Prefetch_Related

### Celery

### Redis

### Session

### Cache

### Cookie

### Http vs Https

### Web Method

* * *

## DevOps

### Gitflow

### CI / CD

### Jenkins

### Unit Test

### TDD vs RDD

### Container vs Virtual Machine vs Virtualenv

### Supervisor

### Puppet

### AWS

### GCP (Google Cloud Platform)

### Cluster

### Master / Slave

### NoSQL - Sharding

### Firebase

### OAuth

### GraphQL

