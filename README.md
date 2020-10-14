# 10 правил стильного кода на JS
---

## 1. Использование запятых 

**не ставьте запятые в начале строки **

 😦bad
``` js
const user = {
  name: 'Antonina'
  , surname: 'Maksimova'
  ,
} 
```

😎good
``` js
const user = {
  name: 'Antonina',
  surname: 'Maksimova',
} 
```
**в конце объектов или массивов всегда ставьте запятую **

 😦bad
``` js
const user = {
  name: 'Antonina',
  surname: 'Maksimova'
} 
```

😎good
``` js
const user = {
  name: 'Antonina',
  surname: 'Maksimova',
} 
```
---

## 2. В конце любого выражения всегда должна стоять точка с запятой.

 😦bad
``` js
function result (user) {
  if(user.firstName && user.middleName && user.lastName) {
  console.log(true)
  } else {
  console.log(false)
  }
 }

result (user)
```

😎good
``` js
function result (user) {
  if(user.firstName && user.middleName && user.lastName) {
  console.log(true);
  } else {
  console.log(false);
  }
 }

result (user);
```
---

## 3. Для того, чтобы сделать код короче, используй деструктуризацию.
 😦bad
``` js
function dogSpec(dog) {
	const tail = user.tail;
	const paws = user.paws;
	const ears = user.ears;

	return `Хвост:${user.tail} Лапы:${user.paws} Уши:${user.ears}`;
}
```

😎good
``` js
function dogSpec ({ tail, paws, ears }) {
	return `Хвост:${user.tail} Лапы:${user.paws} Уши:${user.ears}`;
}
```
---

## 4. Не используйте new  операторах приведения типов String, Number, Boolean.

 😦bad
``` js
const newString = new String('Да будет миру известно');
const newNumber = new Number(5);
const newBoolean = new Boolean(true);
```

😎good
``` js
const paragraph = String('Да будет миру известно');
const five = Number(5);
const truth = Boolean(true);
```
---

## 5. Не оставляйте лишние комментарии и методы отладки(console, debugger) в итоговой версии продукта.
 😦bad
``` js
function larges () {
  if (subm.length > 10) {
    console.log('Верно');
  } else {
    console.log('Неверно');
  }
}
debugger;
larges ();
```

😎good
``` js
function larges () {
  if (subm.length > 10) {
    console.log('Верно');
  } else {
    console.log('Неверно');
  }
}
larges ();
```
---

## 6. Для объявления переменных используй только let и const.
 **Const необходима в случае, если переменная не переназначается, в остальных  let.** Другие интерпретации могут привести к появлению глобальных переменных.

  😦bad
``` js
var name = 'Антонина Максимова, ';
age = 23;
kind1 = ', Человек';
var kind2 = ', Не человек';
const result = confirm ('Ты человек?');
if (result == true) {
document.body.innerHTML = name  age  kind1;
}
if (result == false) {
document.body.innerHTML = name  age  kind2;
}
```

😎good
``` js
let name = 'Антонина Максимова, ';
let age = 23;
let kind1 = ', Человек';
let kind2 = ', Не человек';
const result = confirm ('Ты человек?');
if (result == true) {
document.body.innerHTML = name  age  kind1;
}
if (result == false) {
document.body.innerHTML = name  age  kind2;
}
```
---

## 7. Никогда не оставляйте пустые или неиспользуемые блоки и другие структуры в коде. Даже в закомментированном виде.

  😦bad
``` js
switch(omg) {
}
```

😎good
``` js
switch (true) {
 case money >= 800:
 	console.log ('Ноутбук');
  break;
 case money <= 800 && money > 100: 
 	console.log ('Телефон');
  break;
 case money <= 100:
 	console.log ('Плеер');
  break;
}
```
---

## 8. Пиши в объектах каждую пару "ключ-свойство" с новой строки.
  😦bad
``` js
const user = { name: 'Antonina', surname: 'Maksimova', age: 23 }
```

😎good
``` js
const user = {
  name: 'Antonina',
  surname: 'Maksimova',
  age: 23
}
```
---

## 9. По возможности используйте только строгие типы сравнения, которые учитывают тип данных. 
**В противном случае произойдет преобразование типа данных под один из тех, что стравниваются**

  😦bad
``` js
0 == ''; //верно
1 == '1'; //верно
1 == true; //верно
```

😎good
``` js
0 === ''; //неверно
1 === '1'; //неверно
1 === true; //неверно
```
---

## 10. Для оформления кода используйте отступы в 2 пробела.

  😦bad
``` js
function result (user) {
if(user.firstName && user.middleName && user.lastName) {
 console.log(true);
 } else {
console.log(false);
 }
}
```

😎good
``` js
function result (user) {
  if(user.firstName && user.middleName && user.lastName) {
  console.log(true);
  } else {
  console.log(false);
  }
}
```
---
