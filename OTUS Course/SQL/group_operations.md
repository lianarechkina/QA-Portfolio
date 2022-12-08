## Задание

### Провести анализ продаж:
1. Посчитать общую стоимость проданных книг (продуктов) и их количество. В последующих запросах используем эти данные вручную.
2. Узнать количество продуктов и копий у каждого автора, рассчитать доли авторов в общем количестве проданных книг и в их общей стоимости.
3. Узнать количество копий каждого продукта, долю одной копии в общей стоимости, а также долю всех копий продукта в общей стоимости и количестве. 

**Структура и наполнение таблицы book**:

|book_id|title|author|price|amount|
|---|---|---|---|---|
|1| Мастер и Маргарита| Булгаков М.А.| 670.99 | 3|
|2| Белая гвардия| Булгаков М.А.| 540.50 | 5|
|3| Идиот| Достоевский Ф.М.| 460.00 | 10|
|4| Братья Карамазовы| Достоевский Ф.М.| 799.01 | 3|
|5| Игрок| Достоевский Ф.М.| 480.50 | 10|
|6| Стихотворения и поэмы| Есенин С.А.| 650.00 | 15|

SQL request

```SQL SELECT SUM(price*amount) AS Total_cost, SUM(amount) AS Total_amount
FROM book;

SELECT author,
       COUNT(author) AS Products,
       SUM(amount) AS Copies,
       ROUND(ROUND(SUM(amount * price) / 26267.50, 4) * 100, 2) AS Author_share_in_TC,
       ROUND(ROUND(SUM(amount) / 46, 4) * 100, 2) AS Author_share_in_TA
FROM book
GROUP BY author;

SELECT title AS Product_name,
       ROUND(ROUND(SUM(price)/26267.50, 4) * 100, 2) AS Copy_share_in_TC,
       SUM(amount) AS Copies
FROM book
GROUP BY title;
```


Query result 1:
|Total_cost|Total_amount|
|---|---|
|26267.50|46|

Query result 2:
|author|Products|Copies|Author_share_in_TC|Author_share_in_TA|
|---|---|---|---|---|
| Булгаков М.А.| 2| 8| 17.95| 17.39|
| Достоевский Ф.М.| 3| 23| 44.93| 50.00|
| Есенин С.А.| 1| 15| 37.12| 32.61|

Query result 3:

|Product_name|Copy_share_in_TC|Copies|
|---|---|---|
| Мастер и Маргарита|2.55|3|
| Белая гвардия|2.06|5|
| Идиот|1.75|10|
| Братья Карамазовы|3.04|3|
| Игрок| 1.83|10|
| Стихотворения и поэмы |2.47|15|
