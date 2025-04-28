<!--
Meta Description: # Mathematica 中的 "for" 循環語句 ## 概述 在 Mathematica 中，"for" 循環語句是一種控制結構，用於重複執行一段程式碼，直到滿足特定條件。這類語句對於處理重複任務和迭代計算特別有用。 ## 文檔 ### 目的 "for" 循環語句允許使用者以簡潔的方式進行重複...
Meta Keywords: mathematica, test, start, increment, body
-->

# Mathematica 中的 "for" 循環語句

## 概述
在 Mathematica 中，"for" 循環語句是一種控制結構，用於重複執行一段程式碼，直到滿足特定條件。這類語句對於處理重複任務和迭代計算特別有用。

## 文檔
### 目的
"for" 循環語句允許使用者以簡潔的方式進行重複運算，特別是在需要對數據進行批量處理或多次計算的場合。

### 用法
在 Mathematica 中，"for" 循環通常以 `For[start, test, increment, body]` 的語法來使用：
- **start**：初始化變數的值。
- **test**：條件測試，當條件為真時，循環繼續執行。
- **increment**：在每次迭代後，變數的增量或變化。
- **body**：當條件為真時執行的程式碼區塊。

### 詳細說明
"for" 循環的結構如下：
```mathematica
For[i = start, test, increment, body]
```
在這裡，`i` 是控制變數，`start` 是其初始值，`test` 是判斷循環是否繼續的條件，`increment` 是更新 `i` 值的表達式，而 `body` 是循環中要執行的程式碼。

## 範例
以下是幾個基本用法的範例：

1. 計算 1 到 5 的總和：
   ```mathematica
   sum = 0;
   For[i = 1, i <= 5, i++, sum += i];
   sum
   ```

2. 列印數字 1 到 5：
   ```mathematica
   For[i = 1, i <= 5, i++, Print[i]];
   ```

3. 使用 "for" 循環求解平方數：
   ```mathematica
   squares = {};
   For[i = 1, i <= 5, i++, AppendTo[squares, i^2]];
   squares
   ```

## 解釋
### 常見陷阱
- **無窮迴圈**：確保 `test` 條件能夠在某一點變為假，否則將導致無限循環。
- **變數範圍**：在循環內部修改控制變數可能會導致意外行為。
- **性能問題**：在需要大量重複運算時，考慮使用其他 Mathematica 的高階函數，如 `Table` 或 `Map`。

## 一句話總結
Mathematica 的 "for" 循環語句是一種強大的工具，用於執行重複計算和數據處理。