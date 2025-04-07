#### 1. Reference vs. Value Types:
- Class - ссылочный тип (передается по ссылке)
- Struct - тип значение (передается копированием)
#### 2. Mutability
- Class: можно изменять свойства, если переменная Class помечена ==let==
- Struct:  нельзя изменять свойства, если переменная Struct помечена ==let==
#### 3. Inheritance
У Struct нет наследования, в отличии от Class
#### 4. Init
- Struct: есть по умол. реализованный init для всех свойств
- Class: есть ==convenience==, ==required== init
#### 5. Memory
- Class: хранится в куче(Heap) управляются ==ARC== 
- Struct: хранится в Stack