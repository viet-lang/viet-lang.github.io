---
layout: default
title: Tổng quan
nav_order: 2
---

# Tổng quan
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Giới thiệu

Cùng tên với dự án - ngôn ngữ lập trình **Việt**, đây cũng là một concept đầu tiên về ngôn ngữ lập trình
hỗ trợ tiếng Việt. Cả project này là phần triển khai của ngôn ngữ được viết bằng **Javascript**
và chạy trên nền tảng trình duyệt (hoặc một Javascript engine).

Trong thời gian tới, sẽ có các phần triển khai của ngôn ngữ được viết bằng C/C++ để tối ưu hóa tốc độ
của ngôn ngữ và dễ dàng triển khai trên các nền tảng khác nhau.

### FAQ

_Tại sao lại chọn Javascript để viết phần triển khai đầu tiên của ngôn ngữ?_
> Vì tiếng Việt khá phức tạp, mọi thứ đều là unicode. Sự lựa chọn Javascript và nền tảng web sẽ giúp
đơn giản hóa mọi thứ, khiến việc triển khai thuận tiện và nhanh chóng hơn.

_Tôi có thể làm gì với ngôn ngữ này?_
> Nó chưa hoàn thiện, nên không thể trả lời được

## Những điều cơ bản nhất

### Các từ khóa

Việt có 29 từ khóa chính (các từ khóa được liệt kê cùng dòng sẽ giống nhau)
- `và`
- `đừng`
- `hay`
- `sai`
- `cho`
- `hàm`
- `nếu`
- `rỗng`
- `hoặc`
- `in`
- `trả`
- `đúng`
- `biến`
- `khi`
- `không`
- `thì`
- `thôi` `xong`
- `thoát`
- `bằng` `là` 
- `có` `chứa`
- `của` `trong`
- `hộp` 
- `gọi` `đi`
- `với`

Khi gõ code, sẽ không phân biệt chữ hoa, chữ tường, chữ có dấu với chữ không dấu.
Chẳng hạn từ `nếu` và `neu` hay `KHi` và `khi` đều là giống nhau. Như vậy sẽ giúp
người dùng dễ dàng sử dụng hơn khi không thể gõ được dấu, hoặc không viết hoa đúng chỗ.

Tất cả các ký tự không phải **chữ cái**, không phải **từ khóa**, **tiếng Việt có dấu** hay các **ký tự unicode**
viết _liền nhau_ và bắt đầu không phải là số được gọi là **định danh** (identifier), sẽ được dùng cho tên biến.
```js
sốNăm
con_gà
😁🚗
```

Không chấp nhận:
```
1xyz
?ee
>>abc
```

### Không cần thiết phải có chấm phẩy ';'

Dấu chấm phẩy có lẽ là vấn đề đau đầu trong các ngôn ngữ lập trình họ **C**, thiếu một chút
là có thể thay đổi cả chương trình.

```js
x = 4
-5;
x = 4;
-5;
```

Trong đoạn code trên, `x` ở dòng thứ nhất sẽ có giá trị là -1 (tức 4 trừ 5), còn đối với dòng thứ ba thì
kết quả là 4.

Trong **Việt**, chúng tôi đã đơn giản hóa dấu chấm phẩy (có thể có hoặc không điều được).
Cách ngắt câu lệnh cũng sẽ khác đi một tí, nếu kết thúc (hoàn toàn) câu lệnh và sau đó là xuống dòng
thì dòng sau sẽ là lệnh mới. Nhưng nếu lệnh cũ còn dấu câu nối tiếp thì dòng sau vẫn được tính là
nối tiếp dòng trước.

```js
x = 4 -
5
x = 4
-5
```

### Chú thích

Giống như các ngôn ngữ họ **C**, nhưng **Việt** chỉ hỗ trợ chú thích bằng hai dấu xẹt `//`.

```js
// Đây là chú thích
// Bắt đầu sau hai dấu '//' và kéo dài cho đến hết dòng
a = 4 // Gán biến 'a' bằng 4
```

### Câu lệnh 'in'

Đây là câu lệnh căn bản nhất, nó sẽ in ra kết quả của biểu thức sau từ khóa in.

```js
in 10
in 4+5
in 'Chào thế giới!'
```
