## Kiểu dữ liệu trong Golang

### 1. Kiểu bool

Bool là kiểu dữ liệu chỉ nhận 2 giá trị hoặc true hoặc false (hoặc đúng hoặc sai).

```golang
a := true //a được gán bằng true
b := false // b được gán bằng false
fmt.Println("a:", a, "b:", b) 

c := a && b // c được gán bằng a&&b 
fmt.Println("c:", c) 

d := a || b // d được gán bằng a||b
fmt.Println("d:", d) 
```
---
### 2. Kiểu dữ liệu số (numeric type)
#### Số nguyên
Các kiểu số nguyên trong Go là uint8, uint16, uint32, uint64, int8, int16, int32, int64, int. 
> **uint** tức là **unsigned int** – là kiểu số nguyên không âm

| Kiểu   | Giới hạn                                   |
|--------|--------------------------------------------|
| uint8  | 0 – 255                                    |
| uint16 | 0 – 65535                                  |
| uint32 | 0 – 4294967295                             |
| uint64 | 0 – 18446744073709551615                   |
| int8   | -128 – 127                                 |
| int16  | -32768 – 32767                             |
| int32  | -2147483648 – 2147483647                   |
| int64  | -9223372036854775808 – 9223372036854775807 |

```golang
var num3 int32 = 20132
var num4 int32 = 23244
fmt.Println("Tong 2 so num3 và num4 là:", num3 + num4)

var num5 int = 20132
var num6 int = 23244	
fmt.Println("Tong 2 so num5 và num6 là:", num5 + num6)
```

#### Số thực
Trong Go có 2 kiểu số thực là **float32** và **float64**.

Thông thường để biểu diễn số thực, bạn chỉ cần dùng **float64** là đủ.

```golang
a, b := 5.67, 8.97
fmt.Printf("Kiểu dữ liệu của a là %T và của b là %T\n", a, b)

sum := a + b
sub := a - b

fmt.Println("Tổng a và b:", sum)
fmt.Println("Hiệu a và b:", sub)
```

#### Số phức
Trong Go, có 2 kiểu số phức là **complex64** và **complex128**

- Complex64: Số phức có phần thực **float32** và phần ảo
- Complex128: Số phức có phần thực **float64** và phần ảo

```golang
c1 := complex(5, 7)
c2 := 8 + 27i

cadd := c1 + c2
fmt.Println("Tổng 2 số phức c1 và c2:", cadd)

cmul := c1 * c2
fmt.Println("Tích 2 số phức c1 và c2:", cmul)
```

#### Các kiểu dữ liệu số khác

- **byte** là tên gọi khác của **uint8**
- **rune** là tên gọi khác của **int32**

---
### Kiểu dữ kiệu chuỗi
Trong Go, chuỗi là một tập hợp các byte

```golang
first := "Bùi"
last := "Hiên"

name := first + " " + last
fmt.Println("My name is ",name)
```

---
### Ép kiểu
Ngôn ngữ Go rất nghiêm ngặt và chặt chẽ, nên chúng không cho phép tự động chuyển đổi (ép kiểu) kiểu dữ liệu.
```golang
i := 55      //int
j := 67.8    //float64
sum := i + j //int + float64 not allowed
fmt.Println(sum)
```

> Sửa lại thành
```golang
i := 55      //int
j := 67.8    //float64
sum := i + int(j) //j is được ép kiểu thành int
fmt.Println(sum)
```



