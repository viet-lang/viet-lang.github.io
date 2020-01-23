---
layout: default
title: Hàm
nav_order: 10
---

# Hàm
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Khai báo hàm

Cú pháp:
```js
hàm <tên_hàm>([các_tham_số])
    <thân_hàm>
xong

// Hoặc như này
hàm <tên_hàm>([các_tham_số]) {
    <thân_hàm>
}
```

Để khai báo một hàm, ta sử dụng từ khóa `hàm`, theo sau là tên của hàm. Tiếp theo là cặp ngoặc tròn
chứa các tham số bên trong (có thể có hoặc không). Tiếp tục đến phần thân hàm, và kết thúc là từ khóa
`xong` hoặc `thôi`.

Có thể viết phần thân hàm bằng cách đặt chúng vào trong cặp dấu ngoặc nhọn `{..}`.

Một hàm chỉ có thể được khai báo trong phần thân chương trình chính.

## Trả về

Để cho hàm trả về kết quả, ta chỉ cần thêm từ khóa `trả` và theo sau là một biểu thức.
```js
hàm mười()
    trả 5+5
xong

hàm khôngĐúng()
    trả sai
xong
```

Ta có thể chỉ ghi từ khóa `trả` mà không cần biểu thức theo sau, nhưng bắt buộc phải đặt trước từ khóa `xong`
hoặc dấu đóng ngoặc nhọn `}`. Lúc này, hàm sẽ trả về `rỗng`.

```js
hàm lấyRỗng()
    nếu sai thì
        trả     // ở đây
    thôi     
    trả rỗng    // ở chỗ này
    trả         // và đây đều giống nhau
xong
```

## Sử dụng hàm

Cú pháp:
```js
// Chỉ gọi hàm
<tênHàm>([tham_số_truyền_vào])

// Lấy kết quả trà về từ hàm
<biến> = <tênHàm>([tham_số_truyền_vào])
```

Ví dụ:
```js
hàm inMười()
    in 10
xong

inMười()    // 10
```

```js
hàm mườiHai()
    trả 12
xong

in mườiHai()    // 12
```

```js
hàm mườiTámCộng(x)
    trả 18 + x
xong

in mườiTámCộng(2)   // 20
```

Lưu ý:
- Nếu truyền vào số lượng tham số khác với khai báo của hàm thì chương trình sẽ báo lỗi!
- Như đã nói ở phần [Biến và kiểu dữ liệu](), hàm cũng là một kiểu dữ liệu.

## Một số thứ đặc biệt

### Hàm đệ qui

Hàm đệ qui sẽ gọi lại chính nó, và cần có ít nhất một điều kiện để hàm thoát. Nếu không sẽ trở thành vòng lặp vô hạn
và dẫn đến **tràn ngăn xếp** (stack overflow).

Chẳng hạn, ta có hàm tìm số thứ N trong dãy fibonacci như sau:
```js
hàm tìmFibo(N)
    nếu N < 2 thì trả N
    trả tìmFibo(N-2) + tìmFibo(N-1)
xong

in tìmFibo(10)  // 55
```

Ta có thể dùng từ khóa `hàm` thay cho biến `tìmFibo`, trình biên dịch sẽ nhận biết là chính nó.
```js
hàm tìmFibo(N)
    nếu N < 2 thì trả N
    trả hàm(N-2) + hàm(N-1)
xong
```

### Hàm rút gọn

Đây là một kiểu khai báo dành cho hàm chỉ thực hiện một lệnh đơn.

Thay vì thân hàm đặt trong cặp `{..}` hoặc `..xong` thì ta chỉ cần thay bằng dấu bằng `=` và
theo sau là một biểu thức làm kết quả trả về.

```js
hàm cộng(a, b) = a + b
hàm luỹThừa(a, mũ) = a ^ mũ

in cộng(4, 5)       // 9
in luỹThừa(2, 8)    // 256
```

### Gọi hàm theo ngữ nghĩa (literally)

Thay vì sử dụng cặp ngoặc tròn và truyền tham số vào, có thể sử dụng từ khóa để gọi hàm.

Cú pháp như sau:
```
gọi <tên_hàm> [với <các_tham_số>]
đi <tên_hàm> [với <các_tham_số>]
```

Có hai từ khóa `gọi` và `đi`, tiếp theo là tên hàm cần gọi và (nếu có) từ khóa `với`, theo sau là các tham số.

```js
hàm inRaSố50()
    in 50
xong

gọi inRaSố50
```

```js
hàm muaĐồ(tiền)
    in 'Tôi có ' + tiền + ' đồng'
    in 'Tôi mua 2 cái bánh qui'
xong

đi muaĐồ với 30000
```

```js
hàm sếpTrảLương()
    trả 1800
xong

in (gọi sếpTrảLương()) + ' đô'
```
