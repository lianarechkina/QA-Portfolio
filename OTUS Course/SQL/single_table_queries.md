## Задание
### Составьте запросы:
a) Выведите значение колонки ContactName
b) Выведите все возможные значения колонки Country
c) Выведите все записи, где City имеет значение London
d) Выведите все записи, где City не равен London
e) Выберите все записи, где Country равна Mexico и Postal Code 05021
f) Выберете все записи у которых Country равна Mexico или Sweden

**Структура и наполнение таблицы otusQA**:
| CustomerID | CustomerName                       | ContactName        | Address                       | City        | PostalCode | Country |
|---|---|---|---|---|---|---|
| 1          | Alfreds Futterkiste                | Maria Anders       | Obere Str. 57                 | Berlin      | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados | Ana Trujillo       | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería            | Antonio Moreno     | Mataderos 2312                | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn                    | Thomas Hardy       | 120 Hanover Sq.               | London      | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                 | Christina Berglund | Berguvsvägen 8                | Luleå       | S-958 22   | Sweden  |

SQL request
```SQL a) SELECT contactname FROM otusQA

b) SELECT DISTINCT country FROM otusQA

c) SELECT * FROM otusQA
WHERE city = 'London';

d) SELECT * FROM otusQA
WHERE city != 'London';

e) SELECT * FROM otusQA
WHERE country = 'Mexico' AND postalcode = '05021';

f) SELECT * FROM otusQA
WHERE country IN ('Mexico', 'Sweden');
```
