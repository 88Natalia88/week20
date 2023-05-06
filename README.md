# week20
### Вопросы 💎

1. Какие 2 обязательных шага нужно сделать до начала обращения к методам модулей?
ответ: проверить установлен ли Node.js - node -v и утилиты - npm -v; установить package.json - npm -init
2. Как узнать, установлен ли у тебя менеджер пакетов **npm**?
Ответ: npm -v
3. Зачем нужен блок `finally`? 
Ответ: Для завершения измерений, несмотря ни на что. finally используют, когда мы начали что-то делать и хотим завершить это вне зависимости от того, будет ошибка или нет.
4. Есть следующий код:
    
    ```jsx
    let user = undefined;
    console.log(`Привет, ${user.name}`);
    ```
    
    Как сделать так, чтобы при обращении к нему выводилось внятное сообщение об ошибке «‎Имя пользователя не заполнено»?
    Ответ:
    let user = undefined;
    try {
    console.log(`Привет, ${user.name}`);
    } catch(error) {
    console.log("Имя пользователя не заполнено" + error.message);
    }
    
5. Как сгенерировать собственную ошибку, например, в случае некорректного формата данных?
Ответ:
let json = `{"age": 30}`;
try {
    let user = JSON.parse(json);
    if (!user.name)
        throw new Error('Нет данных имени')
    console.log(user.name);
} catch (error) {
    console.log("Увы! " + error.message);
}

6. Какую команду надо ввести, чтобы сгенерировался файл `package.json`?
Ответ: npm init или npm init -y
7. Приведите пример захвата ошибки в случае некорректного преобразования данных:
    
    ```jsx
    console.log(parseInt('ыыыы'));
    ```
    Ответ:
8. Изучите документацию к библиотеке moment [https://momentjs.com/](https://momentjs.com/) и скажите, как вывести название дня недели по дате?
Ответ: moment().format('dddd'); 