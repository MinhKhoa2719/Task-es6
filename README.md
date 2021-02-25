# Task-es6
# Với ES6
 + Không dùng var
 + Sử dụng let thay vì var
 + Dùng const để định nghĩa hằng số
## Các chức năng mới của ES6
### Một trong những tính năng nổi bật của ES6 đó là sự bổ sung let và const phục vụ cho việc khai báo biến dữ liệu.	
+ Arrow function: Bạn có thể tạo hàm bằng cách sử dụng dấu mũi tên =>.(Arrow là một dạng viết tắt của các function sử dụng dấu =>, tương tự như trong C#, Java 8,…)
+ Block Scoped: Định nghĩa biến với từ khóa let, cách định nghĩa này thì biến chỉ tồn tại trong phạm vi khối của nó (Block Scope)
+ Destructuring Assignments: Bạn có thể khởi tạo các biến từ một mảng bằng một dòng code đơn giản.
+ Default Parameters: Bạn có thể gán giá trị mặc định cho các tham số.
+ Template String: Tạo templaet HTML cực kì đơn giản
Weak, Set: các kiểu dữ liệu phức tạp mới
Để sửa chữa khi bạn sử dụng $(this) sẽ thay bằng $(e.currentTarget)

## 1_Let và Var
+ let cho phép chúng ta cập nhật giá trị của biến (không cho phép chúng ta tái khái báo lại biến đó).
### -Giống nhau:
+ Đều dùng để khai báo biến trong js
### -Khác nhau:
+ Phạm vi của biến số sử dụng var là phạm vi hàm số hoặc bên ngoài hàm số, toàn cục.	
+ Phạm vi của biến số sử dụng let là phạm vi một khối, xác định bởi cặp {}
## 2_Arrow Function 
### Function (hàm, chức năng), gọi chung là subprogram (chương trình con) có thể được gọi ở bên ngoài hoặc bên trong chính nó.
+ Arrow Function (hay còn gọi là hàm mũi tên) là một trong những tính năng mới và rất hay của ES6. Nó thừa hưởng cách viết ngắn gọn bằng cú pháp ES6. Tuy Arrow Function và Function đều là function, nhưng cách viết và cách tham chiếu tới bối cảnh (context) khác nhau
### *Sự khác nhau ở cú pháp
### Arrow Function sử dụng kí tự =>
hello = () => {
console.log('hello')
}
// hello()

### Còn Function thông thường thì :

function hello(){
console.log('hello')
}
// hello()

### Với TH có tham số :

hello = name => {
console.log('hello ', name)
}

### Ta có thể giản lược được dấu () với trường hợp có 1 tham số truyền vào.
+ Ngoài ra, với arrow function ta có thể bỏ qua từ khoá return
double = x => x * 2

+ Còn với function thì :
function double(x){
return x * 2
}

### Ngoài ra, ta còn sử dụng được arrow function trong trường hợp: map, filter, forEach,...
+ Ví dụ:D

const numbers = [1,2,3,4]
const newArray = numbers.map(item => item * 2 )
// console.log(newArray)

+ Trông có vẻ tối giản code so với:

const numbers = [1,2,3,4]
const newArray = numbers.map(function(item){
return item => item * 2
})
*// console.log(newArray)

+ ES6 Bạn có thể tạo hàm bằng cách sử dụng dấu mũi tên =>.(Arrow là một dạng viết tắt của các function sử dụng dấu =>,

## 3_Class
+ Ví dụ giả sử bây giờ chúng ta đang làm một ứng dụng quản lý dự án, đương nhiên class đầu tiên chúng ta cần đó là Project ?. Vậy làm sao khai báo class Project đó ra mà xài đây?
+ Vậy nên ta có thể định nghĩa class Project của ta theo cách này để xài như sau:

class Project {
    *// Một tí code ở đây
}
+ Đây cũng là cách hay được sử dụng nhất. Và khi ta muốn tạo một instance thì vẫn như các ngôn ngữ khác:
    const project = new Project()
### Xong.
+ Class expressions
 chúng ta có thêm một cách nữa để khai báo class Project của chúng ta, class expressions:

const Project = class {
    // Một tí code nữa cũng ở đây
}
+ Nhưng, bên trong cách này lại có một kiểu ghi nữa***, giả sử ta gán vào biến tên Project nhưng lại muốn tên của class phải là MyProject cơ, thế thì làm như sau:

const Project = class MyProject {
    // Một tí code nữa cũng ở đây
}

+ Có vẻ khác, khi định nghĩa class theo kiểu expressions như thế này, chúng ta có thể đặt tên cho class (ví dụ dưới) hoặc có thể không (ví dụ trên) đều được. Và chúng ta có thể xem tên class là tên gì bằng cách :
### console.log(ClassName.name)
+ Khi tạo instance thì chúng ta sẽ new biến mà chúng ta gán class vào (kể cả chúng ta có đặt tên cho class thì vẫn sử dụng biến chúng ta gán vào )
    const project = new Project()
### LƯU Ý:
+ Đối với class thì sẽ không có khái niệm hoisting (Hoisting là hành vi mặc định của JavaScript về việc di chuyển các khai báo lên đầu để compiled hay thực thi code của bạn.) như function, cho nên chúng ta bắt buộc phải định nghĩa class của chúng ta trước rồi sau đó mới có thể sử dụng.

*// 1. Nên*
class Project {
   *// code ở đây*
}

const project = new Project()
*// 2. Không nên*
const project = new Project()

class Project {
    *// code ở đây*
}


+ Javascript chúng ta sẽ được tặng hẳn 1 hàm riêng đó là constructor() luôn. 
+ Thế nên, class Project của chúng ta sẽ được viết như sau:

class Project {
    constructor () {
        *// viết vô cái gì đó *
   }
}

### Lưu ý rằng : một class chỉ có 1 constructor()



## 4_spread operator
+ Khái niệm : được viết là ...). Spread operator là một cách rất hữu dụng và ngắn gọn để dùng trong các thao tác với mảng như thêm phần tử vào mảng,
kết hợp mảng (hoặc object), truyền tham số mảng vào function
+ Spread operator được thêm vào từ phiên bản ES6 (ES2015), cũng như rest parameter, 
2 loại operator này giống nhau về mặt cú pháp, đó là cùng sử dụng dấu ....
# *Ví dụ cơ bản nhất, đó là hàm tìm số lớn nhất trong mảng như sau :

Math.max(1,3,5) // output: 5
Math.max([1,3,5]) // output: NaN

+ Chương trình sẽ không hiểu mà chúng ta cần đến *...,* chỉ cần thêm dấu *...* vào phần argument, chúng ta sẽ có kết quả mong muốn

Math.max(...[1,3,5]) *// output: 5*

+ Trong trường hợp này, spread operator đã mở rộng (spread) mảng 3 phần tử thành 3 tham số riêng biệt.
### Sao chép mảng
+ Với spread operator ..., chúng ta có thể sao chép mảng một cách rất ngắn gọn, bên cạnh đó việc thêm một hay nhiều phần tử vào mảng cũng rất dễ dàng :
+ Ví dụ :

const fruits = ['🍏','🍊','🍌','🍉','🍍']
*//sao chép mảng fruits sang mảng moreFruits*
const moreFruits = [...fruits]; 
console.log(moreFruits) *// Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]*

### Thêm phần tử vào mảng
+ Như đã đề cập ở trên đây, spread operator còn có thể thêm một hay nhiều phần tử vào mảng, giúp cho đoạn code của chúng ta đơn giản và 
tự nhiên hơn rất nhiều so với cách viết code truyền thống như trước đây :

const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit] *//thêm các phần tử của mảng fewFruit vào mảng fewMoreFruit*
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]

### Kết hợp 2 hay nhiều object với nhau
+ Spread operator ngoài có thể thao tác với mảng thì còn có thể thao tác với các object. Chúng ta có thể sử dụng spread operator để kết hợp các thuộc tính, 
các phương thức của 2 hay nhiều object lại thành một object mới. Sau đây là ví dụ :

const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}

 *// Kết hợp objectOne, objectTwo lại trong objectThree và thêm thuộc tính laugh*
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) *// Object { hello: "🤪", world: "🐻", laugh: "😂" }

*// Tương tự chúng ta có objectFour, với laugh là một hàm*
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() *// 😂😂😂😂😂


## 5_Destructuring Assignment 
+ Khái niêm : là một cú pháp cho phép tách dữ liệu được lưu trữ bên trong (nested) Objects hoặc Arrays (tổng quát hơn là các iterable values) và 
gán chúng cho các biến riêng biệt.
+ Chúng ta cũng có thể sử dụng Array Destructuring với các toán tử như Spread nếu cần thiết. Dưới đây là một số ví dụ minh họa:

### Strings
let message = 'Hello';
let [a, b] = message;
let [x, y, ...z] = message;

console.log(a, b);    *// H e*
console.log(x, y, z); *// H e ['l', 'l', 'o']*

### Arrays
let numbers = [101, 102, 103];
let [x, y, z] = numbers;

console.log(x, y, z); *// 101 102 103*
Sets
let set = new Set().add('foo').add('bar');
let [a, b] = set;

console.log(a, b); *// foo bar*
Maps
let map = new Map().set('a', 1).set('b', 2);
let [x, y] = map;

console.log(x, y); *// ["a", 1] ["b", 2]*

## 6_Import và Export trong JS
+ Import: Cho phép import các functionality từ các module khác. 
+ Export: Khai báo những variables hoặc function cho phép những module khác truy cập và sử dụng
### Có 2 loại export đó là named và default:
+ named export được sử dụng để xuất nhiều thứ từ một module bằng cách thêm keyword export vào khai báo của chúng. Những thứ được export sẽ được phân biệt bằng tên. 
Sau đó import những thứ chúng ta cần sử dụng bằng cách bao quanh chúng cặp dấu ngoặc nhọn { }. Tên của module đã nhập phải giống với tên của module đã xuất.

*//-------util.js------*
export function addTwoNumbers(x,y){
  return x + y
}
export let students = ['wisdom','bill','fred','grim']

### Note: Không thể export khi không định nghĩa tên:

export 'value';
import { };
Default Export:

+ Trong Javascript ES6 chỉ cho phép xuất một mặc định cho mỗi file. Default Export có thể cho một function, class hoặc một object.

*//----myFunction.js ----*
export default function () {
  alert("Hello Default Export")
}
### Note: Không thể export khi định nghĩa tên:

export default const name = 'value';
Default + Named export:

+ Bạn có thể cùng lúc sử dụng default export và named export trong 1 file

export const name1 = 'value1';
export const name2 = 'value2';
export default 'value2';

import anyName, { name1, name2 } from '/modules/my-module.js';
console.log(anyName); *// 'value2'*
console.log(name); *// 'value1'*
### Đổi tên Export
+ Nếu không thích tên được export, bạn có thể đổi tên nó bằng cách sử dụng từ khóa as
const name = 'value';
export { name as newName };

import { newName } from '/modules/my-module.js';
console.log(newName); *// 'value'*
*// Tên gốc (name) không còn truy cập được*
console.log(name); *// undefined*
### 2. Import
+ Để import một module vào một script thì bạn có thể sử dụng import. Ví dụ chúng ta có những module dùng named export thì bạn có thể import như thế này.
*//----main.js---*
import { addTwoNumbers, students } from 'util';
Importing with alias:
import * as util from 'util';

console.log(util.addTwoNumbers(2,13))
console.log(util.students)
Ngoài ra bạn cũng có thể sử dụng alias "as" để định danh lại nếu chưa quen thuộc hoặc tuỳ theo dự án của mình:
import {sayHi as hi, sayBye as bye} from './say.js';

## 7_Array trong JS

+Đối tượng Array trong JavaScript là đối tượng toàn cục được dùng để xây dựng nên các mảng; là những đối tượng cấp cao và giống một dạng danh sách.
### “” Có nhiều phương thức liên quan đến mảng””


## 8_FOR IN…FOR IF TRONG JAVASCRIPT
### For ... in \
+Được sử dụng để được sử dụng để lặp lại trên tất cả các enumerable properties của một Object, bao gồm enumerable properties được kế thừa. Câu lệnh lặp này có thể được sử dụng với String, Array, or những object đơn giản, nhưng không phải với các object như Map() hoặc Set().

for (let prop in ['a', 'b', 'c']) 
  console.log(prop);           * // 0, 1, 2 (array indexes)*

for (let prop in 'str') 
  console.log(prop);            *// 0, 1, 2 (string indexes)*

for (let prop in {a: 1, b: 2, c: 3}) 
  console.log(prop);            *// a, b, c (object property names)*

for (let prop in new Set(['a', 'b', 'a', 'd'])) 
  console.log(prop);            *// undefined (no enumerable properties)*



### For ... of \
+ For ... of được sử dụng để lặp qua các iterable objects, lặp lại các giá trị của chúng thay vì các thuộc tính của chúng. Câu lệnh lặp này có thể được sử dụng với các Array, String, Map hoặc Set object, nhưng nó không sử dụng trên những object đơn giản. Điều này có nghĩa là nó ngược với for ... in.

## Example For ... of

for (let val of ['a', 'b', 'c']) 
  console.log(val);           * // a, b, c (array values)*

for (let val of 'str') 
  console.log(val);            *// s, t, r (string characters)*

for (let val of {a: 1, b: 2, c: 3}) 
  console.log(prop);          * // TypeError (not iterable)*

for (let val of new Set(['a', 'b', 'a', 'd'])) 
  console.log(val);          *  // a, b, d (Set values)*






