# #JSX
1. Создайте пустой проект аналогично как  в задании с hw#1
2. По [ссылке](https://ru.reactjs.org/docs/introducing-jsx.html) ознакомьтесь с информацией по JSX разметке.
3. По [ссылке](https://ru.reactjs.org/docs/lists-and-keys.html#embedding-map-in-jsx) ознакомьтесь с информацией по рендеру нескольких компонентов. (в примерах вы встретите такое понятие как props, сейчас представляйте что это обычный js обьект, свойства которого мы на данном этапе используем как исходные данные с которыми намерены работать)
4. Внутри проекта создайте папку Components и уже в нем создайте папку c названием jokesList которая будет хранить в себе одноименный компонент jokesList.js
5. Внутри файла jokesList.js подготовьте разметку компонента и создайте внутри константу jokesData для дайльнейшей работы.
```js
import React from 'react';

const JokeList = () => {
    const jokesData = []
    
    return (
        <div>
            
        </div>
    );
};

export default JokeList;
```
6. Константа jokesData должна хранить в себе следующие данные:
```js
  const jokesData = [
   {
      id: 1,
      punchLine: "It’s hard to explain puns to kleptomaniacs because they always take things literally."
   },
   {
      id: 2,
      question: "What's the best thing about Switzerland?",
      punchLine: "I don't know, but the flag is a big plus!"
   },
   {
      id: 3,
      question: "Did you hear about the mathematician who's afraid of negative numbers?",
      punchLine: "He'll stop at nothing to avoid them!"
   },
   {
      id: 4,
      question: "Hear about the new restaurant called Karma?",
      punchLine: "There’s no menu: You get what you deserve."
   },
   {
      id: 5,
      question: "Did you hear about the actor who fell through the floorboards?",
      punchLine: "He was just going through a stage."
   },
   {
      id: 6,
      question: "Did you hear about the claustrophobic astronaut?",
   }
]
```

7. Ипортируйте компонент JokesList в App.js и используйте в корне компонента аналогичто как было сделано в hw#1.
```js
import React from 'react';
import JokeList from "./Components/jokeList/jokeList";

function App() {

return (
    <div className="App">
        <JokeList/>
    </div>
    );
}

export default App;
```
8. Теперь вернемся к компоненту JokeList. Вам необходимо создать компонент который возвращает разметку для масива jokesData с использованием тегов ul, li, p, h2. Используйте метод перебора масива .map. Для каждого елемента разметки который возвращает .map добавьте атрибут key со значением которое соответсвует id елемента. Если у елемента отсутсвует одно из необходимых полей - верните на его место строку-болванку со значением "empty"

9. После выполнения задания вы получите проект по структуре такой же как и в hw#1, изменится только название самого компонента и его логика уже будет не просто выдавать сообщение "Hello World" , а уже перебирая исходные данные возвращать соответсвующую разметку 
10. После выпполнения задачи и запуска проекта командой npm start по адресу http://localhost:3000/ вы получите результат в формате:
```
joke#1
question: "empty"
punchLine: "It’s hard to explain puns to kleptomaniacs because they always take things literally."

joke#2
question: "What's the best thing about Switzerland?"
punchLine: "I don't know, but the flag is a big plus!"
```
11. Так же добавьте минимальные стили и оформиите каждый елемент в виде карточки. Добавьте отступы, цвет фона, бордер. Для стилизации используйте подход с css модулями. по [ссылке](https://create-react-app.dev/docs/adding-a-css-modules-stylesheet) найдете информацию о том как работать с module.css. В папке с компонентом создайте файл с названием jokeList.module.css в нем опишите стили для классов которые присвоите елементам в разметке JokeList.js и в статье увидите примеры использования ваших классов. Необходимо импортировать стили и прописать елементам атрибуты className. 
12. Дополнительная информация по стилизации в React по [ссылке](https://www.cat-in-web.ru/10-ways-to-style-react/)