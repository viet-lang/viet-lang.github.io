---
layout: default
title: Toán tử
nav_order: 6
---

# Toán tử
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Toán tử số học

Có 5 phép toán:
- `+`: cộng
- `-`: trừ
- `*`: nhân
- `/`: chia
- `%`: chia lấy dư
- `^`: lũy thừa

Ví dụ
```js
in 4 + 5 + 6 - 7        // 8
in -69                  // -69
in 12 * 24              // 288
in 15 / 3               // 5
in 3.14 * 5 ^ 2         // 78.5
in 4096 % 199           // 116
```

Phép cộng có thể cộng giữa hai số hoặc một bên là chuỗi và một bên là bất kỳ kiểu dữ liệu nào, các phép
toán còn lại chỉ chấp nhận hai số.

Ví dụ:
```js
in 'tôi có ' + 30000 + ' đồng'
in 'không sai nghĩa là ' + đúng
in 'một năm có' + (3600 * 24 * 365) + ' phút'
```

## Toán tử so sánh

Có 5 phép toán so sánh chính:
- `<`:  bé hơn
- `>`:  lớn hơn
- `<=`: bé hơn hoặc bằng
- `>=`: lớn hơn hoặc bằng
- `==`: bằng nhau

Ví dụ:
```js
in 6 < 5                // sai
in 1+2 >= 3             // đúng
in 7749 <= 77*49        // sai
in 'abc' == 'a'+'bc'    // đúng
```

4 phép so sánh lớn/bé chỉ cho phép so sánh giữa hai giá trị có cùng kiểu dữ liệu số,
phép so sánh bằng hỗ trợ bất kỳ kiểu dữ liệu nào.

## Toán tử logic

### Phép phủ định

Cú pháp: `!<biểu_thức>`, dấu chấm than `!` và theo sau là một biểu thức, có thể thay dấu này bằng từ khóa `không`.
Phép phủ định chấp nhận mọi kiểu dữ liệu, khi dùng với `sai`, `0` và `rỗng` sẽ luôn cho kết quả `đúng`, ngược lại thì các kết quả khác đều là `sai`.

Ví dụ:
```js
in không đúng           // sai
in !sai                 // đúng
in !!!0                 // đúng
in không 'là tôi'       // sai
```

### Phép và

Cú pháp: `<biểu_thức1> và <biểu_thức2>`.

Phép toán này sẽ kiểm tra xem giá trị của biểu thức 1 có đúng hay không,
nếu sai thì trả về giá trị của biểu thức 1, ngược lại thì trả về giá trị của biểu thức 2.
Thực hiện từ trái sang phải, nếu giá trị của biểu thức 1 sai thì biểu thức thứ hai sẽ không được thực hiện.

Ví dụ:
```js
in 4 và 5               // 5
in sai và 16            // sai
in đúng và sai          // sai
in 'không' và 1         // 1
```

### Phép hoặc

Cú pháp: `<biểu_thức1> hoặc <biểu_thức2>`.

Ngược lại với phép và, phép hoặc kiểm tra xem giá trị của biểu thức 1 có đúng hay không, nếu sai thì trả về giá trị của biểu thức 2, đúng thì trả về giá trị của biểu thức 1 và không thực hiện biểu thức 2.

```js
in 4 hoặc 5             // 4
in sai hoặc đúng        // đúng
in đúng hoặc (55*66)    // đúng  
```

## Thứ tự của các toán tử

updating...

Để thay đổi thứ tự tính toán, ta chỉ cần sử dụng cặp ngoặc tròn để nhóm các biểu thức với nhau.

```js
in (1+2) * 3            // 9
in 'anh ' + ('không' + ' có tiền')
in 'Ừ, ' + (29+1) + ' chưa phải là ' + ('T'+('ế'+'t')) + '!'
```
