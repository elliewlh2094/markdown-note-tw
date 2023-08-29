# Markdown 語法筆記

> 本文參考 GitHub 官方文件 [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) 和 John Gruber 撰寫的 [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) 。

## 關於 Markdown
Markdown 是一種輕量級的標記語言，由 John Gruber（和 Aaron Swartz 的幫助下）於 2004 年開發，用於將文字用簡單的方式轉換為 HTML。  
與其他更複雜的標記語言（如 HTML）或排版系統（如 LaTeX）相比，Markdown 的功能較少，但這也使得它更容易上手。

根據 Markdown 官方的介紹文所說：**「Markdown 的目標是實現『易讀易寫』。」**  
用 Markdown 語法編寫的原始文件不需要特別學習便可以直接閱讀，而文件經渲染後可以讓文章看起來更有結構和有條理，非常適合用於在支援 Markdown 語法的網路平台（如 GitHub 、HackMD）上書寫文章、筆記等。

現在許多平台皆支援 Markdown 語法，但根據支援程度差異，相同語法也會有不同的顯示效果，有些平台的 Markdown 渲染器還會支援部分 HTML 語法，使得文章編排版型有更多方便的選擇。

### 支援 Markdown 的文字編輯器
- GitHub：可以支援大部分的 Markdown 語法和內嵌 HTML。
- Visual Studio Code (VS Code) ：不僅支援 Markdown 語法，還可以同步預覽效果。
- HackMD：不僅支援 Markdown 語法，還可以同步預覽效果。同時作為一個筆記平台，有許多平台專屬的特殊語法，也支援共同協作編寫共同筆記。

### 跳過說明一鍵複製
請直接查看 [markdown-cheatsheet-tw](markdown-cheatsheet-tw.md) 。

### 快速導航
- [標題（Headers）](#標題（Headers）)
  - 用 \# 建立標題
  - 用 = 和 -
- [段落（Paragraphs）](#段落（Paragraphs）)
  - 分出段落
  - 段落內換行
  - 創造多行空行
  - 分隔線
- [清單（Lists）](#清單（Lists）)
  - 無序清單
  - 有序清單
  - 清單換行
  - 清單段落
  - 任務清單
- [引文（Quotations）](#引文（Quotations）)
- [字體變化（Types）](#字體變化（Types）)
- [特殊符號（Symbols）](#特殊符號（Symbols）)
  - 具有語法意義的符號
  - 表情符號
- [連結（Links）](#連結（Links）)
  - 使用外部連結
  - 使用內部連結
  - 自動連結
  - 錨點連結
- [圖片（Images）](#圖片（Images）)
  - 使用外部圖片連結
  - 使用內部圖片連結
- [程式碼（Codes）](#程式碼（Codes）)
  - 行內程式碼
  - 區塊程式碼
- [表格（Sheets）](#表格（Sheets）)

---

## 標題（Headers）
### 用 \# 建立標題
使用 `#` 可以建立標題，每多一個 `#` 會成為次一層級的標題。  
當 Markdown 文件中具有兩個以上的標題時， GitHub 會自動生成一個目錄，方便檢視時直接跳到該標題。

以下是所有層級標題的樣子：

# 一級標題

## 二級標題

### 三級標題

#### 四級標題

##### 五級標題

###### 六級標題，這是最多了

使用方式：
```
# 一級標題

## 二級標題

### 三級標題

#### 四級標題

##### 五級標題

###### 六級標題，這是最多了
```

### 用 = 和 -
在文字底下加三個 `=` 或 `-` 也會變成一級標題或二級標題。

效果如下：

一級標題
===

二級標題
---

使用方式：
```
一級標題
===

二級標題
---
```
<br>

## 段落（Paragraphs）
### 分出段落

如果要區分不同的段落，需要在段落和段落之間空一個空行。如果只是單純的換行，在 Markdown 語法中會視同一個空格，並且直接接在上一句文字之後。

效果如下：

這是第一句
這是只有換行的第二句

這是空一個空行的第三句
```
這是第一句
這是只有換行的第二句

這是空一個空行的第三句
```
### 段落內換行
一段文字結尾後加上 2 個空格，則這時候便能夠展現段落之內的換行效果。

效果如下：

這是第一行  
這是第二行

這是下一段

使用方式：
```
這是第一行  
這是第二行

這是下一段
```

### 創造多行空行
無論中間有多少空行都只會被視為一個空行，因此在 Markdown 文件中要產生多個空行，只能借用 HTML 語法的換行標籤 `<br>`。

效果如下：

這是第一行。<br><br><br><br>
這是第五行。

使用方式：
```
這是第一行。<br><br><br><br>
這是第五行。
```

### 分隔線
使用連續三個 `-` 或 `*` 可創造分隔線，注意和前一段文字要空一行，不然會變成二級標題。

效果如下：

---
***

使用方式：
```
---
***
```
<br>

## 清單（Lists）
### 無序清單
使用 `*` 或 `-` 來創建無序清單，在 `*` 或 `-` 前面用 2 個空格（或是 4 個空格）縮排可以創建子清單。

效果如下：

- 清單
- 清單
  - 清單
    - 清單
- 清單
    - 清單
        - 清單

使用方式：
```
- 清單
- 清單
  - 清單
    - 清單
- 清單
    - 清單
        - 清單
```

### 有序清單
使用 `1.` 、 `2.` 來創建有序清單，**數字前面用 4 個空格縮排**可以創建子清單。

> Note: 當使用有序清單時可以不用按照順序新增，渲染器會自動按照數字排序。也就是全部打 1. 也是可以的。

效果如下：

1. 清單
1. 清單
1. 清單
    1. 清單
        1. 清單

使用方式：
```
1. 清單
1. 清單
1. 清單
    1. 清單
        1. 清單
```
### 清單換行
無論是在有序清單或是無序清單中，想要換行也是透過 2 個空格來換行。

效果如下：

- 這是清單
直接換行會接在後面

- 這是清單，在句尾加 2 個空白  
  就可以換行（習慣清單內文字也用 2 個空白縮排）

1. 這是清單，在句尾加 2 個空白  
  就可以換行（習慣清單內文字也用 2 個空白縮排）

使用方式：
```
- 這是清單
  直接換行會接在後面

- 這是清單，在句尾加 2 個空白  
  就可以換行（習慣清單內文字也用 2 個空白縮排）

1. 這是清單，在句尾加 2 個空白  
  就可以換行（習慣清單內文字也用 2 個空白縮排）
```

### 清單段落

效果如下：

- 這是清單，在句尾加 2 個空白  
  在清單裡換行

  用 2 個空白縮排可以建立清單的第二個段落

使用方式：
```
- 這是清單，在句尾加 2 個空白  
  在清單裡換行

  用 2 個空白縮排可以建立清單的第二個段落
```
### 任務清單
使用 `- [ ]` 可以建立 Checklist，如果中間的空白改成 X ，也就是 `- [X]` ，則會打勾。

效果如下：

- [ ] Task 1
- [X] Task 2
- [ ] Task 3

使用方式：
```
- [ ] Task 1
- [X] Task 2
- [ ] Task 3
```
<br>

## 引文（Quotations）
在文字前加上 `>` 可以呈現引用文字的效果，和清單一樣可以建立多層引用。

效果如下：

> 引用文字
> > 引用文字
> > > 引用文字

使用方式：
```
> 引用文字
> > 引用文字
> > > 引用文字
```
<br>

## 字體變化（Types）
Markdown 支援多種字體變化，包含斜體、粗體、斜粗體、刪除線、上標和下標。

效果如下：

*斜體字* 、 **粗體字** 、 ***斜粗體*** 、 ~刪除線~ 、 文字<sup>上標</sup> 和 文字<sub>下標</sub> 。

使用方式：
```
*斜體字* 、 **粗體字** 、 ***斜粗體*** 、 ~刪除線~ 、 文字<sup>上標</sup> 和 文字<sub>下標</sub> 。
```
<br>

## 特殊符號（Symbols）
### 具有語法意義的符號
\` \* \_ \{ \} \[ \] \( \) \# \+ \- \. \! \| 這些符號在 Markdown 語法中具有特殊語法意義，在一般文字中有時候沒辦法正常顯示，因此需要在符號前加上一個反斜線 `\` 使其可以強制顯示。

### 表情符號
使用兩個冒號 `:` 將特定文字包起來可以顯示表情符號，常用表情符號表可以參考 [emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)。

效果如下：

sweat smile: :sweat_smile:  
heart eyes: :heart_eyes:

使用方式：
```
sweat smile: :sweat_smile:  
heart eyes: :heart_eyes:
```
<br>

## 連結（Links）
### 簡易連結
直接在連結或是信箱兩側加上 `<>` 便能夠快速建立一個連結。

效果如下：

這是連結: <https://github.com/elliewlh2094/markdown-practice>

使用方式：
```
這是連結: <https://github.com/elliewlh2094/markdown-practice>
```

### 使用外部連結
使用 `[顯示文字](外部連結)` 可以建立連結，並且可以編輯連結顯示的文字。

效果如下：

這是[這個 Repo 的連結](https://github.com/elliewlh2094/markdown-practice)

使用方式：
```
這是[這個 Repo 的連結](https://github.com/elliewlh2094/markdown-practice)
```

### 使用內部連結
如果想在文件中連結 GitHub 上相同 Repo 的檔案，可以將連結改成文件內的相對路徑，也就是使用 `[顯示文字](內部連結)` 可以建立內部連結。

效果如下：

查看 [markdown-cheatsheet-tw](markdown-cheatsheet-tw.md)

使用方式：
```
查看 [markdown-practice.md](markdown-practice.md)
```
### 錨點連結
如果想在相同文件中的不同標題跳轉，可以將連結改成 `#標題文字`，也就是使用 `[顯示文字](#標題文字)` 如此便能建立錨點連結。

效果如下：

[跳到連結](#連結（Links）)

使用方式：
```
[跳到連結](#連結)
```
<br>

## 圖片（Images）
### 使用外部圖片連結
和建立連結的做法相似，但多加一個驚嘆號，使用 `![顯示文字](外部連結)` 可以插入圖片。 

效果如下：[Photo by Daniel Radford on Unsplash](https://unsplash.com/photos/8TMaXnXF9_8)

![img](https://images.unsplash.com/photo-1569527129264-02fbc2b075db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2340&q=80)

### 使用內部圖片連結
將外部連結改成在文件中連結 GitHub 上相同 Repo 的檔案，也就是使用 `![顯示文字](內部連結)` 也可以插入圖片。
<br>

## 程式碼（Codes）
### 行內程式碼
使用反引號 \` 將一段文字包起來，可以顯示一段行內的程式碼。

效果如下：

這是一段行內的程式碼: `printf("The number is %d.\n", num);` 。

使用方式：
```
這是一段行內的程式碼: `printf("The number is %d.\n", num);` 。
```
### 區塊程式碼
使用三個反引號 \` 便能夠顯示一個程式碼區塊，如果在開頭的反引號後面標註程式語言，如 c、python 還可以根據語法而有不同顏色。  
前面的使用方式也都是使用區塊程式碼來呈現。

效果如下：

```c
#include <stdio.h>
int main(void) /* display an integer on screen */
{
  int num;
  num = 40;
  printf("The number is %d.\n", num);
  return 0;
}
```

使用方式：

\```c  
#include <stdio.h>  
int main(void) /* display an integer on screen */  
{  
  int num;  
  num = 40;  
  printf("The number is %d.\n", num);  
  return 0;  
}  
\```
<br>

## 表格（Sheets）
使用 `|` 將文字包起來可以形成一個簡易的表格，並且可以透過 `:--`、`--:` 和 `:--:` 來調整表格中置左、置右或是置中。

| 欄位1 | 欄位2 | 欄位3 |
| :-- | --: |:--:|
| 整欄置左  | 整欄置右 | 整欄置中 |
| $100 | $100 | $100 |
| $10 | $10 | $10 |
| $1  | $1 | $1 |

```
| 欄位1 | 欄位2 | 欄位3 |
| :-- | --: |:--:|
| 整欄置左  | 整欄置右 | 整欄置中 |
| $100 | $100 | $100 |
| $10 | $10 | $10 |
| $1  | $1 | $1 |
```
