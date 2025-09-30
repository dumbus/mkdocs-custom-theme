## Создание и развертывание статического сайта (Отчёт)

> Дисциплина "Проектирование и развертывание веб-решений в эко-системе Python"

### Шаги работы

1. Создать репозиторий в GitHub.
2. Клонировать репозиторий локально, не забыть добавить .gitignore.
3. Развернуть Python-проект на каком-либо движке (создание виртуального окружения, установка зависимостей) *(был выбран mkdocs)*
4. Создать 1-2 страницы локально, сбилдить их, загрузить на хостинг
5. Автоматизировать деплой (GitHub Actions)

### Описание выполнения работы

1. Создание репозитория в github

<img width="1920" height="986" alt="1" src="https://github.com/user-attachments/assets/408f9624-fa65-4ba7-81dc-3a3f88fef354" />

2. Клонирование репозитория локально, создание виртуального окружения

<img width="1920" height="1030" alt="2" src="https://github.com/user-attachments/assets/071d70d5-38a4-412c-8038-06044c21d471" />

3. Использование виртуального окружения

<img width="1920" height="1030" alt="3" src="https://github.com/user-attachments/assets/346e711a-ddec-4797-b5ee-dc64a5c11a5a" />

4. Создание шаблона проекта с помощью `mkdocs`

<img width="1920" height="983" alt="4" src="https://github.com/user-attachments/assets/6c501496-055f-4083-bf28-067f70fc38c8" />

5. Наполнение статического сайта своей информацией (информация о НИР 2)

<img width="1920" height="983" alt="5" src="https://github.com/user-attachments/assets/26722b72-db7c-4ddd-9aeb-0cb077dbc9bb" />

6. Сборка статического сайта с помощью `mkdocs`

<img width="1920" height="1030" alt="6" src="https://github.com/user-attachments/assets/f19c7269-23bc-4e38-9688-3526b6264da8" />

7. Деплой созданного сайта на `github-pages` вручную (использовался push папки `site` в ветку `gh-pages`)

<img width="1920" height="981" alt="7" src="https://github.com/user-attachments/assets/46c4338b-09b3-40c4-8d2b-44bb034cf85f" />

8. Демонстрация опубликованного на `gh-pages` вручную сайта

<img width="1920" height="983" alt="8" src="https://github.com/user-attachments/assets/9ed02a9f-b5a9-4c6b-9982-9f4c5e47983f" />

9. Создание и настройка `GitHub Actions workflow` для автоматического деплоя на `gh-pages` (при `push` в ветки `develop/main`)

<img width="1920" height="1030" alt="9" src="https://github.com/user-attachments/assets/1f6438c5-1aa7-4ca1-b306-944c40a55de6" />

10. Переключение gh-pages на деплой с помощью `github actions`

<img width="1920" height="979" alt="10" src="https://github.com/user-attachments/assets/59ef3812-b803-4709-bd15-30de7bb374a7" />

11. Добавление дополнительного контента на сайт, чтобы можно было удостовериться, что на gh-pages находится новая версия, опубликованная автоматически с помощью github-actions

<img width="1920" height="1030" alt="11" src="https://github.com/user-attachments/assets/fa3d8e08-2c6d-4a4c-973f-2812315f27cf" />

12. Успешное выполнение github action

<img width="1920" height="981" alt="12" src="https://github.com/user-attachments/assets/15112fde-4db8-43db-9344-2f2ae6853d61" />

13. Новая запись среди `gh-pages deployments `

<img width="1920" height="981" alt="13" src="https://github.com/user-attachments/assets/631552bc-4391-4628-a00f-75aaaa4e40e4" />

14. Демонстрация автоматически опубликованного на `gh-pages` сайта (добавленная на сайт для проверки строчка присутствует)

<img width="1920" height="977" alt="14" src="https://github.com/user-attachments/assets/573673de-bdd5-4c02-89d0-8f0b0db0b3ec" />

## Ответы на вопросы (Исследование)

1.	Возможности использования отечественных CDN для ускорения доставки контента

[ngenix](https://ngenix.net/ecp/cdn/) – Есть возможность запросить бесплатный пробный период на 2 недели
[EDGE Центр](https://edgecenter.ru/cdn) – Есть возможность запросить бесплатный пробный период на 2 недели


[Selectel]( https://selectel.ru/services/additional/cdn/)
[VK Cloud]( https://cloud.vk.com/cdn/)
[Yandex Cloud](https://yandex.cloud/ru/docs/cdn)
[cdnvideo](https://www.cdnvideo.ru/solutions/cdn-for-website-acceleration/)
[Cloud.ru](https://cloud.ru/products/cloud-cdn?utm_source=google.com&utm_medium=organic&utm_campaign=google.com&utm_referrer=google.com)

2. Возможности Gitverse для реализации CI/CD

Судя по документации, Gitverse поддерживает `GitVerse Actions`, схожие по функционалу с `GitHub Actions`: https://gitverse.ru/docs/knowledge-base/actions/runners/  

По аналогии с GitHub Actions, конфигурационные файлы рабочих процессов GitVerse Actions должны быть написаны в синтаксисе YAML и располагаться в .gitverse/workflows/  репозитория.  

Пример из документации: https://gitverse.ru/gitverse_tutorials/CICD_examples/content/demo

3. Какие существуют варианты деплоя статического сайта в продакшен среду и какие технические инструменты для этого могут потребоваться, приведите примеры

- Ручной деплой (загрузка файлов сборки на сервер вручную через клиенты вроде FileZilla)

- Деплой через Git (ряд хостингов имеет возможность автоматически подтягивать изменения из ветки и запускать сборку и деплой. Пример: [Vercel](https://vercel.com/docs/deployments#git))

- Деплой через CI/CD пайплайн (настраивается автоматический конвейер, который запускает скрипты для тестирования, сборки и деплоя автоматически при поступлении нового кода в репозиторий. Пример инструментов: использование `GitHub Actions`, `GitLab-CI`, `Jenkins` для построения пайплайнов).
