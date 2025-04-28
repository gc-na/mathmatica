<!--
Meta Description: # Câu Lệnh "If" trong Mathematica: Cách Sử Dụng và Ví Dụ ## Tóm Tắt Câu lệnh `If` trong Mathematica cho phép thực hiện các quyết định dựa trên điều ki...
Meta Keywords: giá, trị, điều, kiện, nếu
-->

# Câu Lệnh "If" trong Mathematica: Cách Sử Dụng và Ví Dụ

## Tóm Tắt
Câu lệnh `If` trong Mathematica cho phép thực hiện các quyết định dựa trên điều kiện, giúp lập trình viên kiểm soát luồng thực thi của chương trình.

## Tài Liệu
Câu lệnh `If` trong Mathematica được sử dụng để kiểm tra một điều kiện và thực hiện một trong hai hành động tùy thuộc vào kết quả của điều kiện đó. Cú pháp cơ bản của câu lệnh `If` như sau:

```mathematica
If[điều kiện, giá trị nếu đúng, giá trị nếu sai]
```

- **Điều kiện**: Một biểu thức boolean (đúng hoặc sai).
- **Giá trị nếu đúng**: Giá trị hoặc biểu thức được trả về nếu điều kiện là đúng.
- **Giá trị nếu sai**: Giá trị hoặc biểu thức được trả về nếu điều kiện là sai (tùy chọn).

### Chi Tiết
- Nếu chỉ cần một giá trị cho trường hợp sai, bạn có thể bỏ qua tham số thứ ba:
  
  ```mathematica
  If[điều kiện, giá trị nếu đúng]
  ```

- Nếu điều kiện là đúng, giá trị thứ hai sẽ được trả về; ngược lại, giá trị thứ ba (nếu có) sẽ được trả về.

## Ví Dụ
### Ví dụ 1: Kiểm Tra Số Dương
```mathematica
If[5 > 0, "Số là dương", "Số là âm"]
```
Kết quả: `"Số là dương"`

### Ví dụ 2: Kiểm Tra Số Chẵn
```mathematica
If[Mod[4, 2] == 0, "Số chẵn", "Số lẻ"]
```
Kết quả: `"Số chẵn"`

### Ví dụ 3: Sử Dụng Nếu Không Có Giá Trị Sai
```mathematica
If[3 < 2, "Sai"]
```
Kết quả: `Null` (Không có giá trị trả về)

## Giải Thích
Khi sử dụng câu lệnh `If`, một số người mới có thể mắc phải những sai lầm sau:
- **Không sử dụng dấu ngoặc đúng cách**: Cần đảm bảo rằng điều kiện và các giá trị được định nghĩa trong ngoặc vuông đúng cách.
- **Quên giá trị nếu sai**: Nếu bạn bỏ qua giá trị thứ ba, hãy chắc chắn rằng điều đó không ảnh hưởng tới logic của chương trình.
- **Sử dụng các biểu thức không boolean**: Đảm bảo điều kiện là một biểu thức có thể đánh giá thành đúng hoặc sai.

## Tóm Tắt Một Dòng
Câu lệnh `If` trong Mathematica cho phép thực hiện các quyết định dựa trên điều kiện, trả về giá trị tương ứng với kết quả của điều kiện đó.