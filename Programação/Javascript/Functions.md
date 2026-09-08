
`function MyFunc() {}`
# Functions Callbacks 

> Passar uma função como argumento para uma função

```js
function addTwoNumbers(callback, num1, num2) {
    let sum = num1 + num2;
    callback(sum);
}

function printNum(num) {
    console.log(num);
}

addTwoNumbers(printNum, 1, 2);
```
