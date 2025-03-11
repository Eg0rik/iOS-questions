1. в отличие от some можно ложить любой тип
   ![[Pasted image 20240906103846.png|200]]
2. используется в Swift 5.7+ для явного указания на использование протокола в качестве типа (экзистенциальный тип). Пример:

```swift
func printValue(value: any CustomStringConvertible) {
    print(value.description)
}
```