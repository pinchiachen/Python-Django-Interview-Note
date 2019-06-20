# Python Django Interview Note

Prepare interview for Python and Django

## Python

### What is Python?

- Python 是一種解釋型語言，與 C 語言和 C 的衍生語言不同，Python 程式碼在運行之前不需要編譯。其他解釋型語言還包括 PHP 和 Ruby。

- Python 是動態類型語言，也就是在宣告變數時，不需要說明變數的類型。

- Python 非常適合物件導向 (OOP)，因為它支持通過組合 (composition) 與繼承 (inheritance) 的方式定義類別 (class)。 Python 中也沒有存取規格符 (access specifier，類似 C++ 中的 public 和 private)。

- 在 Python 中，函數是第一類對象 (first-class objects)。這指的是它們可以被指定給變數，函數既能返回函數類型，也可以接受函數作為輸入。類別 (class) 也是第一類對象。

- Python 程式碼編寫快，但是運行速度通常比編譯語言慢。不過 Python 允許加入基於 C 語言編寫的擴展，因此能夠優化程式碼。 numpy 就是一個很好的例子，它的運行速度非常快，因其很多算術運算並非通過 Python 所實現。

- Python 用途非常廣泛——網絡應用、自動化、科學建模、大數據應用等等。它也常被用作膠水語言 (glue language)，幫助其他語言和組件改善運行狀況。

- [Ref](http://codingpy.com/article/essential-python-interview-questions/)

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


