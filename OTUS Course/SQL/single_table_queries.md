## Задание
### Составьте запросы:
1. Выведите значение колонки ContactName
2. Выведите все возможные значения колонки Country
3. Выведите все записи, где City имеет значение London
4. Выведите все записи, где City не равен London
5. Выберите все записи, где Country равна Mexico и Postal Code 05021
6. Выберете все записи у которых Country равна Mexico или Sweden

**Структура и наполнение таблицы otusQA**:
| CustomerID | CustomerName                       | ContactName        | Address                       | City        | PostalCode | Country |
|---|---|---|---|---|---|---|
| 1          | Alfreds Futterkiste                | Maria Anders       | Obere Str. 57                 | Berlin      | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados | Ana Trujillo       | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería            | Antonio Moreno     | Mataderos 2312                | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn                    | Thomas Hardy       | 120 Hanover Sq.               | London      | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                 | Christina Berglund | Berguvsvägen 8                | Luleå       | S-958 22   | Sweden  |

SQL request
```SQL 
1. SELECT contactname FROM otusQA

2. SELECT DISTINCT country FROM otusQA

3. SELECT * FROM otusQA
WHERE city = 'London';

4. SELECT * FROM otusQA
WHERE city != 'London';

5. SELECT * FROM otusQA
WHERE country = 'Mexico' AND postalcode = '05021';

6. SELECT * FROM otusQA
WHERE country IN ('Mexico', 'Sweden');
```
