Необходимо создать компонент <Profile>, с помощью которого мы могли бы отображать информацию о пользователе социальной сети. Данные о пользователе лежат в файле user.json.

Описание компонента <Profile>
Компонент должен принимать несколько пропсов с информацией о пользователе:

username — имя пользователя
tag — тег в социальной сети без @
location — город и страна
avatar — ссылка на изображение
stats — объект с информацией об активности
Компонент должен создавать DOM элемент следующей структуры.


Компонент должен создавать DOM элемент следующей структуры.

<div class="profile">
  <div class="description">
    <img
      src="https://cdn-icons-png.flaticon.com/512/1077/1077012.png"
      alt="User avatar"
      class="avatar"
    />
    <p class="name">Petra Marica</p>
    <p class="tag">@pmarica</p>
    <p class="location">Salvador, Brasil</p>
  </div>

  <ul class="stats">
    <li>
      <span class="label">Followers</span>
      <span class="quantity">1000</span>
    </li>
    <li>
      <span class="label">Views</span>
      <span class="quantity">2000</span>
    </li>
    <li>
      <span class="label">Likes</span>
      <span class="quantity">3000</span>
    </li>
  </ul>
</div>


Пример использования
import user from 'путь/к/user.json;

<Profile
  username={user.username}
  tag={user.tag}
  location={user.location}
  avatar={user.avatar}
  stats={user.stats}
/>