# Markdown 列表语法

可以将多个条目组织成有序或无序列表。

---

## 有序列表

要创建有序列表，请在每个列表项前添加数字并紧跟一个英文句点。  
<font color = lightblue>数字不必按数学顺序排列，但是列表应当以数字 1 起始。</font>

| Markdown 语法  |   HTML语法   | 预览效果  |
| :------------------- | :-------------- |:-------------- |
|`1. First item` <br> `2. Second item`<br>`3. Third item`<br>`4. Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item|
|`1. First item` <br> `1. Second item`<br>`1. Third item`<br>`1. Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item|
|`1. First item` <br> `8. Second item`<br>`3. Third item`<br>`5. Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item|
|`1. First item` <br> `2. Second item`<br>`3. Third item`<br>&nbsp;&nbsp;&nbsp;&nbsp;`1. Indented item`<br> `4. Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<ol>`<br>`<li>Indented item</li>`<br>`</ol>`<br>`</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|1. First item<br>2. Second item<br>3. Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>4. Fourth item|

---

## 有序列表最佳实践
CommonMark and a few other lightweight markup languages let you use a parenthesis (`)`) as a delimiter (e.g., `1) First item`), but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. For compatibility, use periods only.

| ✅ Do this     | ❌ Don't do this     |
| :------------- | :------------- |
| `1. First item`<br>`2. Second item`       | `1) First item`<br>`2) Second item`       |

---

## 无序列表
要创建无序列表，请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。

| Markdown 语法  |   HTML语法   | 预览效果  |
| :------------------- | :-------------- |:-------------- |
|`- First item` <br> `- Second item`<br>`- Third item`<br>`- Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`| <li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li> |
|`* First item` <br> `* Second item`<br>`* Third item`<br>`* Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|<li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li>|
|`+ First item` <br> `+ Second item`<br>`+ Third item`<br>`+ Fourth item`| `<ol>`<br>`<li>First item</li>`<br>`<li>Second item</li>`<br>`<li>Third item</li>`<br>`<li>Fourth item</li>`<br>`</ol>`|<li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li>|

## 无序列表最佳实践
Markdown applications don’t agree on how to handle different delimiters in the same list. For compatibility, don't mix and match delimiters in the same list — pick one and stick with it.

| ✅ Do this     | ❌ Don't do this     |
| :------------- | :------------- |
| `- First item` <br> `- Second item`<br>`- Third item`<br>`- Fourth item`      | `- First item` <br> `+ Second item`<br>`* Third item`<br>`- Fourth item`       |

---

## 在列表中嵌套其他元素
要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进四个空格或一个制表符，如下例所示：

### 段落
```
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.
```
渲染效果如下：
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.

### 引用块
```
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.
```

渲染效果如下:
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.

### 代码块
代码块通常采用四个空格或一个制表符缩进。当它们被放在列表中时，请将它们缩进八个空格或两个制表符。
```
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
```
渲染效果如下:
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

### 图片
```
1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![Tux, the Linux mascot](/Users/apple/Downloads/Markdown/tux.png)

3.  Close the file.
```
渲染效果如下:
1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![Tux, the Linux mascot](/Users/apple/Downloads/Markdown/tux.png)

3.  Close the file.

### 列表
You can nest an unordered list in an ordered list, or vice versa.
```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```
渲染效果如下:
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
