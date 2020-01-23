---
layout: default
title: Rẽ nhánh và vòng lặp
nav_order: 5
---

# Rẽ nhánh và vòng lặp
{: .no_toc }

## Mục lục
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## Câu điều kiện

### Nếu..thì (đơn)

Cú pháp:
```js
nếu <điều_kiện> thì <làm_gì_dó>
```

Đúng như nghĩa của nó, nếu điều kiện đúng thì sẽ thực hiện một lệnh sau từ khóa `thì`.

Ví dụ:
```js
nếu đúng thì in đúng 	// đúng
nếu sai thì in 'sao được'
```

### Nếu..thì..thôi

Cú pháp:
```js
nếu <đều_kiện> thì
    <làm_cái_này>
    <làn_cái_kia>
thôi
```

Tương tự như nếu..thì ở trên, nhưng ở đây có thể thực hiện nhiều lệnh hơn nếu điều kiện đúng.
Các lệnh phải xuống dòng sau từ khóa `thì`, và sử dụng từ khóa `thôi` hoặc `xong` để kết thúc.

Ví dụ:
```js
nếu 4<5 thì
    in 'bốn bé hơn năm'
    in 'đúng mà'
thôi

nếu 12 + 3 > 6 thì
    in 'Okê'
xong
```

### Nếu..hay..thì

Cú pháp:
```js
nếu <điều_kiện> thì
    <làm_1>
hay
    <làm_2>
thôi
```

Thêm từ khóa `hay` vào để nối tiếp câu lệnh `nếu` phía trước. Lệnh trước sai sẽ thực hiện lệnh còn lại trong câu lệnh `hay`.

Ví dụ:
```js
nếu sai thì
    in sai
hay nếu 4>5 thì
    in 'chắc chắn sai'
hay 
    in 'hay'		// => hay
thôi
```

## Vòng lặp

### Khi..thì

Cũng giống như nếu..thì, nhưng ở đây sẽ thực hiện câu lệnh mãi cho đến khi điều sai thì dừng lại.

Cú pháp:
```js
khi đúng thì in 'vô tận'
khi sai thì in 'không thể nào'

biến a = 0
khi a < 10 thì
    in a
    a = a + 1
xong
```

### Thoát vòng lặp

Để thoát khỏi vòng lặp, ta sử dụng từ khóa `dừng`.

Ví dụ:
```js
khi đúng thì dừng

biến a = 0
khi đúng thì
    a = a + 1
    nếu a > 10 thì dừng
xong
```
