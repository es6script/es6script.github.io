---
layout: post
title: "ES6 Block Scoped - Khởi tạo và sử dụng biến let"
date: 2016-11-05 14:30:00
categories: huongph
featured_image: /images/corver.jpg
---



Chúng ta thường sử dụng var để khai báo biến, trong ES6 cũng vậy nhưng có thêm let.
Vậy `let` với `var` khác nhau chỗ nào.

var khi khái báo thì nó có hai dạng , toàn cục và cục bộ. 

## Ready???

Ví dụ :

``` js

var h = 'noname'; // Đây la biến toàn cục
function name(){
	var n = 'huongph'; // đây là biến cục bộ 
}

```

Còn với `let` thì phạm vi nó nhỏ hơn, nó chỉ tồn tại trong khối khai báo. Còn gọi là phạm vi Block scoped. Cho nên ta chú ý với những trường hợp nào mà sử dụng. 

## Block Scoped là gì?

Block Scoped là phạm vi trong một khối, nghĩa là chỉ hoạt động trong phạm vi được khai báo bời cặp {}.

Ví dụ : 

``` js
if(1 === 1){
	if(0 === 0){
		var a = ["a", "b", "c"];

		a.forEach(function(element) {
		    console.log(element);
		});
	}
}

```

Ở ví dụ trên ta thấy nè : 

if 1 là một block , if 2 cũng là một block, và forEach cũng là một block.

Vậy Block Scoped là phạm vi chứa tất cả những đoạn code nằm bên trong cặp thẻ {}.

OK vậy sử dụng `let` ở đâu phù hợp và ở đâu là lỗi.

Ví dụ : 

``` js
if(1 === 1){
	let n = 'huongph';
	var m = 'me';
}

console.log(m); // print me
console.log(n); // Lỗi biến không tồn tại

```

Qua ví dụ đó ta thấy cách hoạt động của `let` và `var` như thế nào.

## Vậy khi nào nên sử dụng let để khai báo biến

Đó là khi ta sử dụng biến tạm (tmp) trong function đó mấy chế. 

Xong, phần sau tôi sẽ chia sẻ tiếp về * Arrow Function trong ES6 *


