<!--
Meta Description: # Mathematica 的 "Case" 語句：條件判斷與分支執行 ## 概述 在 Mathematica 中，"Case" 是一種強大的條件判斷語句，用於根據不同的情況執行相應的代碼塊。它類似於其他編程語言中的 switch 語句，能夠根據表達式的值選擇性地執行多個選項中的一個。 ## 文檔 ...
Meta Keywords: case, mathematica, positive, switch, expression
-->

# Mathematica 的 "Case" 語句：條件判斷與分支執行

## 概述
在 Mathematica 中，"Case" 是一種強大的條件判斷語句，用於根據不同的情況執行相應的代碼塊。它類似於其他編程語言中的 switch 語句，能夠根據表達式的值選擇性地執行多個選項中的一個。

## 文檔
### 目的
"Case" 語句的主要目的是提供一種簡潔的方法來處理多種條件的情況。它使得代碼更加容易閱讀和維護，特別是當需要多個分支條件時。

### 使用方法
基本語法如下：
```mathematica
Case[expression, pattern1 :> result1, pattern2 :> result2, ... , _, defaultResult]
```
- `expression` 是要檢查的表達式。
- `pattern1`, `pattern2`, 等是要匹配的模式。
- `result1`, `result2`, 等是匹配到相應模式時的結果。
- `_` 是一個通配符，用來匹配未被其他模式捕獲的情況。
- `defaultResult` 是當沒有任何模式匹配時的返回結果。

### 詳細說明
1. **模式匹配**：在使用 "Case" 時，模式是核心。每個模式可以是具體的值、表達式或使用模式符號（如 `_`）來捕獲變量。
2. **優先順序**：按順序檢查每個模式，找到第一個匹配的模式並執行相應的結果。
3. **預設結果**：如果所有模式均不匹配，則返回預設結果。如果沒有指定預設結果，則返回 `Null`。

## 範例
### 基本使用範例
```mathematica
result = Case[2, 1 :> "One", 2 :> "Two", 3 :> "Three", _, "Unknown"]
(* 輸出: "Two" *)
```

### 使用模式符號
```mathematica
result = Case[5, n_ /; n > 0 :> "Positive", n_ :> "Non-positive"]
(* 輸出: "Positive" *)
```

## 解釋
### 常見的陷阱與注意事項
- **模式的順序**：確保更具體的模式在前，否則可能會被更通用的模式捕獲。
- **未匹配的情況**：考慮在沒有匹配時提供合理的預設結果，以避免返回 `Null`。
- **性能考量**：對於大量的模式，"Case" 可能不如其他條件語句（如 `If` 或 `Switch`）高效，因此在性能關鍵的應用中需謹慎使用。

## 一句總結
"Case" 語句在 Mathematica 中提供了一種方便的方式來根據不同情況執行相應的代碼，增強了代碼的可讀性和維護性。