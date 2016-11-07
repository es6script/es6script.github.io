---
layout: post
title: "ES6 Arrow Function - Sử dụng arrow function trong es6"
date: 2016-11-07 8:30:00
categories: huongph
featured_image: /images/corver.jpg
---

Như chúng ta đã biết để khai báo function thì có nhiều cách 

Ví dụ : 

``` js

var fun1 = function(var1, var2){
	
}
// hoặc

function fun2(var1, var2){
	
}

```

## Sử dụng Arrow function trong ES6

Nếu sử dụng trong es6 thì cú pháp căn bản sẽ là như thế này

``` js

var fun3 = (var1, var2) => {
    // Code here
};

```
## Ví dụ cụ thể nha

Bình thường chúng ta viết

``` js

var a = [
  "NguyenTung",
  "NGocDuong",
  "NGocAN",
  "ThanhDuy",
  'NgocTho'
];

var a2 = a.map(function(s){ return s.length });

console.log(a2); //[10, 9, 6, 8, 7]

```

Bây giờ es6 viết

``` js

var a = [
  "NguyenTung",
  "NGocDuong",
  "NGocAN",
  "ThanhDuy",
  'NgocTho'
];

var a3 = a.map( s => s.length );

console.log(a3); //[10, 9, 6, 8, 7]

```
Các bạn đã thấy khác nhau gì chưa ... Nhanh , gọn...???

## Tiếp 

Bình thường chúng ta viết

``` js
// ex1

function tungns(name){
  console.log('Hello '+ name); 
}

tungns("Song"); //Hello Song


//ex2

function Person() {

  this.age = 0;

  setInterval(function growUp() {

    this.age++;
  }, 1000);
}

var p = new Person();


```

Bây giờ es6 viết

``` js
//ex1
var tungns1 = (name) => console.log('Hello '+ name);
tungns1('hihi'); //Hello hihi

//ex2

function Person(){
  this.age = 0;

  setInterval(() => {
    this.age++; // |this| properly refers to the person object
  }, 1000);
}

var p = new Person();
```
Kết luận : Mình thấy chẳng mạnh gì so với khai báo truyền thống, chỉ gọn hơn thôi. 
ok nhé còn nhiều ví dụ các bạn có thể học thêm [Tai day](https://developer.mozilla.org/vi/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
