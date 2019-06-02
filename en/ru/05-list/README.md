## 5. Правила списков

Я не встречал ни одного АПИ, которое бы не возвращало список элементов. Либо это постраничная листалка, либо что-то построенное на курсорах для бесконечных списков. Списки надо фильтровать, сортировать, ограничивать кол-во возвращаемых элементов. Сам GraphQL никак не ограничивает свободу реализации, но для того чтобы сформировать некое единообразие, необходимо завести стандарт.

- **5. Правила списков** 
  - [5.1.](./5.1-filter.md) Для фильтрации списков используйте аргумент `filter`, который содержит в себе все доступные фильтры.
  - [5.2.](./5.2-sort.md) Для сортировки списков используйте аргумент `sort`, который должен быть `Enum` или `[Enum!]`.
  - [5.3.](./5.3-limit-skip.md) Для ограничения возвращаемых элементов в списке используйте аргументы `limit` со значением по умолчанию и `skip`.
  - [5.4.](./5.4-pagination.md) Для пагинации используйте аргументы `page`, `perPage` и возвращайте output-тип с полями `items` с массивом элементов и `pageInfo` с метаданными для удобной отрисовки страниц на клиенте.
  - [5.5.](./5.5-cursor-connection.md) Для бесконечных списков (infinite scroll) используйте [Relay Cursor Connections Specification](https://facebook.github.io/relay/graphql/connections.htm).