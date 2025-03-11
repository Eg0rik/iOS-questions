- inout используется для передачи параметров по ссылке. 
- Изменения, сделанные внутри функции, отражаются на оригинальной переменной.

```swift 
func doubleInPlace(number: inout Int) {
    number *= 2
}

var myNum = 10 
doubleInPlace(number: &myNum)
```
