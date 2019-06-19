# Python Django Interview Note

Prepare interview for Python and Django

## Python

### Zen of Python 

- [Python 台灣使用者群組中英翻譯版](http://wiki.python.org.tw/The%20Zen%20Of%20Python)

### PEP8

- [PEP8 Python 編碼規範手冊](https://cflin.com/wordpress/603/pep8-python%E7%B7%A8%E7%A2%BC%E8%A6%8F%E7%AF%84%E6%89%8B%E5%86%8A)

### PyLint

- 以 PEP8 為依據的 Python 代碼風格檢查工具。

### 可變 (Mutable) vs 不可變 (Immutable)

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

### ```foo_``` vs ```_foo``` vs ```__foo``` vs ```__foo__```

- [Python，你到底是在__底線__什麼啦！](https://aji.tw/python%E4%BD%A0%E5%88%B0%E5%BA%95%E6%98%AF%E5%9C%A8__%E5%BA%95%E7%B7%9A__%E4%BB%80%E9%BA%BC%E5%95%A6/)

### ```if __name__ == '__main__'```

- ```__name__ == '__main__'```：假如你叫小明.py，在朋友眼中，你是小明 ```__name__ == '小明'```；在你自己眼中，你是你自己 ```__name__ == '__main__'```。

- ```if __name__ == '__main__'``` 的意思是：當 .py 文件被直接運行時，```if __name__ == '__main__'``` 之下的程式碼將被運行；當 .py 文件以模組形式被導入時，```if __name__ == '__main__'``` 之下的程式碼不被運行。

- [See More](https://blog.csdn.net/yjk13703623757/article/details/77918633)

- [```if __name__ == '__main__' ``` 實例](https://blog.castman.net/%E6%95%99%E5%AD%B8/2018/01/27/python-name-main.html)


