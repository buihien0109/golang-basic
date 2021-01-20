Bài 1. Viết function kiểm tra 1 chuỗi có nằm trong chuỗi còn lại hay không
- Ví dụ: checkStringExist("i love you", "you") => true
- Ví dụ: checkStringExist("i love you", "hate") => false

```golang
package main

import (
	"fmt"
	"strings"
)

func checkStringExist(strC, strP string) bool {
	return strings.Contains(strC, strP)
}

func main() {
	fmt.Println(checkStringExist("i love you", "you"))
	fmt.Println(checkStringExist("i love you", "yoau"))
}
```


Bài 2. Viết function rút ngắn chuỗi bằng cách cắt ra 8 ký tự đầu của 1 chuỗi và thêm dấu ba chấm ở cuối chuỗi.
- Ví dụ: shortenString('Xin chào các bạn') => 'Xin chào...'
- Ví dụ: shortenString('Hello') => 'Hello'
```golang
package main

import (
	"fmt"
	"strings"
)

func shortenString(str string) string {
	if len(str) > 8 {
        sliceString := strings.Split(str,"")
        subString := sliceString[:8]
		return strings.Join(subString, "")
	} else {
		return str
	}
}

func main() {
	fmt.Println(shortenString("Xin"))
	fmt.Println(shortenString("Xin chào các bạn"))
}

```


Bài 3. Viết function có tác dụng biến 1 chuỗi thành chuỗi chỉ viết hoa từ đầu tiên.
- Ví dụ: capitalizeString('chÀo MừnG đẾn với techMaster') => 'Chào Mừng Đến Với Techmaster'
```golang
package main

import (
	"fmt"
	"strings"
)

func capitalizeString(str string) string {
	return strings.Title(str)
}

func main() {
	fmt.Println(capitalizeString("Xin"))
	fmt.Println(capitalizeString("Xin chào các bạn"))
}
```


Bài 4. Cho 1 chuỗi và 1 số nguyên n > 1, hãy viết function có tác dụng sao chép đó chuỗi lên n lần, ngăn cách nhau bởi dấu gạch ngang.
- Ví dụ: repeatString('a', 5) => 'a-a-a-a-a'
```golang
package main

import (
	"fmt"
)

func repeatString(str string) string {
	var newStr string
	for i := 0; i < 10; i++ {
		newStr += str
	}
	return newStr
}

func main() {
	fmt.Println(repeatString("hi"))
	fmt.Println(repeatString("a"))
}
```


Bài 5. Viết function với đầu vào là 1 chuỗi string. Trả về chuỗi đảo ngược của chuỗi đó
- Ví dụ: reverseString('Hello') => 'olleH'
```golang

```

Bài 6. Cho 1 chuỗi, kiểm tra xem chuỗi đó có phải chuỗi đối xứng hay không (đọc xuôi hay ngược đều như nhau, không tính khoảng trắng, không phân biệt hoa thường),
- Ví dụ: checkSymmetricString("Race car") => true
- Ví dụ: checkSymmetricString("hello world") => false



Bài 7. Viết một function nhận vào string, trả về số lượng nguyên âm có trong string

Nguyên âm:  a, o, e, u, i.

- Ví dụ: countNumberVowels("hello") => 2
- Ví dụ: countNumberVowels("hello hien") => 4



Bài 8. Viết function kiểm tra xem một chuỗi có kết thúc bằng chuỗi khác hay không.
- Ví dụ : confirmEnding("hello", "lo") => true
- Ví dụ : confirmEnding("hello", "ll") => false



Bài 9. Viết function lấy ra những chữ cái đầu của từng từ trong chuỗi, các chữ cái đầu được phân tách với nhau bằng dấu cách
- Ví dụ : getFirstLetter("xin chào các bạn") => "x c c b"
- Ví dụ : getFirstLetter("hello world") => "h c"



Bài 10. Viết function nhập vào 1 chuỗi bất kỳ. Sắp xếp các ký tự trong chuỗi theo chiều tăng dần của bảng chữ cái (có phân biệt chữ hoa, chữ thường). Yêu cầu loại bỏ khoảng trắng trong chuỗi trước khi sắp xếp
- Ví dụ : sortLetters("hello world") => "dehllloorw"
- Ví dụ : sortLetters("HellO WorLd") => "HLOWdellor"



Bài 11. Viết function nhập vào 1 chuỗi bất kỳ. Tìm ra ký tự không bị lặp lại trong chuỗi (không tính khoảng trắng)
- Ví dụ : getLetterNoRepeat("abc abce") => "e";
- Ví dụ : getLetterNoRepeat("abce abcdf") => "e,d,f";
- Ví dụ : getLetterNoRepeat("abab") => "";