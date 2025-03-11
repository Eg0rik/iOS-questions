```swift 
// 1. в цикле
for number in numbers where number % 2 == 0 {
    print(number)  // Выведет: 2, 4, 6, 8, 10
}

// 2. в switch с enum
switch myDevice {
case .iPhone(let model, let year) where year > 2020:
    print("Современный iPhone: \(model)")
case .iPhone(let model, _):
    print("Старый iPhone: \(model)")
case .iPad(let model, let year) where year > 2020:
    print("Современный iPad: \(model)")
case .iPad(let model, _):
    print("Старый iPad: \(model)")
}

// 3. в extension
extension Array where Element: Numeric {
    func sum() -> Element {
        return self.reduce(0, +)
    }
}

// 4. в методе с generic
func findFirstMatch<T: Sequence>(in array: T, value: T.Element) -> T.Element? where T.Element: Equatable {
    for element in array where element == value {
        return element
    }
    return nil
}
```