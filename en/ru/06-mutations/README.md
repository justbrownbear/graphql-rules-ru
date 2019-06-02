## 6. Правила Мутаций

Сколько схем я не смотрел, но больше всего бардака разводят в Мутациях. Следующие правила позволят вам сделать ваше АПИ сухим, чистым и удобным.

- **6. Правила Мутаций** 
  - [6.1.](./6.1-mutation-namespaces.md) Используйте Namespace-типы для группировки мутаций в рамках одного ресурса!
  - [6.2.](./6.2-business-operations.md) Выходите за рамки CRUD – cоздавайте небольшие мутации для разных бизнес операций над ресурсами.
  - [6.3.](./6.3-batch-changes.md) Рассмотрите возможность выполнения мутаций сразу над несколькими элементами (однотипные batch-изменения).
  - [6.4.](./6.4-required-args.md) У мутаций должны быть четко описаны все обязательные аргументы, не должно быть вариантов либо-либо.
  - [6.5.](./6.5-input-arg.md) У мутации вкладывайте все переменные в один уникальный `input` аргумент.
  - [6.6.](./6.6-payload.md) Мутация должна возвращать свой уникальный Payload-тип. 
    - [6.6.1.](./6.6.1-payload-record.md) В ответе мутации возвращайте измененный ресурс и его `id`.
    - [6.6.2.](./6.6.2-payload-status.md) В ответе мутации возвращайте статус операции.
    - [6.6.3.](./6.6.3-payload-query.md) В ответе мутации возвращайте поле с типом `Query`.
    - [6.6.4.](./6.6.4-payload-errors.md) В ответе мутации возвращайте поле `errors` с типизированными пользовательскими ошибками.