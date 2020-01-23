---
layout: default
title: Hộp
nav_order: 11
---

# Hộp
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Khai báo hộp

Hộp là một kiểu dữ liệu đặc biệt, nó có thể chứa dữ liệu bên trong, và có thể truy cập chúng thông qua
vị trí hoặc thuộc tính đã được định nghĩa. 

Cú pháp:
```js
[]
// Hoặc
[<các_giá_trị_khởi_tạo>]
```

Để khai báo hộp, ta chỉ cần sử dụng cặp ngoặc vuông `[]`. Có thể khởi tạo các giá trị ban đầu cho hộp
bằng cách cho các biểu thức vào trong cặp ngoặc, nhiều hơn hai thì cách nhau bởi dấu phẩy.

```js
x = []
y = [1, '2', 'năm']
```

## Sử dụng hộp

### Vị trí

Vị trí trong hộp là một con số, nơi sẽ luu trữ một giá trị trong hộp.

Sử dụng cặp ngoặc vuông theo sau kiểu hộp để tương tác với vị trí.
```js
x = []
x[1] = 4
x[2] = 5

in x[2]             // 4
in x[10-9] == x[1]  // đúng
```

Đối với hộp đã có giá trị khởi tạo, vị trí của các giá trị đó sẽ tương ứng với thứ tự của chúng
và bắt đầu từ 0.
```js
x = [1, 2, 3]
in x[0]     // 1
in x[1]     // 2
```

### Thuộc tính

Cũng giống như vị trí, nhưng thuộc tính sẽ là một chuỗi. Ta có thể sử dụng dấu chấm '.' để
truy cập tên thuộc tính viết liền không có khoảng cách.
```js
x = []
x['a'] = 4
x['b'] = 6
x.c = 3+3

in x['a']       // 4
in x.b == x.c   // đúng
```

Lưu ý: giống như biến, vị trí và thuộc tính chưa được định nghĩa thì khi truy cập sẽ trả về `rỗng`.


### Độ dài của hộp

Đây là kích thước (số lượng) các giá trị có vị trí liền kề nhau trong hộp bắt đầu từ 0.

Để lấy độ dài, ta chỉ cần truy cập thuộc tính `độDài` của hộp.
```js
x = [4, 5, 6]
in x.độDài  // 3
```

Tăng kích thước bằng cách tạo thêm vị trí có số bằng với độ dài hiện tại của hộp.
```js
x = [9]     // [0] -> 9
x[1] = 4    // [1] -> 4
x[2] = 6    // [2] -> 6
x[8] = 7
in x.độDài  // 3
```

## Hộp ngữ nghĩa

Cũng giống như hàm vậy, ta có thể sử dụng từ khóa để tạo hộp và tương tác với nó.

Tạo hộp với từ khóa `hộp..có/chứa`:
```js
x = hộp
y = hộp có 1, '2', 'ba'
z = hộp chứa 'bánh', 'kẹo'
```

Tạo thuộc tính và truy cập thuộc tính:
```js
x = hộp
x có 'a' = 10
x chứa 'b' = 2^2
in 'a' trong x  // 10
in 'b' của x    // 4
```

```js
hàm cộngHộp(a, b) = ('x' của a) + ('y' của b)
in cộngHộp([] có 'x' = 4, [] có 'y' = 6)    // 10
```
