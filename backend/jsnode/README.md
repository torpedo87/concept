# nodejs
- 웹브라우저에서만 사용하던 js를 서버(runtime)쪽에서 사용할 수 있게 됨
- 하나의 언어로 웹애플리케이션을 구현 가능
- 파일 읽고쓰기(FS), 네트워크(HTTP), 운영체제(OS) 기능제공

---

# nodejs 가 제공하는 module (http, os)
- 부품처럼 갖다 쓸 수 있게 만든 것
- require('http')    //require 함수로 http 모듈 호출
- [모듈 사용설명서 링크](https://nodejs.org/dist/latest-v6.x/docs/api/)
- npm 앱스토어에서 모듈(express, underscore, jade) 다운받아서 사용
- supervisor(변경사항을 watch하여 자동으로 node를 재부팅하는 모듈)
- multer(파일 업로드 모듈)

---
# npm (node package manager)
- nodejs에서 타인의 모듈을 가져와 사용할 수 있게 하는 연결고리
- node계의 앱스토어
- 설치, 삭제, 업그레이드, 의존성 관리
- uglifyjs(불필요한 공백제거하고 코드를 간결하게 하는 앱)
- underscore
- fs(파일 저장, 읽기)

---
# callback 함수
- sort(b) 함수는 함수 b를 인자값으로 받는다
- 이때 함수 b는 콜백함수라 한다.
- 내가 b를 호출하는 것이 아니라 sort함수가 필요할때마다 알아서 b를 호출한다

# 비동기
- nodejs가 single thread이지만 빠른 속도를 갖는 이유
- nodejs 의 일처리 방식 철학은 비동기
- 동기(여러명에게 이메일 보낼때 한명씩 보내주기)
- 비동기(이메일 보내주는 업체에 맡기고 다른일 하고있다가 이메일 다 보냈으면 콜백함수 호출)

---
# express
## nodejs로 웹서버 만들때 사용하는 웹 프레임워크

## 라우팅(웹페이지별 길 찾아주기)
- 사용자-> 라우터(get) -> controller(send)

## template 엔진(jade, handlebar)
- express가 사용하는 모듈
- html에서 js 동작시키는 방법
- 정적페이지와 동적페이지의 단점들을 보완
- 정적페이지(순수html)는 js를 못쓰니까 변경시 힘들어
- 동적페이지는 js 내에서 html 다루기가 까다롭다(\`를 사용해도 되지만 지저분함)

## 쿼리스트링(home/?id=1&name=jun)
- ? 뒤의 내용이 쿼리스트링
- 라우팅되는 페이지가 쿼리스트링에 따라 다른 정보를 가져오도록
- req.query.id, req.query.name 으로 url정보 가져올 수 있다
- url의 정보 전달

## 시맨틱 url(home/1)
- 라우팅페이지 자체에 쿼리스트링을 넣어서 깔끔한 url
- query 대신에 params(parameters) 사용
- restful api 참고
---
# 사용자로부터 데이터를 전송받는 방법
## 1. get (url을 통해 정보전달)
- 주소 입력해서 정보를 가져오는 것
- html의 form 태그 get방식(사용자 입력값을 쿼리스트링을 통해 전달)

## 2. post (url 이외의 수단을 통한 정보전달)
- 사용자의 정보를 서버로 전달(로그인 정보 등등)
- url의 한계 극복(긴내용, 보안성 내용 전달시 사용)
- html의 form 태그 post방식(url이 아닌 body를 통해 전달)
- req.query 대신에 req.body 를 사용(이때 미들웨어 bodyparser 필요)
---

# database
## 관계형(oracle, mysql, sql server)
### mysql
- 

## 비관계형(nosql)

---
