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
### 설명
> ANIMAL_INS 테이블에서 모든 컬럼을 가져오고
ANIMAL_ID를 정렬해서 가져오는 문제이다.
방법은 Select *를 통해 모든 칼럼을 가져오고
Order By ANIMAL_ID를 넣어
ANIMAL_ID를 정렬하여 조회하면 된다.

### 답안
Select * 
From ANIMAL_INS 
Order By ANIMAL_ID ASC;


## 역순 정렬하기
![image](https://user-images.githubusercontent.com/102028778/159832128-4c0db837-5da5-44b9-b651-a7cde0f71999.png)
### 설명
> ORDER BY DESC역순정렬(내림차순)<->ORDER BY ASC(오름차순)
위, 문제와 비슷하며 위에는 오름차순 이 문제는 역순으로 내림차순(DESC)를
사용한다.

## 답안
SELECT NAME,DATETIME from ANIMAL_INS order by ANIMAL_ID DESC;


## 아픈 동물 찾기
![image](https://user-images.githubusercontent.com/102028778/159832686-d64bc52b-21fb-4095-8a07-9ad21e440dcc.png)
### 설명
> 

## 어린 동물 찾기

## 동물의 아이디와 이름

## 여러 기준으로 정렬하기

## 상위 n개 레코드
