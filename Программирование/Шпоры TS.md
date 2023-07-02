TypeScript поддерживает множество типов данных, включая:

- string (строковый тип данных);
- number (числовой тип данных);
- boolean (булевый тип данных);
- object (объектный тип данных);
- array (массивный тип данных);
- tuple (кортежный тип данных);
- enum (перечисляемый тип данных);
- any (любой тип данных);
- void (отсутствие типа данных);
- null (ничего или отсутствие значения);
- undefined (неопределенный тип данных);
- never (тип данных, который никогда не должен возникать).
1. **Что такое TypeScript и зачем он используется?** TypeScript - это язык программирования, разработанный Microsoft. Это строго типизированное надмножество JavaScript, которое добавляет статическую типизацию и объектно-ориентированные паттерны.
    
2. **Какие основные отличия между TypeScript и JavaScript?** TypeScript предоставляет статическую типизацию, интерфейсы и классы. В то время как JavaScript - динамически типизированный язык и не поддерживает статическую типизацию.
    
3. **Что такое файл объявления в TypeScript и для чего он используется?** Файлы объявлений используются, чтобы помочь TypeScript понять формат библиотек, написанных на JavaScript. Они обычно имеют расширение .d.ts.
    
4. **Что такое тип `any` в TypeScript?** Тип `any` в TypeScript позволяет переменной принимать любой тип данных. Это полезно, когда тип данных неизвестен или может быть разным.
    
    typescriptCopy code
    
    `let variable: any = 'Hello'; variable = 42;  // Это допустимо, поскольку variable имеет тип any`
    
5. **Как работают `interface` в TypeScript?** Интерфейсы в TypeScript используются для определения специфического формата объекта. Они не переводятся в JavaScript и используются только для проверки типов во время компиляции.
    
    typescriptCopy code
    
    `interface Person {   firstName: string;   lastName: string; }`
    
6. **Что такое `enum` в TypeScript и как его использовать?** `enum` в TypeScript используется для определения набора именованных констант. `enum` может сделать код более читаемым и менее подверженным ошибкам.
    
    typescriptCopy code
    
    `enum Color {   Red,   Green,   Blue } let c: Color = Color.Green;`
    
7. **Что такое `union` и `intersection` типы в TypeScript?** `Union` типы позволяют объявить переменную, которая может содержать один из нескольких типов данных. `Intersection` типы используются для комбинирования нескольких типов в один.
    
    typescriptCopy code
    
    `type StringOrNumber = string | number;  // Union type NameAndId = { name: string } & { id: number };  // Intersection`
    
8. **Как TypeScript обрабатывает `null` и `undefined`?** По умолчанию `null` и `undefined` могут быть присвоены любому типу в TypeScript. Однако, если включена опция компилятора `strictNullChecks`, то `null` и `undefined` могут быть присвоены только к типам `null` и `undefined` соответственно.
    
9. **Что такое `generics` в TypeScript?** `Generics` в TypeScript позволяют создавать обобщенные функции, классы и интерфейсы. `Generics` улучшают повторное использование кода и гарантируют тип безопасности.
    
    typescriptCopy code
    
    `function identity<T>(arg: T): T {    return arg; }`
    
10. **Что такое декораторы в TypeScript?** Декораторы представляют собой специальный тип объявления, который может быть прикреплен к объявлению класса, метода, аксессора, свойства или параметра. Декораторы используют синтаксис `@expression`.
    
11. **Что такое Tuple в TypeScript?** `Tuple` позволяет указать тип каждого элемента массива. Это полезно, когда массив представляет собой совокупность различных типов.
    
    typescriptCopy code
    
    `let x: [string, number]; x = ["hello", 10]; // OK`
    
12. **Как можно привести типы в TypeScript?** Приведение типов можно сделать с использованием угловых скобок или оператора `as`.
    
    typescriptCopy code
    
    `let someValue: any = "this is a string"; let strLength: number = (<string>someValue).length; // или let strLength: number = (someValue as string).length;`
    
13. **Что такое модули в TypeScript?** Модули используются для организации и инкапсуляции кода. Модули в TypeScript можно импортировать и экспортировать с использованием ключевых слов `import` и `export`.
    
    typescriptCopy code
    
    `// someModule.ts export const someValue = 42; // someOtherModule.ts import { someValue } from './someModule';`
    
14. **Что такое наследование в TypeScript?** Наследование - это ключевой принцип объектно-ориентированного программирования, который TypeScript поддерживает с использованием ключевых слов `extends` и `super`.
    
    typescriptCopy code
    
    ``class Animal {   move(distanceInMeters: number = 0) {     console.log(`Animal moved ${distanceInMeters}m.`);   } }  class Dog extends Animal {   bark() {     console.log('Woof! Woof!');   } }``
    
15. **Что такое `ReadonlyArray<T>` в TypeScript?** `ReadonlyArray<T>` - это массив, который нельзя изменить после его создания. Это полезно для предотвращения мутаций в массиве.
    
    typescriptCopy code
    
    `let a: ReadonlyArray<number> = [1, 2, 3, 4];`
    
16. **Что такое `namespace` в TypeScript?** `namespace` используются для группировки кода и избегания конфликтов имен. `namespace` может содержать классы, функции, переменные и другие `namespace`.
    
17. **Что такое Promise в TypeScript?** Promise в TypeScript представляет собой объект, используемый для асинхронного вычисления. Promise может быть в трех состояниях: pending, fulfilled и rejected.
    
    typescriptCopy code
    
    `const promise = new Promise<string>((resolve, reject) => {   setTimeout(() => {     resolve("Promise resolved")   }, 2000) });`
    
18. **Как вы обрабатываете ошибки в TypeScript?** Обработка ошибок в TypeScript обычно выполняется с использованием блоков `try/catch`. Также можно использовать `.catch()` метод с Promise.
    
19. **Что такое Map и Set в TypeScript?** `Map` и `Set` - это новые структуры данных в ES6, которые также поддерживаются в TypeScript. `Map` - это коллекция ключ/значение, а `Set` - это коллекция уникальных элементов.
    
20. **Что такое деструктуризация в TypeScript?** Деструктуризация - это ES6-функция, которую TypeScript поддерживает. Он позволяет извлекать данные из массивов или объектов с использованием синтаксиса, который зеркалирует конструкцию массивов и объектов.
    
    typescriptCopy code
    
    `let { a, b }: { a: string, b: number } = { a: "baz", b: 101 };`