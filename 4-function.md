## Function trong Golang
### 1. Định nghĩa
Function là một tập hợp các dòng code thực hiện một công việc nhất định. 

Function tiếp nhận đầu vào, sau đó thực hiện một vài tính toán và trả về kết quả đầu ra.

### 2. Khởi tạo function
#### Cú pháp
```golang
func functionname(parametername type) returntype {  
    //function body
}
```

> **parametername**, **returntype** là các giá trị tùy chọn của function

### Các ví dụ về fuction
#### 1. Function không có tham số và không trả về giá trị
```golang
func sayHello() {  
    fmt.Println("Xin chào các bạn")
}
```

### 2. Function không có tham số và trả về giá trị
```golang
func sayHello() string{  
    mess := "Xin chào các bạn"
    return mess
}
```

### 3. Function có tham và không trả về giá trị
```golang
func sayHello(name string) {  
    fmt.Println("Xin chào", name)
}
```

### 4. Function có tham và trả về giá trị
```golang
func sum(a,b int) int{  
    return a + b
}
```

### 5. Function trả về nhiều giá trị
```golang
func calculate(a, b int) (int,int) {
	var add = a + b
	var plus = a * b
	return add,plus
}
```

Các giá trị trả về được đặt tên
```golang
func calculate(a,b int) (add, plus int){
    add = a + b
    plus = a * b
    return
}
```

### 6. Định dang trống
"_" được hiểu là định danh trống trong Go

Loại bỏ giá trị không được sử dụng

```golang
func calculate(a,b int) (add, plus int){
    add = a + b
    plus = a * b
    return
}

func main() {
	_, plus := calculate(3, 4)
	fmt.Println(plus)

}
```
