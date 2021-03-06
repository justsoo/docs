# docs-markdown

https://gist.github.com/ihoneymon/652be052a0727ad59601
https://heropy.blog/2017/09/30/markdown/
https://steemit.com/kr/@antares007/-201787t14245290z
https://gist.github.com/ninanung/6691b7d68a4c1b815c0cc85693929ca3

## 목록
* [제목](#제목)
* [호라이즌](#호라이즌)
* [리스트](#리스트1)
	* [리스트1](#리스트1)
	* [리스트2](#리스트2)
* [인용](#인용)
* [개행](#개행)
* [문자강조](#문자강조)
* [링크](#링크)
* [이미지넣기](#이미지넣기)
* [블럭](#블럭)
* [테이블](#테이블)

## 제목
### 코드
```
# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6
```

### 뷰
![제목](https://github.com/justsoo/docs-markdown/blob/master/images/title_1.PNG?raw=true)
--------------------------------------------------------------------------------------------------

## 호라이즌
### 코드
```
***
---
___
--------------------------------------------------------------------------------------------------
```
### 뷰
![호라이즌](https://github.com/justsoo/docs-markdown/blob/master/images/horizion_1.PNG?raw=true)

## 리스트1
### 코드
```
* 리스트
  * 서브 리스트ㄹ
    * 서브 리스트

+ 리스트
  + 서브 리스트
    + 입 리스트

- 리스트
- 리스트
- 리스트
```
### 뷰
![리스트1](https://github.com/justsoo/docs-markdown/blob/master/images/list_1.PNG?raw=true)

## 리스트2
### 코드
```
1. 첫번째
	1. 서브
	2. 서브
2. 두번째
	1. 서브
		1. 서서브
		2. 서서브
	1. 서브
3. 세번째
	+ 서브
	+ 서브
```
### 뷰
![리스트2](https://github.com/justsoo/docs-markdown/blob/master/images/list_2.PNG?raw=true)	
	
## 인용
### 코드
```
> 인용구문 1
>> 인용구문 2
>>> 인용구문 3
>>>> 인용구문 4

> # 타이틀 인용
> * 리스트
> * 서브 리스트는 안됨

> `블럭`
```
### 뷰
![인용문](https://github.com/justsoo/docs-markdown/blob/master/images/quotation_1.PNG?raw=true)	

## 개행
### 코드
```
첫번째 줄(스페이스)(스페이스)    
두번째 줄(스페이스)(스페이스)    
세번째 줄(스페이스)(스페이스)  


첫번째 줄

두번째 줄

세번째 줄
```
### 뷰
![개행](https://github.com/justsoo/docs-markdown/blob/master/images/newline_1.png?raw=true)	


## 문자강조
### 코드
```
*이탤릭1*(스페이스)(스페이스)    
_이탤릭2_

**볼드**(스페이스)(스페이스)    
__볼드__
```
### 뷰
![문자강조](https://github.com/justsoo/docs-markdown/blob/master/images/bold_1.png?raw=true)	


## 링크
### 코드
```
<https://github.com/justsoo/docs>

[just mark down test](https://github.com/justsoo/docs)
```
### 뷰
![링크](https://github.com/justsoo/docs-markdown/blob/master/images/link_1.PNG?raw=true)


## 이미지넣기
### 코드
```
![이미지1](./images/profile.jpg)
![이미지2](https://avatars3.githubusercontent.com/u/10492283?s=460&v=4)
![이미지3](https://avatars3.githubusercontent.com/u/10492283?s=460&v=4 "프로필 이미지")
```
### 뷰
![이미지](https://github.com/justsoo/docs-markdown/blob/master/images/image_1.png?raw=true)	



## 블럭
### 코드
~~~
```
 for (int i = 0; i < 5; i++)
 {
     Console.WriteLine(i);
 }
```
~~~

```
~~~
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}
~~~
```

~~~
```c#
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}
```
~~~
### 뷰
![블럭](https://github.com/justsoo/docs-markdown/blob/master/images/block_1.PNG?raw=true)

## 테이블
### 코드
```
헤더1|헤더2| 헤더3
----|----|---- 
컬럼(1,1)|컬럼(1,2)|컬럼(1,3)
컬럼(2,1)|컬럼(2,2)|컬럼(2,3)
컬럼(3,1)|컬럼(3,2)|컬럼(3,3)
```
### 뷰
![테이블](https://github.com/justsoo/docs-markdown/blob/master/images/table_1.PNG?raw=true)


마크업, 마크다운 둘 다 힘들다...
