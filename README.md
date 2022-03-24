# Programmers_SQL_Select
* 사이트명 : 프로그래머스(Programmers)
* SQL : Oracle
* 난이도 : 하
## 문제 설명
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159735880-3e0eba1d-08b9-4953-b492-da2475404def.png">

| NAME | TYPE | NULLABLE |
|------|------|------|
| ANIMAL_ID | VARCHAR(N) | FALSE |
| ANIMAL_TYPE | VARCHAR(N) | FALSE |
| DATETIME | DATETIME |FALSE|
| INTAKE_CONDITION | VARCHAR(N)| FALSE |
| NAME|VARCHAR(N) | TRUE| 
| SEX_UPON_INTAKE | VARCHAR(N) | FALSE | 

## 모든 레코드 조회하기
![image](https://user-images.githubusercontent.com/102028778/159832084-2facca8a-8641-4f0b-9397-4aa502339dd5.png)
### * 설명
> ANIMAL_INS 테이블에서 모든 컬럼을 가져오고
ANIMAL_ID를 정렬해서 가져오는 문제이다.
방법은 Select *를 통해 모든 칼럼을 가져오고
Order By ANIMAL_ID를 넣어
ANIMAL_ID를 정렬하여 조회하면 된다.

### * 답안
Select * 
From ANIMAL_INS 
Order By ANIMAL_ID ASC;


## 역순 정렬하기
![image](https://user-images.githubusercontent.com/102028778/159832128-4c0db837-5da5-44b9-b651-a7cde0f71999.png)
### * 설명
> ORDER BY DESC역순정렬(내림차순)<->ORDER BY ASC(오름차순)
위, 문제와 비슷하며 위에는 오름차순 이 문제는 역순으로 내림차순(DESC)를
사용한다.

## * 답안
SELECT NAME,DATETIME from ANIMAL_INS order by ANIMAL_ID DESC;


## 아픈 동물 찾기
![image](https://user-images.githubusercontent.com/102028778/159832686-d64bc52b-21fb-4095-8a07-9ad21e440dcc.png)
### * 설명
> Where를 써서 테이블을 조회하는 방법인데
> ANIMAL_INS테이블에서 ANIMAL_ID , NAME 컬럼을 조회하면서
> INTAKE_CONDITION이 Sick인 경우에만 조회한다. ANIMAL_ID가 

### * 답안
SELECT ANIMAL_ID, NAME 
FROM ANIMAL_INS
WHERE INTAKE_CONDITION = 'Sick'
order by ANIMAL_ID;

## 어린 동물 찾기
<img width="534" alt="image" src="https://user-images.githubusercontent.com/102028778/159899237-b1612507-cfca-4ac8-816a-65cbba823ad2.png">
<img width="534" alt="image" src="https://user-images.githubusercontent.com/102028778/159899363-35f62a41-1e13-4f95-bfbc-4ec9ec9daa10.png">

### * 설명
> ANIMAL_INS테이블에서 ANIMAL_ID, NAME컴럼을 조회하지만 
> INTAKE_CONDITION컴럼이 AGED가 아닌 것을 조건으로 두기 때문에 <>을 써서 Where절을 완성하고
> 마지막으로 ANIMAL_ID를 오름차순(ASC)로 계산한다.
### * 답안
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS 
WHERE INTAKE_CONDITION <> 'Aged'
order by ANIMAL_ID ASC;
## 동물의 아이디와 이름
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159849064-a9978ce9-5bea-40d1-85a1-b4d025b17b63.png">

### * 설명
> ANIMAL_INS테이블에서 ANIMAL_ID, NAME컬럼을 가져오고 ANIMAL_ID를 오름차순(ASC)로 정렬한다.
### * 답안
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS 
order by ANIMAL_ID ASC;
## 여러 기준으로 정렬하기
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159849412-d3ea3322-7f02-4e63-b873-a01083cabdcc.png">
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159849617-cb7af358-04a5-4972-9d9e-3728736b7d33.png">

### * 설명
> ANIMAL_INS테이블에서 ANIMAL_ID,NAME,DATETIME을 가져오는데 
> NAME을 먼저 오름차순(ASC)으로 정렬을 하고 바로 DATETIME을 내림차순(DESC)을 해 가져오는 것이다.
### * 답안
SELECT ANIMAL_ID, NAME,DATETIME
FROM ANIMAL_INS 
order by NAME ASC,DATETIME DESC
## 상위 n개 레코드
<img width="527" alt="image" src="https://user-images.githubusercontent.com/102028778/159903040-8671d2c9-b2b2-42e2-854b-62dbc8b1f911.png">
<img width="527" alt="image" src="https://user-images.githubusercontent.com/102028778/159903099-4cb4e2e7-6edb-4dbf-8b91-f1ad3d96435d.png">

### * 설명
> 테이블을 조회할 때 SELECT * 
FROM ANIMAL_INS 
ORDER BY DATETIME으로 DATETIME을 오름차순으로 정렬하여 DATETIME이 가장 빠른 시간으로 정렬하고, Where절에서 ROWNUM < 2를 써 상위 1개 값 NAME 컬럼만 조회한다.
### * 답안
SELECT NAME
FROM (SELECT * 
FROM ANIMAL_INS 
ORDER BY DATETIME) 
WHERE ROWNUM < 2;
