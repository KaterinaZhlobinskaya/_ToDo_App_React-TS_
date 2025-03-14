# React Todo App with API

Цей проєкт є покроковою реалізацією Todo-додатку з інтеграцією API. Проєкт в процесі розробки був поділений на три основні етапи: завантаження, додавання/видалення та редагування/відмітка всіх завдань.

## 📖 Про проєкт

У рамкаx проєкту я розробила Todo-додаток, який дозволяє користувачам завантажувати завдання з API, додавати нові та видаляти необхідні завдання, фільтрувати завдання за статусом (всі, активні, завершені), позначати завдання як виконані (всі або окремі з них), редагувати заголовки завдань, бачити відображення помилки у випадку неуспішного запиту, автоматично зберігати зміни після виходу з поля вводу (onBlur, Enter), не зберігати порожні завдання при спробі зберегти пустий заголовок.

## 🔧 Використані технології

- **React, React-dom** – основа проєкту;
- **TypeScript** – для типізації коду;
- **SCSS + Bulma** – для стилізації компонентів;
- **HTTP-запити** – для запитів до API з костомним client, заснованим на fetch;
- **API** – використовується для збереження та отримання завдань.

## 🚀 Функціональність

### ✅ 1. Завантаження списку завдань (Load Todos)
- Завантаження списку задач через API (з використанням `fetchClient.ts`).
- Відображення повідомлень про помилки у разі невдачі.
- Фільтрація задач за статусом: `All`, `Active`, `Completed`.
- Відображення спінерів при завантаженні.

### ✍️ 2. Додавання та видалення завдань (Add & Delete)
- Додавання нового завдання за допомогою `POST`-запиту.
- Валідація введеного заголовка (не може бути пустим).
- Фокусування на полі введення після додавання.
- Тимчасове відображення нового завдання до отримання відповіді API.
- Видалення завдань (індивідуально або масово для `completed`).
- Відображення спінера під час взаємодії із сервером.

### 🔄 3. Перемикання статусу та редагування (Toggle & Rename)
- Перемикання статусу виконання завдання (`completed` / `active`).
- Відображення спінерів при оновленні статусу.
- Групове перемикання статусу всіх завдань.
- Редагування заголовка завдання (на `double click`).
- Автоматичне збереження змін після виходу з поля вводу (`onBlur` або `Enter`).
- Видалення завдання при спробі зберегти пустий заголовок.
- Відображення повідомлення про помилку при невдалому запиті.

## ✨ Особливості

- **Реалізація додатку з нуля**: функціональні компоненти написані вручну з використанням хуків (useRef, useCallback, useMemo, useState, useEffect).
- **Кастомний HTTP-клієнт**: кастомний HTTP-клієнт був заснований на fetch для запитів до API.
- **Штучна затримка**: затримка в 100мс при надсиланні запитів до API реалізована для коректної роботи тестів за необхідності.
- **Ефективна обробка помилок**:  відображення повідомлень про помилки без переривання роботи програми.

## 🛠 Як запустити локально

- **Клонуйте репозиторій**:
     ```sh
     git clone https://github.com/KaterinaZhlobinskaya/_ToDo_App_React-TS_.git
- **Відкрийте проєкт в редакторі коду** (приклад для VSC):
     ```sh
     code _ToDo_App_React-TS_
- **Перевірте версію ноди** (23.9.0):
  
       node -v
   - якщо версія не підходить до вимог, змініть її:
       ```sh
       nvm use XX.X.X
   - за відсутності встановленої Node встановіть її згідно інструкцій за посиланням:
       ```sh
       https://nodejs.org/uk/download
- **Встановіть залежності** (введіть наступну команду в терміналі редактора коду):
     ```sh
     npm install
- **Запустіть проєкт**:
     ```sh
     npm start

## 🌟 Демонстрація
Додаток доступний за посиланням:  
👉 [Todo App Demo](https://katerinazhlobinskaya.github.io/_ToDo_App_React-TS_/)

## 🛠 Чого я навчилася

- **Робота з API:** навчилася виконувати HTTP-запити (GET, POST, PATCH, DELETE) для роботи з сервером та керування списком задач.  
- **Обробка асинхронних запитів:** реалізувала затримку перед виконанням запиту для тестування та навчилася правильно обробляти помилки.  
- **Кастомний клієнт для запитів:** створила універсальну функцію `request`, яка спрощує взаємодію з API та зменшує повторення коду.  
- **Обробка стану додатку:** навчилася керувати станом задач, оновлювати інтерфейс після успішного виконання запитів та показувати спінери під час очікування.  
- **Фільтрація та управління списком задач:** реалізувала можливість фільтрувати задачі за статусом (усі, активні, виконані) та керувати ними (додавати, редагувати, видаляти, змінювати статус).  
- **Реалізація повідомлень про помилки:** створила систему сповіщень, яка інформує користувача про помилки та автоматично ховається через певний час.  
- **Оптимізація взаємодії користувача:** навчилася робити додаток зручнішим:  
  - Блокування кнопок під час запиту, щоб уникнути повторних дій.  
  - Фокусування на полях введення для швидшої взаємодії.  
  - Автоматичне очищення полів після успішного додавання задачі.  

Цей проєкт допоміг мені краще зрозуміти роботу з React, асинхронними запитами та оптимізацію UI для покращення взаємодії користувача. 🚀

# React Todo App with API

This project is a step-by-step implementation of a Todo app with API integration. The project was divided into three main stages during development: loading, adding/removing and editing/marking all tasks.

## 📖 About the project

As part of the project, I developed a Todo app that allows users to load tasks from the API, add new and delete necessary tasks, filter tasks by status (all, active, completed), mark tasks as completed (all or individual ones), edit task titles, see an error message in case of an unsuccessful request, automatically save changes after exiting the input field (onBlur, Enter), do not save empty tasks when trying to save an empty title.

## 🔧 Technologies used

- **React, React-dom** – the basis of the project;
- **TypeScript** – for code typing;
- **SCSS + Bulma** – for component styling;
- **HTTP requests** – for API requests with a custom client based on fetch;
- **Prettier** for code formatting;
- **API** – used to save and retrieve tasks.

## 🚀 Functionality

### ✅ 1. Loading a list of tasks (Load Todos)
- Loading a list of tasks via the API (using `fetchClient.ts`).
- Displaying error messages in case of failure.
- Filtering tasks by status: `All`, `Active`, `Completed`.
- Displaying spinners when loading.

### ✍️ 2. Adding and deleting tasks (Add & Delete)
- Adding a new task using a `POST` request.
- Validating the entered header (cannot be empty).
- Focusing on the input field after adding.
- Temporarily displaying a new task until receiving an API response.
- Deleting tasks (individually or in bulk for `completed`).
- Displaying the spinner when interacting with the server.

### 🔄 3. Toggle status and edit (Toggle & Rename)
- Toggle task execution status (`completed` / `active`).
- Displaying spinners when updating the status.
- Group switching of the status of all tasks.
- Editing the task title (on `double click`).
- Automatically saving changes after leaving the input field (`onBlur` or `Enter`).
- Deleting the task when trying to save an empty title.
- Displaying an error message on an unsuccessful request.

## ✨ Features

- **Implementation of the application from scratch**: functional components are written manually using hooks (useRef, useCallback, useMemo, useState, useEffect).
- **Custom HTTP Client**: The custom HTTP client was based on fetch for API requests.
- **Artificial Delay**: A 100ms delay when sending API requests is implemented to ensure correct test performance when needed.
- **Efficient Error Handling**: Error messages are displayed without interrupting the application.

## 🛠 How to run locally

- **Clone the repository**:
   ```sh
   git clone https://github.com/KaterinaZhlobinskaya/_ToDo_App_React-TS_.git
- **Open the project in the code editor** (example for VSC):
   ```sh
   code _ToDo_App_React-TS_
- **Check the node version** (23.9.0):

      node -v
   - if the version does not meet the requirements, change it:
      ```sh
      nvm use XX.X.X
   - if Node is not installed, install it according to the instructions at the link:
      ```sh
      https://nodejs.org/uk/download
- **Install dependencies** (enter the following command in the code editor terminal):
   ```sh
   npm install
- **Start the project**:
   ```sh
   npm start

## 🌟 Demo
The application is available at the link:
👉 [Todo App Demo](https://katerinazhlobinskaya.github.io/_ToDo_App_React-TS_/)

## 🛠 What I learned

- **Working with API:** learned how to execute HTTP requests (GET, POST, PATCH, DELETE) to work with the server and manage the list of tasks.
- **Handling asynchronous requests:** implemented a delay before executing a request for testing and learned how to handle errors correctly.
- **Custom client for requests:** created a universal `request` function that simplifies interaction with the API and reduces code duplication.
- **Handling application state:** learned how to manage the state of tasks, update the interface after successful execution of requests, and show spinners while waiting.
- **Filtering and managing the task list:** implemented the ability to filter tasks by status (all, active, completed) and manage them (add, edit, delete, change status).
- **Implementing error notifications:** created a notification system that informs the user about errors and automatically hides after a certain time.
- **Optimizing user interaction:** learned how to make the application more convenient:
- Locking buttons during a request to avoid repeated actions.
- Focusing on input fields for faster interaction.
- Automatic clearing of fields after a successful task addition.

This project helped me better understand working with React, asynchronous requests, and optimizing UI to improve user interaction. 🚀
