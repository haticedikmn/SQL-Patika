# SQL-Patika
ÖDEVLER

ÖDEV-1:Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.
1.	film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
            
            select title, description from film;
2.	film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
            
            select * from film
            where length > 60 and length < 75;
3.	film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
            
            select * from film
            where rental_rate= 0.99 and replacement_cost = 12.99 or replacement_cost = 28.99;
4.	customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
          
           select * from customer 
           where first_name='Mary' ;
           ("Smith")
5.	film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
         
          select * from film
           where  length < 50 and not (rental_rate=2.99 or 
           rental_rate=4.99);

Ödev-2:Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.
1.film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)
            
           select * from film
           where replacement_cost between 12.99 and 16.99;

2.actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)  
         
         select first_name, last_name from actor
         where first_name in('Penelope', 'Nick', 'Ed');

3.film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)
        
        select * from film
        where rental_rate in(0.99, 2.99, 4.99) and replacement_cost in(12.99, 15.99, 28.99);


