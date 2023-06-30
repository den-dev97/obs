## debounce()
- это техника в программировании, которая позволяет установить задержку между последним вызовом функции и ее фактическим выполнением. Это полезно в ситуациях, когда функция вызывается часто или множество раз, но требуется выполнить ее только один раз после определенного периода неактивности.
```
const fetchUrl = (url) => {
  console.log(`fetch url ${url}...`)
}
function debounce(callback, delay) {
  let timer = null;
  return (...args) => {
    clearTimeout(timer); // Очищаем предыдущий таймер, если он был установлен
    timer = setTimeout(() => {
      callback(...args); // Вызываем функцию callback после задержки
    }, delay);
  }
}

const fetching = debounce(fetchUrl, 1);

fetching(1); // Запускаем вызов функции fetchUrl с аргументом 1
fetching(2); // Запускаем вызов функции fetchUrl с аргументом 2
fetching(3); // Запускаем вызов функции fetchUrl с аргументом 3
```