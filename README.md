## [REST API](http://localhost:8080/doc)

## Концепция:

- Spring Modulith
    - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
    - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
    - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

- Есть 2 общие таблицы, на которых не fk
    - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
    - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем
      проверять

## Аналоги

- https://java-source.net/open-source/issue-trackers

## Тестирование

- https://habr.com/ru/articles/259055/

Список выполненных задач:

| №  | Задача                                                      | Статус | Комментарий                                                                            |
|:---|:------------------------------------------------------------|:-------|:---------------------------------------------------------------------------------------|
| 1  | Разобраться со структурой проекта                           | [x]    | Разобрался!                                                                            |
| 2  | Удалить социальные сети: vk, yandex                         | [x]    | Удалил все упоминания vk и yandex в проекте                                            |
| 3  | Вынести чувствительную информацию в отдельный проперти-файл | [ ]    | Вынес чувствительную информацию в `application-secrets.properties`                     |
| 4  | Переделать тесты для использования in-memory БД             | [ ]    |                                                                                        |
| 5  | Написать тесты для `ProfileRestController`                  | [ ]    |                                                                                        |
| 6  | Рефакторинг метода `FileUtil#upload`                        | [ ]    | Переписать метод, используя API `java.nio.file`                                        |
| 7  | Добавить функционал тегов для задач                         | [ ]    |                                                                                        |
| 8  | Добавить подсчет времени задачи                             | [ ]    |                                                                                        |
| 9  | Написать Dockerfile для основного сервера                   | [x]    | Dockerfile создан, приложение собирается и запускается                                 |
| 10 | Написать docker-compose файл                                | [x]    | docker-compose настроен для сервера, PostgreSQL и nginx. Проверить `config/nginx.conf` |
| 11 | Добавить локализацию                                        | [ ]    |                                                                                        |
| 12 | Переделать аутентификацию на JWT                            | [ ]    |                                                                                        |
