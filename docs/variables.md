---
layout: default
title: Biến và kiểu dữ liệu
nav_order: 3
---

# Biến và kiểu dữ liệu
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Khai báo biến

Cú pháp:
```
biến <tên_biến> [= <giá_trị>]
```

Đầu tiên là từ khóa `biến`, theo sau là `tên_biến` (không được trùng với từ khóa). Nếu chỉ có 2 thành phần trên thì
biến sẽ mang giá trị là `rỗng`, thêm dấu bằng `=` và một giá trị theo sau để gán cho biến.

Biến chưa được khai báo, nếu sử dụng sẽ báo lỗi là chưa định nghĩa.

## Kiểu dữ kiệu

### Logic (boolean)

Kiểu này chỉ có thể chứa một trong 2 giá trị, là `đúng` hoặc `sai`.

```js
biến khôngĐúng = sai
in đúng
```

### Số (number)

```js
biến một = 1
biến mườiLăm = 15
biến PI = 3.14
in 0xFF // 255, hệ thập lục
```

Là các số nguyên hoặc số thực. Đối với số thực sẽ có dấu chấm sau phần nguyên, và theo sau là phần thập phân.
Ta có thể viết số trong hệ thập lục (cơ số 16) bằng cách viết hai ký tự `0x` và theo sau là các chữ số trong hệ.

### Rỗng (null)

Đúng với tên gọi, có thể hiểu (một cách trừu tượng) là không có gì, không mang giá trị gì,
hoàn toàn trống rỗng.

Ví dụ:
```js
biến a
in a    // rỗng
in ()   // rỗng
in rỗng
```

Như đã nói ở phần trên, một biến được khai báo mà không gán bất cứ giá trị nào sẽ mang giá trị là `rỗng`.
Để tạo kiểu `rỗng` thì ta có thể sử dụng từ khóa `rỗng` hoặc cặp ngặc tròn liền nhau `()`.

### Chuỗi (string)

Là một chuỗi ký tự. Khi khai báo chuỗi, chỉ cần cho đoạn chuỗi vào trong cặp dấu nháy kép `"` hoặc
dấu nháy đơn `'` là được.

Ví dụ:
```js
biến chào = "Xin chào!"
biến nămMới = 'Happy new year!'
in 'Nhà tôi có một vườn cau.'
```

### Hàm (function)

Kiểu này chỉ cần biết là khi in sẽ xuất hiện chữ `hàm`.
Chuyển sang trang [Hàm]() để xem chi tiết cách khai báo và sử dụng.
