# Các kiểu dữ liệu 
Trong js chia thành 2 kiểu dữ liệu
+ Kiểu dữ liệu nguyên thủy
+ Kiểu dữ liệu tham chiếu
## I. Kiểu dữ liệu nguyên thủy
Kiểu dữ liệu nguyên thủy là kiểu dữ liệu lưu trữ giá trị trực tiếp tại ô nhớ, thay vì tại ô nhớ đó lưu địa chỉ tham chiếu
+ **Lưu trữ trực tiếp:** Biến chứa thẳng giá trị thay vì trỏ đến một đối tượng khác.
+ **Kích thước cố định:** Tốn ít bộ nhớ và dung lượng được xác định rõ tùy theo từng kiểu
+ **Hiệu năng cao:** Thao tác tính toán trên các kiểu này diễn ra rất nhanh

### 1. Kiểu dữ liệu null
Kiểu dữ liệu null là kiểu dữ liệu mang giá trị null <br/>
Ví dụ: 
```js
let x = null;
```
### 2. Kiểu dữ liệu undefined
Kiểu dữ liệu undefined là kiểu dữ liệu có giá trị undefined. Khi một biến được khởi tạo nhưng chưa có giá trị thì biến đó mang giá trị là undefined
<br/>
Ví dụ: 
```js
let x = undefined
```

### 3. Kiểu dữ liệu number
- Kiểu dữ liệu này biểu diễn số nguyên và số thực 
<br/>
Ví du:
```js
let x = 100;
let y = 9.5;
```

- Để lấy phạm vi của kiểu dữ liệu số này sử dụng cú pháp **Number.MAX_VALUE** và **Number.MIN_VALUE** <br/>
ví dụ: 

```js
console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
console.log(Number.MIN_VALUE); // 5e-324
```

### 4. Kiểu dữ liệu NaN
+ Kiểu dữ liệu NaN (Not a Number) là một giá trị đặc biệt. Ví dụ lấy chuỗi chia cho một số <br/>
Ví dụ:
```js
console.log('a'/2); // NaN;
```

### 5. Kiểu dữ liệu chuỗi
+ Chuỗi là một kiểu dữ liệu gồm nhiều kí tự và đặt trong dấu nháy đơn hoặc dấu nháy kép
+ Chuỗi trong js là bất biến, nghĩa là chuỗi đã tạo ra thì không thể sửa đổi được nữa. Tuy nhiên có thể tạo ra một chuỗi từ chuỗi cũ bằng cách sử dụng toán tử cộng chuỗi

``` js
let str = 'JavaScript';
str = str + ' String';
```

### 6. Kiểu dữ liệu boolean
Kiểu dữ liệu mang giá trị true hoặc false

## II. Kiểu dữ liệu tham chiếu
+ Kiểu dữ liệu không lưu trực tiếp giá trị, mà lưu địa chỉ ô nhớ (vị trí) nơi dữ liệu thực sự được cất giữ 
+ Biến sẽ nằm trên bộ nhớ stack giữ địa chỉ ô nhớ, còn bộ nhớ heap cũng sẽ có địa chỉ tương ứng nhưng nó chứa giá trị đối tượng đó <br/>
ví dụ: 
``` js
const user = {
    name: "Nam",
    age: 25
}
```
Biến user có giá trị là user địa chỉ 0xABC123. Bộ nhớ heap nó có đối tượng trong ngoặc đơn và cũng nằm trên địa chỉ 0xABC123

+ Việc copy biến tham chiếu này sang biến tham chiếu khác thực chất là copy địa chỉ chung. Nên nếu thay đổi thuộc tính đối tượng này cũng sẽ làm thay đổi thuộc tính đối tượng kia.

