## Khai báo biến trong golang
### Khai báo biến một biến
```golang
var number int
```

Khi khai báo biến mà không khởi tạo giá trị thì mặc định biến đó nhận giá trị **zero value** ứng với kiểu dữ liệu của biến đó

Ví dụ
```golang
var number int
fmt.println(number) // 0
```
---
### Khai báo biến sau đó mới khởi tạo giá trị cho biến
```golang
var number int
number = 32
```

---
### Khai báo biến đồng thời khởi tạo giá trị cho biến
```golang
var number int = 32
```

---
### Khai báo biến không cần chỉ định kiểu dữ liệu
```golang
var number = 32
```
> Go có thể tự động suy ra kiểu của biến này từ giá trị khởi tạo đó

---
### Khai báo biến kiểu shorthand
```golang
var number := 32
```
> Cách này không áp dụng với biến khai báo ngoài function

> Cách khai báo nhanh được sử dụng khi có ít nhất một biến mới được khai báo phía bên trái của toán tử :=

### Khai báo biến nhiều biến
```golang
// Trường hợp 2 biến khác kiểu dữ liệu
var (
    number int
    name string
)
```

```golang
// Trường hợp 2 biến cùng kiểu dữ liệu
var number, age int
```

```golang
// Khai báo xong mới khởi tạo giá trị cho biến
var (
    number int
    name string
)
number = 23
name = "Hiên"
```
```golang
// Trường hợp 2 biến cùng kiểu dữ liệu
var number, age int
number = 23
age = 40
```
```golang
// Khai báo biến kiểu suy luận
var number = 23
var age = 40
```
```golang
// Khai báo biến nhanh
number := 23
age := 40
```


