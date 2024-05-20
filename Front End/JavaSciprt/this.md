#2024-05-20 #2024-05  #2024 [[2024-05-20 회사]]

## 한 줄 요약 : 함수의 실행 문맥을 나타내는 키워드

---
## **this** 키워드 사용하기
함수 내부에서의 예제
```js
function sayHello() {
    console.log("Hello, " + this.name + "!")
}
 
var person = {
    name: "이지민",
    sayHello: sayHello
};
var person2 = {
    name: "리짜이밍",
    sayHello: sayHello
};
person.sayHello();
person2.sayHello();

//Hello, 이지민!
//Hello, 리짜이밍!
```


## 객체에서 메소드를 호출할때 예제
```js
var car = {
    make: "HYUNDAI",
    model: "ionic",
    year: "2024",
    getCarInfo: function() {
    return this.make + " " + this.model + " (" + this.year + ")";
    }
};
console.log(car.getCarInfo()); 
//HYUNDAI ionic (2024)
```

## **this** 사용시 주의 사항

- **this**를 사용하는 <font color="#ff0000">함수</font>를 <font color="#4f81bd">객체</font>의 메서드로 사용시 **this**가 해당 <font color="#4f81bd">객체</font>를 참조하는지 확인
- 중첩된 <font color="#ff0000">함수</font> 내부에서 **this**를 사용시 중첩된 <font color="#ff0000">함수</font> 내부에서 **this** 재사용 시 **this** 값 변경 가능성 있음
- call, apply, bind 와 같은 메서드를 통해 **this** 변경 가능 사용시 **this** 값 올바르게 선언