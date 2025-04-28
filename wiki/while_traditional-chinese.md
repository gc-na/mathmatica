<!--
Meta Description: # Mathematica 的 "While" 迴圈指令：用法與範例 ## 簡介 在 Mathematica 中，`While` 是一個控制流程的指令，用來重複執行一段程式碼，直到指定的條件不再成立。這使得 `While` 在處理需要重複計算的情況下非常有用。 ## 文檔說明 `While` 指令的...
Meta Keywords: while, mathematica, condition, body, true
-->

# Mathematica 的 "While" 迴圈指令：用法與範例

## 簡介
在 Mathematica 中，`While` 是一個控制流程的指令，用來重複執行一段程式碼，直到指定的條件不再成立。這使得 `While` 在處理需要重複計算的情況下非常有用。

## 文檔說明
`While` 指令的語法如下：
```mathematica
While[condition, body]
```
- **condition**：在每次迭代開始時檢查的布林條件。只要這個條件為 `True`，`While` 就會繼續執行 `body`。
- **body**：當 `condition` 為 `True` 時要執行的程式碼塊。

### 用途
`While` 迴圈通常用於當迴圈的執行次數不確定時，或是當需要根據某些條件動態調整執行的情況。

### 注意事項
- 如果 `condition` 總是返回 `True`，則 `While` 迴圈將進入無窮迴圈，需謹慎使用。
- `body` 中的程式碼必須在某個時候改變 `condition`，否則將無法退出迴圈。

## 範例
### 基本用法
以下範例展示 `While` 的基本用法：
```mathematica
i = 1;
While[i <= 5,
  Print[i];
  i++;
]
```
這段程式碼將輸出數字 1 到 5，每次迭代中 `i` 的值都會增加。

### 使用 `While` 計算階乘
以下範例使用 `While` 來計算一個數字的階乘：
```mathematica
factorial[n_] := Module[{result = 1, i = 1},
  While[i <= n,
    result *= i;
    i++;
  ];
  result
]

factorial[5]  (* 輸出 120 *)
```
這段程式碼定義了一個計算階乘的函數，並在 `While` 迴圈中逐步計算。

## 解釋
- **常見陷阱**：在使用 `While` 時，必須確保 `condition` 最終會變為 `False`，否則將導致無窮迴圈，造成程式掛起。
- **執行效率**：相較於其他迴圈結構（如 `For` 或 `Do`），`While` 迴圈對於條件變化的檢查是動態的，因此在某些情況下可能會增加執行時間。

## 一句總結
`While` 是 Mathematica 中用於根據條件重複執行程式碼的強大迴圈指令。