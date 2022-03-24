# Programmers_SQL_Select
* 사이트명 : 프로그래머스(Programmers)
* SQL : Oracle
* 난이도 : 하
## 모든 레코드 조회하기
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159735880-3e0eba1d-08b9-4953-b492-da2475404def.png">

| NAME | TYPE | NULLABLE |
|------|------|------|
| ANIMAL_ID | VARCHAR(N) | FALSE |
| ANIMAL_TYPE | VARCHAR(N) | FALSE |
| DATETIME | DATETIME |FALSE|
| INTAKE_CONDITION | VARCHAR(N)| FALSE |
| NAME|VARCHAR(N) | TRUE| 
| SEX_UPON_INTAKE | VARCHAR(N) | FALSE | 
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

## 아픈 동물 찾기

## 어린 동물 찾기

## 동물의 아이디와 이름

## 여러 기준으로 정렬하기

## 상위 n개 레코드
