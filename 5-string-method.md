## Package strings golang

### In thường, in hoa chữ
```golang
ss := "Sammy Shark"

fmt.Println(strings.ToUpper(ss)) // In hoa
fmt.Println(strings.ToLower(ss)) // In thường
```

### String Search Functions
String package có một số hàm giúp xác định xem một chuỗi có chứa một chuỗi ký tự cụ thể hay không.

#### 1. strings.HasPrefix
- Kiểm tra xem chuỗi có được bắt đầu bằng 1 chuỗi chỉ định hay không?
- Trả về : true / false
```golang
ss := "Sammy Shark"
fmt.Println(strings.HasPrefix(ss, "Sammy")) // true
fmt.Println(strings.HasPrefix(ss, "Abc")) // false
```

#### 2. strings.HasSuffix
- Kiểm tra xem chuỗi có được bắt đầu bằng 1 chuỗi chỉ định hay không?
- Trả về : true / false
```golang
ss := "Sammy Shark"
fmt.Println(strings.HasSuffix(ss, "Shark")) // true
fmt.Println(strings.HasSuffix(ss, "Abc")) // false
```

#### 3. strings.Contains
- Kiểm tra xem chuỗi có chứa chuỗi chỉ định hay không?
- Trả về : true / false
```golang
ss := "Sammy Shark"
fmt.Println(strings.Contains(ss, "Sh"))) // true
fmt.Println(strings.Contains(ss, "Sv")) // false
```

#### 4. strings.Count
- Đếm số lần xuất hiện của 1 chuỗi chỉ định
- Trả về : số lần xuất hiện
```golang
ss := "Sammy Shark"
fmt.Println(strings.Count(ss, "S")) // 2
```

### Xác định độ dài của chuỗi
- Hàm **len()** trả về độ dài của 1 chuỗi
```golang
openSource := "Sammy contributes to open source."
fmt.Println(len(openSource)) // 33
```

### Function thao tác với chuỗi
#### 1. string.Join
Hàm **string.Join** rất hữu ích để kết hợp **slice string** thành một **string mới**.
```golang
fmt.Println(strings.Join([]string{"sharks", "crustaceans", "plankton"}, ",")) // sharks,crustaceans,plankton
```