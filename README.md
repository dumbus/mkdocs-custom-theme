## Кастомизация статического сайта (шаблонизация, сборка статики: HTML, CSS, JS) (Отчёт)

> Дисциплина "Проектирование и развертывание веб-решений в эко-системе Python"

### Шаги работы

1. Создать собственную тему на основе HTML, CSS, JS с использованием или без использования CSS-библиотек таких как Bootstrap, Bulma, фреймворков (например, Tailwind), JS-библиотек для разработки фронтэнда (например, React). 
2. Разработать пайплайн или набор пайплайнов (yml-файл) для тестирования и  сборки статики (HTML, CSS, JS) — фронтэнда сайта, а затем построения собственно самого сайта (интеграции контента в разметке Markdown в шаблон сайта) и деплоя его на GitHub Pages. 
3. Необходимо учесть, что HTML файлы должны валидироваться на корректность, минифицироваться, должна быть предусмотрена сборка с помощью PostCSS.

### Описание выполнения работы

1. Создание папки `theme` с файлами шаблона `main.html` и стилей `styles.css`.

<img width="1920" height="1030" alt="1" src="https://github.com/user-attachments/assets/a1eaf2c0-5c98-4013-bb8d-77b84e05d045" />

2. Использование синтаксиса `Jinja2` для добавления в html-шаблон контента из mkdocs (расположенного в файлах `*.md`)

<img width="1920" height="1030" alt="2" src="https://github.com/user-attachments/assets/cc035a3a-3739-4c82-bb4c-39e0223e4376" />

3. Добавление в файл `styles.css` стилей для страниц сайта

<img width="1920" height="1030" alt="3" src="https://github.com/user-attachments/assets/c71bdd68-3b32-4488-95fd-481db003f410" />

4. Добавление на сайт meta-тегов с метаданными

<img width="1920" height="1030" alt="4" src="https://github.com/user-attachments/assets/d10b74eb-674b-465c-96c7-5a1a39e8465c" />

5. Запуск статического сайта с кастомной темой локально

<img width="1920" height="1030" alt="5" src="https://github.com/user-attachments/assets/9a6bee7b-706c-4728-af11-1e5837becd86" />

6. Формирование npm-скриптов для минимизации и валидации статики сайта

<img width="1920" height="1030" alt="6" src="https://github.com/user-attachments/assets/eddcf536-dd21-43a1-b95a-c4b69dd7e8d2" />

7. Запуск команды сборки (`npm run build`) для получения минифицированной версии статики сайта

<img width="1920" height="1030" alt="7" src="https://github.com/user-attachments/assets/0f8bc822-e78c-420d-bf16-3b3579764df7" />

8. Демонстрация работы валидации html-кода (валидатор указывает на незакрытый html-тег)

<img width="1920" height="1030" alt="8" src="https://github.com/user-attachments/assets/4a552d10-800a-4ef8-a9c9-f6819b59eb02" />

9. Формирование обновлённого пайплайна для публикации на `gh-pages` со сборкой кастомной темы

<img width="1920" height="1030" alt="9" src="https://github.com/user-attachments/assets/233a8466-5f35-4503-b584-c5af8611865c" />

10. Успешное выполнение команд из пайплайна

<img width="1920" height="1030" alt="10" src="https://github.com/user-attachments/assets/8dbd028b-7a1f-4f42-95f2-8c99ac26051d" />

11. Сайт с кастомной темой, автоматически опубликованный на `gh-pages`

<img width="1920" height="1030" alt="11" src="https://github.com/user-attachments/assets/d4bfbc93-b504-49f7-bce4-36bbab84eb9b" />
