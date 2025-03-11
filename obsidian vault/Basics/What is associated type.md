The ==associated type== in Swift provides us with a placeholder name (designation) to be used as part of the protocol. When inheriting from the protocol, the actual type will be specified. The ==associated type== makes the protocol generic by providing a placeholder.
````swift
protocol Container {
    associatedtype Item // Определение ассоциированного типа
    
    mutating func append(_ item: Item)
    var count: Int { get }
    subscript(i: Int) -> Item { get }
}

struct IntStack: Container {
    // конкретная реализация ассоциированного типа Item как Int
    typealias Item = Int

    // реализация требований протокола
    var items = [Item]()
    mutating func append(_ item: Item) {
        items.append(item)
    }
    var count: Int {
        return items.count
    }
    subscript(i: Int) -> Item {
        return items[i]
    }
}
```
````
