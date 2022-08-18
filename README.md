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

```
2. 어떤 상황에 어떤 방식의 request를 써야하나요?
```

```
3. RESTful한 API를 설계했나요? 어떤 부분이 그런가요? 어떤 부분이 그렇지 않나요?
```

```
4. 적절한 관심사 분리를 적용하였나요? (Controller, Repository, Service)
```

```
5. 작성한 코드에서 빈(Bean)을 모두 찾아보세요!
```

```
6. API 명세서 작성 가이드라인을 검색하여 직접 작성한 명세서와 비교해보세요!
```

## 배포 ip
13.209.88.187

## 유스케이스 및 API 명세서
https://yonykk.tistory.com/20
