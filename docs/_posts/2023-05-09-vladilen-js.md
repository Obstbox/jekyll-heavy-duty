---
layout: post
title: Владилен Минин - JS за 6 часов
---

### массивы и объекты 

`array.indexOf(value) // index` для примитивных т.д.  
`array.findIndex(callback) //index` для объектов или более сложных условий поиска  
`array.find(callback) //value by index` аналог _findIndex()_
```js
const people = [{name: 'Елена', budget: 3500}, ...]
const person = people.find(human => human.budget === 4200)
```
`array.map(callback)` к каждому элементу массива
`array.reduce(callback, [initialValue])` выполняет _свёртку массива_ с 
сохранением промежуточного результата  

```js
// деструктуризация массива. вместо 
const name = person.name
const age  = person.age
...
const {name, age} = person
const {name, sex = 'male', age} = person // значение по умолчанию
```

в описании метода объекта слово `function` не обязательно  
`for in` __плох тем__, что проходит не только по _объекту_, но и по его
_прототипу (\_proto)_  
```js
for (let key in person) {
    if (person.hasOwnProperty(key)) {
        ... // вот так безопасно
    }
}

// или
const keys = Object.keys(person)
keys.forEach(callback(key)) {}

// или 
Object.keys.forEach(callback(key)) {}
```

__Контекст__. В _js_ можно вызывать методы у методов. В некоторых случаях
_this_ теряется (например, _function_ создает свой контекст). поэтому:  
- функция-обертка  
- метод `bind()`. грубо говоря, позволяет в __метод__ _одного_ объекта передать
  _другой_ объект. возвращает функцию. можно передавать параметы.  
- метод `call()` - суть таже, но выполнение сразу.  
- метод `apply()` - как `call()`, но принимает только 2 параметра: объект и
  массив аргуметров.  

### асинхронка
1. передача коллбеков  
2. промисы  
3. async - await  

__промисы__ позволяют избежать _callback hell_.  
`const promise = new Promise( (resolve, reject) => {} )`  
`// resolve() - основной код`  
`// reject() - когда что-то пошло не так`  

методы:  
- `.then()`
- `.catch()`
- `.finally()`  

```js
const getData = () => new Promise(resolve => resolve([
    1, 1, 2, 3, 5, 8, 13, 21
]))
getData().then( data => console.log(data))
```

`async` - `await`  и `try - catch - finally` вместо `reject()`  

### DOM

`window.prompt()`  
`window.confirm()`  
```js
const heading = document.getElementById('special-class')
console.dir(heading)    // dir VS log
heading.style.color = "red"
heading.style.textAlign = "center"  // camelCase(js) vs kebab-case(css)
```

`getElementsByClassNames()[]` и `getElementsByTagNames()[]` считаются
устаревшими и медленными. `querySelector()` вместно них (вернет _первое_ совпадение).  
```js
const heading2 = document.querySelector('h2')  
const heading3 = heading2.nextElementSibling
const h2list = document.querySelectorAll('h2')
const heading4 = h2list[1]
```
