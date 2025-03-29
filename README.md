# Урок 1. Знакомство с React и первые компоненты. Работа с JSX

Развернуть новый проект с использованием create-react-app.
Создать компонент Message, отображающий переданный ему props текст.
Стилизовать компоненты через css (при желании можно использовать less или sass).
Дополнительное задание: Установить расширение React Devtools.

# Урок 2. State, Props. Жизненный цикл react компонента. Хуки
Задание: Список комментариев с удалением.

Цель: Комбинирование useState, рендеринга списков и обработки событий для создания интерактивного интерфейса.

Задача:
Создать компонент CommentsList, который отображает список комментариев. Каждый комментарий должен иметь кнопку для его удаления. При нажатии на кнопку комментарий должен удаляться из списка.

# Урок 3. Virtual DOM. Подключение библиотеки UI-компонентов
Задание 1: Температурный конвертер с Material UI

Цель: Создать компонент TemperatureConverter, используя компоненты TextField и Button из Material UI для ввода и отображения температур в градусах Цельсия и Фаренгейта.

Компоненты:
Используйте TextField для ввода значения температуры.
Добавьте лейблы к каждому TextField, указывая единицы измерения (Цельсия и Фаренгейта).

Логика:
При вводе значения в одно поле, автоматически конвертируйте его и отобразите в другом.
Реализуйте конвертацию температур в обоих направлениях.


Задание 2: Список дел с Material UI

Цель: Разработать компонент TodoList для управления задачами: добавление, отображение, и удаление задач.

Компоненты:
Используйте TextField для ввода новой задачи.
Добавьте Button для добавления задачи в список.
Для каждой задачи в списке используйте Card или ListItem из Material UI. Внутри каждого элемента списка разместите текст задачи и IconButton с иконкой удаления (например, DeleteIcon).

Логика:
При нажатии на кнопку добавления, новая задача должна добавляться в список.
Рядом с каждой задачей должна быть кнопка для её удаления.

# Урок 4. Children. Роутинг в React
Создать приложение с двумя страницами: "Главная страница" и "О нас".
На каждой странице должна быть навигационная ссылка для перехода на другую страницу.

Шаги выполнения:

Установка react-router-dom:
Если еще не установлен, добавьте react-router-dom в ваш проект: npm install react-router-dom.

Создание компонентов:
— Создайте два компонента: HomePage.jsx и AboutPage.jsx.
— В каждом компоненте добавьте простой текст, например, <h1>Главная страница</h1> для HomePage и <h1>О нас</h1> для AboutPage.
— Реализовать переходы.

# Урок 5. Компоненты высшего порядка знакомство с Redux
Приложение для переключения темы сайта
Создать приложение, позволяющее пользователю переключать между светлой и темной темой сайта.

Функционал:

Action types: TOGGLE_THEME.
Actions: Создайте действие для переключения темы.
Reducer: Реализуйте редьюсер, который обрабатывает это действие и изменяет тему в состоянии приложения.
Component: Создайте компонент, который отображает переключатель для изменения темы сайта.


Описание:

Состояние: Для хранения текущей темы можно использовать логическую переменную (true для темной темы и false для светлой) или строку ("dark" или "light").

Интерфейс: Ваш интерфейс может состоять из переключателя, который изменяет тему с светлой на темную и обратно.

# Урок 6. Погружение в Redux. Connect
Разработать приложение для управления каталогом продуктов, позволяющее добавлять, удалять, отображать и редактировать продукты.

Настройка Redux Store:

Используйте configureStore из @reduxjs/toolkit для создания хранилища.
Определите начальное состояние и создайте слайс с использованием createSlice для продуктов. Каждый продукт должен иметь id, name, description, price, и available.

В слайсе определите редьюсеры и действия для добавления нового продукта, удаления продукта по ID, обновления продукта и изменения его доступности.


Компоненты React:

Компонент для добавления продукта:
Создайте форму, позволяющую пользователям вводить данные нового продукта (имя, описание, цена, доступность) и добавлять его в каталог.

Компонент для отображения продуктов:
Разработайте компонент, который отображает список всех продуктов с их атрибутами, а также кнопки для удаления продукта из каталога и переключения его доступности.

Компонент для редактирования продукта:
Опционально, предоставьте возможность редактирования существующих продуктов, чтобы можно было изменять их имя, описание, цену и доступность.

# Урок 7. Redux middlewares. Redux persist
Имитация асинхронной загрузки и отображения списка задач из локального хранилища.

1. Инициализация проекта и установка зависимостей: Инициализируйте новый проект React . Установите @reduxjs/toolkit и react-redux.

2. Создание локальных данных: Определите массив объектов, представляющих задачи, в файле, например, src/data/tasks.js. Каждая задача может содержать поля, такие как id, title и completed.

3. Настройка Redux store: Создайте Redux store с использованием configureStore из @reduxjs/toolkit. Используйте Redux Thunk middleware, уже включённый в @reduxjs/toolkit.

4. Создание асинхронного действия с использованием Thunk: Используйте createAsyncThunk для создания асинхронного действия, которое "загружает" данные задач из локального файла. Хотя данные и локальные, имитируйте асинхронное поведение, например, с использованием setTimeout.

5. Работа с компонентом: Используйте хуки useDispatch и useSelector в компоненте для диспетчеризации асинхронного действия и выборки списка задач из состояния. Выведите список задач.