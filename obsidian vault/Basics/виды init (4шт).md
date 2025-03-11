1. обычный
2. Required init – обязательные для переопределения в подклассах.
3. Convenience init – вспомогательные, должны вызывать обычные инициализаторы текущего класса.
4. init? - могут возвращать ==nil==

```swift 
   init?(value: String) {
    if value.isEmpty { return nil }
    self.value = value
}
```