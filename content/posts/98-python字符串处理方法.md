---
title: "Python 常用字符串处理方法"
date: "2025-02-10T21:05:11-03:00"
tags: ["Python", "字符串"]
title_images: ["", "",]
ending_images: ["", "", "",]
author: "via"
draft: false
---

# Python 字符串处理

## 1. 使用字符串方法 `translate()` 替换字符串中的字符

`translate()` 方法可以根据指定的映射表替换字符串中的字符。

```python
translation_table = str.maketrans("aeiou", "12345")
s = "hello world"
new_s = s.translate(translation_table)
print(new_s)  # 输出: h2ll4 w4rld
```

## 2. 使用字符串方法 `swapcase()` 交换字符串中的大小写

`swapcase()` 方法可以交换字符串中的大小写。

```python
s = "Hello, World!"
print(s.swapcase())  # 输出: hELLO, wORLD!
```

## 3. 使用字符串方法 `zfill()` 在数字字符串前面填充零

`zfill()` 方法可以在数字字符串的左侧填充零，使其达到指定的宽度。

```python
number = "42"
padded_number = number.zfill(5)
print(padded_number)  # 输出: 00042
```

## 4. 使用字符串方法 `partition()` 和 `rpartition()` 分割字符串

`partition()` 方法可以将字符串按照指定的分隔符分割为三部分，返回一个包含分割结果的元组；`rpartition()` 则是从右边开始分割。

```python
s = "hello world python"
parts = s.partition(" ")
print(parts)  # 输出: ('hello', ' ', 'world python')
parts = s.rpartition(" ")
print(parts)  # 输出: ('hello world', ' ', 'python')
```

## 5. 使用字符串方法 `splitlines()` 按行拆分字符串

`splitlines()` 方法可以将字符串按行拆分，并返回一个包含每行内容的列表。

```python
text = "Hello\nWorld\nPython"
lines = text.splitlines()
print(lines)  # 输出: ['Hello', 'World', 'Python']
```

## 6. 使用字符串方法 `center()`、`ljust()` 和 `rjust()` 对齐字符串

这些方法可以让字符串在指定的宽度内居中、左对齐或右对齐。

```python
s = "hello"
print(s.center(10, '*'))  # 输出: **hello***
print(s.ljust(10, '-'))  # 输出: hello-----
print(s.rjust(10, '='))  # 输出: =====hello
```

## 7. 使用字符串方法 `capitalize()` 和 `title()` 将字符串首字母大写或每个单词的首字母大写

这两个方法可以帮助我们规范化字符串的格式。

```python
s = "hello world"
print(s.capitalize())  # 输出: Hello world
print(s.title())  # 输出: Hello World
```

## 8. 使用字符串方法 `lower()` 和 `upper()` 将字符串转换为小写或大写

这两个方法可以方便地将字符串转换为小写或大写形式。

```python
s = "Hello, World!"
print(s.lower())  # 输出: hello, world!
print(s.upper())  # 输出: HELLO, WORLD!
```

## 9. 使用字符串方法 `isalpha()`、`isdigit()` 和 `isalnum()` 判断字符串的类型

这些方法可以帮助我们判断字符串是否只包含字母、数字或字母和数字的组合。

```python
s1 = "hello"
s2 = "123"
s3 = "hello123"
s4 = "hello 123"

print(s1.isalpha())  # 输出: True
print(s2.isdigit())  # 输出: True
print(s3.isalnum())  # 输出: True
print(s4.isalnum())  # 输出: False
```

## 10. 使用字符串方法 `startswith()` 和 `endswith()` 判断字符串是否以指定的前缀或后缀开始或结束

这两个方法可以帮助我们快速判断字符串是否以某个前缀或后缀开始或结束。

```python
filename = "example.txt"
print(filename.startswith("ex"))  # 输出: True
print(filename.endswith(".txt"))  # 输出: True
```

## 11. 使用正则表达式进行复杂的字符串匹配和替换

当处理复杂的字符串匹配和替换时，可以使用 Python 的 `re` 模块来操作正则表达式。

```python
import re

s = "hello 123 world 456"
numbers = re.findall(r'\d+', s)
print(numbers)  # 输出: ['123', '456']

new_s = re.sub(r'\d+', '###', s)
print(new_s)  # 输出: hello ### world ###
```

## 12. 使用字符串方法 `count()` 统计子串出现的次数

`count()` 方法可以统计子串在字符串中出现的次数。

```python
s = "hello hello world"
print(s.count("hello"))  # 输出: 2
```

## 13. 使用字符串方法 `find()` 或 `index()` 查找子串的位置

`find()` 方法可以返回子串在字符串中第一次出现的位置，如果未找到则返回 `-1`；而 `index()` 方法也是查找子串的位置，但是如果未找到会抛出异常。

```python
s = "Hello, World!"
print(s.find("World"))  # 输出: 7
print(s.find("Python"))  # 输出: -1

print(s.index("World"))  # 输出: 7
# print(s.index("Python"))  # 会抛出 ValueError 异常
```
