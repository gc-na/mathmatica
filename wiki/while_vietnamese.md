<!--
Meta Description: # Câu lệnh "While" trong Mathematica: Hướng dẫn Chi tiết và Ví dụ ## Tóm tắt Câu lệnh "While" trong Mathematica cho phép người dùng thực hiện một khối...
Meta Keywords: lặp, while, một, điều, kiện
-->

# Câu lệnh "While" trong Mathematica: Hướng dẫn Chi tiết và Ví dụ

## Tóm tắt
Câu lệnh "While" trong Mathematica cho phép người dùng thực hiện một khối lệnh lặp lại cho đến khi một điều kiện nhất định trở thành sai. Đây là một công cụ mạnh mẽ cho việc lập trình lặp và điều kiện trong các ứng dụng tính toán.

## Tài liệu
Câu lệnh "While" trong Mathematica có cú pháp như sau:

```mathematica
While[condition, body]
```

### Mục đích
Câu lệnh "While" được sử dụng để thực hiện một khối mã (body) lặp đi lặp lại miễn là điều kiện (condition) được chỉ định vẫn đúng (True). Khi điều kiện trở thành sai (False), vòng lặp sẽ dừng lại.

### Cách sử dụng
- **condition**: Đây là một biểu thức logic. Nếu biểu thức này trả về True, khối lệnh body sẽ được thực hiện.
- **body**: Đây là một hoặc nhiều lệnh mà bạn muốn thực hiện khi điều kiện vẫn đúng.

### Chi tiết
Khi sử dụng "While", điều quan trọng là phải đảm bảo rằng điều kiện sẽ trở thành sai tại một thời điểm nào đó để tránh việc tạo ra vòng lặp vô tận. Người dùng nên cẩn thận kiểm tra và đảm bảo rằng các biến trong điều kiện sẽ thay đổi trong mỗi lần lặp.

## Ví dụ
### Ví dụ 1: Lặp đơn giản
```mathematica
i = 1;
While[i <= 5, Print[i]; i++];
```
Kết quả sẽ in ra các số từ 1 đến 5.

### Ví dụ 2: Tính toán tổng
```mathematica
total = 0;
i = 1;
While[i <= 10, total += i; i++];
total
```
Kết quả là tổng của các số từ 1 đến 10, tức là 55.

### Ví dụ 3: Vòng lặp với điều kiện phức tạp
```mathematica
n = 1;
While[n < 100, If[Mod[n, 2] == 0, Print[n]]; n++];
```
Kết quả sẽ in ra tất cả các số chẵn nhỏ hơn 100.

## Giải thích
Khi sử dụng câu lệnh "While", người dùng cần lưu ý một số điểm sau:
- **Vòng lặp vô tận**: Nếu điều kiện không bao giờ trở thành sai, vòng lặp sẽ tiếp tục mãi mãi. Hãy chắc chắn rằng bạn có một cách để điều kiện thay đổi.
- **Hiệu suất**: Vòng lặp "While" có thể không hiệu quả bằng các cấu trúc khác như "For" hoặc "Do" trong một số trường hợp, vì "While" kiểm tra điều kiện trước mỗi lần lặp.

## Tóm tắt một dòng
Câu lệnh "While" trong Mathematica cho phép thực hiện một khối lệnh lặp đi lặp lại cho đến khi một điều kiện nhất định trở thành sai.