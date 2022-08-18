# PostProject
sparta 3주차 개인 과제입니다.


## 클래스 설명
```
Controller
-PostController: post의 생성, 조회, 삭제, 수정 등의 기능을 제어하는 컨트롤러

Service
-PostService: Postcontroller에게서 받은 요청을 수행한 후 결과를 넘겨준다.

Domain
-Post: 게시물 객체
-Timestamped: 생성일자, 수정일자를 자동으로 갱신하고 만들어준다.

Dto
-PostResponseDto: post목록을 반환할 때의 정보를 담고있는 dto
-ResponseDto: post의 정보를 전달하는 dto
-PostRequestDto: request 정보를 담아 전달하는 dto

Repository
- PostRepository: DB에서 Post를 관리하는 repository. post 리스트를 최신순으로 정렬하여 반환하는 역할도 있음
```  
  
```
통일된 형식을 위한 클래스

-ExceptionController: ID관련 오류 발생 시 가로채서 설정한 에러메시지를 반환하도록 한다.

-ResponseService: Controller가 전달해준 에러 메시지를 형식에 맞게 담아서 반환한다.

-CommonResponse: Response 형식을 정의한 객체.
-Exception: ID가 없는 오류 발생시 에러메시지를 설정하는 enum

-ErrorDto: 설정해둔 에러메시지인 code와 message를 담고있는 dto
```  
  
    
##  Q&A
```
1. 수정, 삭제 API의 request를 어떤 방식으로 사용하셨나요? (param, query, body)
```
id는 @PathVariable 어노테이션을 사용하여 param 방식으로 id를 가져온 뒤
query문을 이용하여 DB에 일치하는 POST 객체를 찾아낸다.
여기서 삭제는 바로 그 객체를 삭제만 하면 되고 수정은 body에 담아온 내용으로 update한다.
  
```
2. 어떤 상황에 어떤 방식의 request를 써야하나요?
```
JSON과 같은 데이터를 요청할 때에는 body를 사용하고 url값에서 숫자나 짧막한 값을 가져올 때에는 param을 사용한다. param은 이번 과제의 지정한 게시물의 조회, 수정, 삭제 등과 같이 url로 특정 객체를 지정할 때 주로 사용된다. query란 특정 조건으로 조회하고 싶을 때 규칙에 맞게 문자열을 작성하면 그대로 반환해주는 것이다. 특정 객체를 DB에서 찾거나, 규칙에 맞춰 리스트를 반환할 때 사용된다.
  
```
3. RESTful한 API를 설계했나요? 어떤 부분이 그런가요? 어떤 부분이 그렇지 않나요?
```
Get, Post, Put, Delete를 상황에 맞게 사용하였다. 자원인 Post를 사용하여 표현하였다. 다만 비밀번호 대조는 다른 이름을 사용하여 구별해야했을까 라는 생각이 든다.
  
```
4. 적절한 관심사 분리를 적용하였나요? (Controller, Repository, Service)
```
  controller에서는 입력을 받고 결과를 응답하는 용도로만 사용하였고  
  service에서 요구사항에 맞게 동작하여 controller 결과를 전달하였다.  
  repository는 DB 자원관리 역할만을 수행하였다.  
  또한 Post와 통일된 형식을 위해 만든 Repsonse 두 가지에서 또 각각의 컨트롤러와 서비스, 리포지토리를 만들어주었다.  
    
    
```
5. 작성한 코드에서 빈(Bean)을 모두 찾아보세요!
```
  Controller 2개, Service 2개, Repository 1개 총 5개이다.  
  
  
```
6. API 명세서 작성 가이드라인을 검색하여 직접 작성한 명세서와 비교해보세요!
```
  나와 같이 기능에 대한 설명이 있는 명세서도 있고 없는 명세서도 있었고,  
  Request와 Response를 나처럼 입력과 출력 그대로 적는 명세서도 있었고 타입만 적는 명세서도 있었다.  
  디테일이 사람마다 조금씩 차이가 있는 것 같다.  
    
    
    
## 배포 ip
  13.209.88.187  
    
      
    
## 유스케이스 및 API 명세서
https://yonykk.tistory.com/20
