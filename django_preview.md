# **Django**

### MTV : 개발 규칙

- MODEL : 데이터의 표현

  - 역할 : 명세 +관리 (CRUD)

- Web Service의 목적
  - 사용자가 Data를 관리
- ORM : 프로그래밍 언어를 SQL 언어로 변환

  - (Object Relational Mapping)

- View : Controller
  - 역할 : 요청처리 & 결과 반환 (응답 :response )

### Response 종류

1. Data : JSON / XML (정보만 전달할 때)
2. Page (Template) : HTML / CSS / JAVA SCRIPTS 등 화면과 함께 전달해야 할 때

### APP

- APP은 프로젝트를 구성하는 하나의 모듈
- <개발순서>

  - 1. 반드시 모델부터 개발!
  - 2. 이후 View /Template 원하는 것 (모델이 가장 1순위 개발)

- 테이블은 tb\_ 를 붙힌다

- ALTER : 메타데이터 변경 (CREATE를 만든것을 변경 할 때)
-

### **method** : 어떤 '방식'으로 데이터를 보낼 것인가

- 사전적 의미

  - GET : 가지고 오는것
  - POST : 데이터 등록

- GET 방식 : URL에 실어서 보낸다. **일반적**으로 Query String 활용
  - Path parameter 도 사용
    - **Parameter** : 클라이언트가 서버에게 보내는 값
- POST 방식 : Body에 실어서 보낸다.

#### GET 방식의 장단점

- 장점 : 가볍고 빠르다.(서칭 등에 사용)
- 단점 :
  - 1. 보안에 취약,
  - 2. 데이터 제약 & 큰 데이터 전송 X (Text 데이터만 가능)

#### POST 방식의 장단점

- 장점 :
  - 1. 보안에 취약 X
  - 2. 큰 데이터 전송 가능 (Text , 사진 등등 여러 데이터 전송 가능)
- 단점 : 무겁고 느리다.

#### API

- API 의 의미
  - Application : 프로그램
  - Programing : 제어
  - Interface : 창구

#### URL URL URM

- **URI** : http://www.naver.comwebtoon/web (scheme + host + path)
- **URL** : www.naver.com/webtoon/web (HOST + Path) (스킴이 없음)
- **URN** : webtoon/web (path) (스킴 호스드 없음)

- Form 을 전달하기 위해선 CSRF 토큰을 만들어야 한다

  - 부여 방식: {% csrf_token %}

- Attribute : Server 가 Clinet 에게 보여 줄 데이터
  - **{{ }}** :(Expression Block) 표현식 블록 : 출력을 담당 python 코드를 HTML 로 표현
  - **{% %}** :Syntax Block :문법 블록(파이썬)

_hash 알고리즘을 통해 암호화 (비밀번호 등)_

- session : 서버가 클라이언트의 정보를 저장하는 공간

  - 삭제 방법

  1. 브라우저 종료
  2. 시간

  - session 공간에 사용자의 정보가 들어있지 않으면 로그인 X
  - session은 처음 request 하는 순간(접속(로그인)) session 공간이 생긴다. (서버 내에)

- Cookile : 클라이언트의 공간
- redirect : URL로 이동 시켜주는 함수

#### FORM 커스터마이징

- id.\_for_label =아이디 속성값 (id_password , id_user_id)
- input_type = text, password, email

#### widget : input 태그의 타입

#### 설계 방법

1. 설계
   - 어떤 Data를 사용할 것인가?
2. Data Io 가 잘 되는 지 확인
   - IO : Input & Output
3. 재 설계
   - 이 데이터를 이용해서 어떻게 구현할 지

- 위 내용을 반복
