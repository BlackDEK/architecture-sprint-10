# Аудит

## Данные в покое

- Данные никак не классифицируются по критичности.
- Персональные данные хранятся в открытом формате и их может прочитать любой авторизованный пользователь.
  - ФИО, дата рождения, телефон, электронная почта, адрес прописки, место работы и т.д.
- Данные анализов и приема пациентов лежат в открытом виде, редактировать их может любой сотрудник.
- Нету логирования чтения и записи данных.
- Нет валидации для формата данных, на диск могут быть сохранены любые данные в любом формате.
- Нет механизма гарантированного удаления данных о клиенте. То есть при необходимости удалить данные из БД, надо будет в ручную просмотреть несколько папок и вычистить данные о клиенте.
- У данных нет времени жизни.

## Данные в пути

- Данные ни как не шифруются при передаче.

## Данные в работе

- При обработке данных, нет валидации. То есть при ручном заполнении могут быть допущены ошибки и система никак их не обработает.

# Предложение по улучшению

## Данные в покое

- Персональные данные надо хранить в зашифрованном виде.
- Медицинские информации надо хранить в зашифрованном виде.
- Необходимо классифицировать данные и ограничить доступ к данным по ролям.
  - Например можно классифицировать так
    - Публичные - брошюры, рекламные материалы и т.д.
    - Внутренние - данные связанные с сотрудниками компании.
    - Конфиденциальные - персональные и медицинские данные клиентов, коммерческая тайна.
- Раз в полгода проводить аудит доступа к данным.
- Реализовать централизованное хранилище данных.
- Ввести для некоторого типа данных срок жизни, если клиент не обращается в клинику в течении некоторого времени то данные связанные с ним должны удаляться.

## Данные в пути

- Персональны данные при передаче надо обезличивать.
  - Как пример при передаче анализов в лабораторию.

## Данные в работе

- При работе с данными, нужно обеспечить валидацию перед записью.
  - Например сделать форму для заполнения телефонного номера или номера СНИЛС.