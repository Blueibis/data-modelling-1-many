1)
SELECT title FROM articles
WHERE author_id in(SELECT id FROM authors
WHERE name = 'Kara Melton');
2)
SELECT * FROM cities
WHERE province_id in(SELECT id FROM provinces
WHERE name = 'Ontario');
3)
SELECT name FROM authors
WHERE id in(SELECT author_id FROM articles
WHERE title = 'Coding Bootcamps and Emotional Labor');
4)
SELECT COUNT(name) FROM provinces
WHERE country_id in(SELECT id from countries
WHERE name = 'Canada');
5)
select * from persons
where residence_id in(select id from residences
where address = '4740 McDermott Street');
6)
select * from cities
where id in(select city_id from residences
where address = '4740 McDermott Street');
7)
select * from provinces
where id in(select province_id from cities
where id in(select city_id from residences
where address = '4740 McDermott Street'));
8)
select * from countries
where id in(select country_id from provinces
where id in(select province_id from cities
where id in(select city_id from residences
where address = '4740 McDermott Street')));
9)
select * from countries
where id in(select country_id from provinces
where id in(select province_id from cities
where id in(select city_id from residences
where id in(select residence_id from persons
where name = 'Destini Davis'))));
10)
select count(title) from articles
where author_id in(select id from authors
where name = 'Aditya Mukerjee');
