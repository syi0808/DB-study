<h1>첫번째 쿼리</h1>

world 데이터베이스에서 country 테이블에서 A로 시작하는 CODE만 SurfaceArea를 기준으로 내림차순으로 정렬해 출력하시오.

```mysql
SELECT * 
  FROM world.country
 WHERE CODE LIKE 'A%'
ORDER BY SurfaceArea DESC;
```

<h1>두번째 쿼리</h1>

world 데이터베이스에서 country 테이블에서 IndepYear이 1000년도 이후에 생성되고 인구수가 10만명 이하이고 대륙이 아시아 이거나 오세아니아 인 B를 포함한 나라를 출력하시오

```mysql
SELECT *
  FROM world.country
 WHERE IndepYear >= 1000 && Population <= 100000 && Continent in ('ASIA', 'OCEANIA') && Name LIKE '%B%';
```

<h1>세번째 쿼리</h1>

world 데이터베이스에서 country 테이블에서 평균수명이 60세 이상 70세 미만인 나라들 중 인구수가 500만명 이상인 나라들을 나라이름 내림차순으로 NAME과 GNP만  출력하시오.

```mysql
SELECT NAME, GNP
  FROM world.country
 WHERE (LifeExpectancy >= 60 && LifeExpectancy < 70) && Population <= 5000000
ORDER BY Name DESC;
```

