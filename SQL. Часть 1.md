Задание 1
Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.

Решение:

SELECT DISTINCT
    district
FROM
    addresses
WHERE
    district REGEXP '^K.*a$'
    AND district REGEXP '^[^\s]+$'


Задание 2
Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.

    Решение:

    SELECT
    payment_id,
    customer_id,
    movie_id,
    payment_date,
    payment_amount
FROM
    payments
WHERE
    payment_date >= '2005-06-15'
    AND payment_date <= '2005-06-18'
    AND payment_amount > 10.00



Задание 3
Получите последние пять аренд фильмов.


  Решение: 
  SELECT
    rental_id,
    customer_id,
    movie_id,
    rental_date,
    return_date
FROM
    rentals
ORDER BY
    rental_date DESC
LIMIT
    5

    Задание 4
Одним запросом получите активных покупателей, имена которых Kelly или Willie.

Сформируйте вывод в результат таким образом:

все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
замените буквы 'll' в именах на 'pp'.

Решение:

SELECT
    customer_id,
    last_name,
    first_name
FROM
    customers
WHERE
    last_name IN ('Kelly', 'Willie')
    AND is_active = TRUE
    AND first_name LIKE '%ll%'
    AND first_name = REPLACE(first_name, 'll', 'pp')

    Задание 5*
Выведите Email каждого покупателя, разделив значение Email на две отдельных колонки: в первой колонке должно быть значение, указанное до @, во второй — значение, указанное после @.

Решение: 
SELECT
    customer_id,
    email_prefix,
    email_suffix
FROM
(
    SELECT
        customer_id,
        email,
        SPLIT_PART(email, '@', 1) AS email_prefix,
        SPLIT_PART(email, '@', 2) AS email_suffix
    FROM
        customers
) AS t

Задание 6*
Доработайте запрос из предыдущего задания, скорректируйте значения в новых колонках: первая буква должна быть заглавной, остальные — строчными.

Решение:
SELECT
    customer_id,
    UPPER(email_prefix) AS email_prefix,
    UPPER(email_suffix) AS email_suffix
FROM
(
    SELECT
        customer_id,
        email,
        SPLIT_PART(email, '@', 1) AS email_prefix,
        SPLIT_PART(email, '@', 2) AS email_suffix
    FROM
        customers
) AS t


