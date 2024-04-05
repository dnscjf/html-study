# 1. HTML

## 1.1 HTML 구조 파악하기

```html
<!-- 1. 현재 문서가 HTML 언어를 작성한 웹 문서라는 의미 -->
<!DOCTYPE html>
<!-- 2. <html> ~ </html> 웹 문서의 시작과 끝을 나타내는 태그 -->
<html lang="ko">
    <!-- 3. <head> ~ </head> 웹 브라우저가 웹 문서를 해석하는데 필요한 정보를 입력하는 부분 -->
<head>
    <!-- 메타정보 : 데이터 관련 -->
    <!-- 한글 인코딩을 명시하는 태그 -->
    <!-- 웹 사이트의 키워드나 간단한 설명, 제작자 등의 정보를 지정 -->
    <!-- 검색 엔진에서 사이트를 검색할 때 차고 -->
    <meta charset="UTF-8">
    <!-- 반응형을 위한 메타 태그 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 웹 문서의 키워드 -->
    <meta name="keywords" content="html의 구조"/>
    <!-- 웹 문서의 설명 -->
    <meta name="description" content="html의 구조를 알아봅시다"/>
    <meta name="author" content="dnscjf"/>
    <!-- 타이틀 태그 : 웹 문서의 제목, 웹 브라우저의 제목 표시줄에 표시 -->
    <!-- 웹 사이트의 즐겨찾기를 지정할 때도 웹 문서 제목으로 추가 -->
    <title>HTML 구조파악하기</title>
</head>
<body>
    <div>
        <header>
            <h1>헤더입니다</h1>
        </header>
        <main>
            <h2>프론트엔드 웹 개발</h2>
            <hr />
            <p>HTML</p>
            <p>CSS</p>
            <p>Javascript</p>
            <p>React</p>
        </main>
        <footer>
            <h3>푸터입니다</h3>
        </footer>
    </div>
</body>
</html>
```

## 1.2 웹 문서 구조를 만드는 시맨틱 태그

- 웹사이트 구조는 헤더, 본문, 푸터, 사이드 바
- 시맨틱 태그 Can I use 사이트 참고
- main 태그 : 웹 문세에서 핵심이 되는 내용, 웹 문서마다 다르게 보여주는 내용으로 구성, 웹 문서에 한번만 사용할 수 있음
- articla 태그 : 블로그의 포스트나 뉴스 사이트의 기사처럼 독립된 웹 콘텐츠 항목 여러개 사용가능
- section 태그 : 웹 문서의 콘텐츠 영역을 나타냄, articla은 독립된 콘텐츠, section은 몇개의 콘텐츠를 묶는 용도
- aside 태그 : 사이드바 만들 때 필요한 경우에 사용
- footer 태그 : 웹 문서 맨 아래쪽에 있는 푸터 영역을 만든다. 웹 사이트의 정보, 저작권 정보, 연락처 등을 넣음
- div 태그 : 영역을 나눔

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>시맨틱 태그</title>
</head>
<body>
    <!-- 헤더 영역 -->
    <header>
        <!-- 로고 영역 -->
        <div>
            <a href="#"><h1>Dream Jeju</h1></a>
        </div>
        <hr />
        <!-- 내비게이션 영역 -->
        <nav>
            <li><a href="#">단체 여행</a></li>
            <li><a href="#">맞춤 여행</a></li>
            <li><a href="#">갤러리</a></li>
            <li><a href="#">문의하기</a></li>
        </nav>
        <hr />
    </header>
    <!-- 메인 영역 -->
    <main>
        <section>
            <h2>몸과 마음이 치유되는 섬</h2>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic consequatur sequi voluptate esse exercitationem odit vel molestias quisquam! Quo totam in voluptatibus quos officiis velit nostrum obcaecati, labore nam exercitationem?
        </section>
        <section>
            <h2>다양한 액티비티가 기다리는 섬</h2>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic consequatur sequi voluptate esse exercitationem odit vel molestias quisquam! Quo totam in voluptatibus quos officiis velit nostrum obcaecati, labore nam exercitationem?
        </section>
    </main>
    <!-- 푸터 영역 -->
    <footer>
        <div>
            <ul>
                <li> <a href="#">회사 소개</a></li>
                <li> <a href="#">개인 정보 처리 방침</a></li>
                <li> <a href="#">여행약관</a></li>
                <li> <a href="#">사이트맵</a></li>
            </ul>
        </div>
    </footer>
</body>
</html>
```

## 1.3 웹 문서에 다양한 내용 입력하기

### 1.3.1 텍스트 입력하기

- 제목을 나타내는 h태그
- 텍스트 단락을 만드는 p태그, 줄바꿈 br 태그
- 인용할 때 쓰는 blockquote 태그
- 텍스트를 굵게 표시 strong, b
- 기울인 텍스트를 입력해주는 em, i

### 1.3.2 목록 만들기

- 순서 있는 목록 ol, li

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>제목을 나타내는 h태그</title>
</head>
<body>
    <h1>레드향</h1>
    <p>껍질에 붉은 빛이 돌아 <b>레드향</b>이라 불린다.</p>
    <p>
        레드향은 <em>한라봉과 귤을 교배</em>한 것으로<br />
        <b>일반 귤보다 2~3배 크고, 과육이 붉고 통통하다.</b>
    <p>
        비타민 C와 비타민 P가 풍부해<br />
        혈액순환, 감기예방 등에 좋은 것으로 알려져 있다.
    </p>
    <blockquote>
        <i>비타민 C</i>와 <i>비타민 P</i>가 풍부해<br />
    <strong>혈액순환, 감기예방</strong> 등에 좋은 것으로 알려져 있다.
    </blockquote>
    </blockquote>
    <h2>레드향 샐러드 레시피</h2>
    <h3>상품 구성</h3>
</body>
</html>
```

- 순서 있는 목록 ol, li
- 순서가 없는 목록 ul, li
- 설명 목록을 만드는 di, dt, dd 태그 d1 : description list, dt: 제목, dd: 값(설명)

### 1.3.3 표 만들기

### 1.2.4 이미지 삽입

### 1.2.5 오디오와 비디오 삽입하기

- 멀티미디어 파일을 삽입할 때 쓰는 object, embed 태그
- audio, vedio
- a 태그 새창으로 이동하기 target="\_blank"

## 1.4 입력 양식 작성하기

### 1.4.1 폼 삽입하기

- 아이디, 비밀번호 입력
- 로그인, 회원가입
- 쇼핑몰 주문
- 커뮤니티 등등...
- form 태그 속성
    - method: get, post
    - name: 자바스크립트로 폼을 제어할 때 사용할 폼의 이름을 지정
    - action: form 태그 안의 내용을 처리해줄 서버 프로그램 지정
    - target: action 속성에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에서 열도록 함
- 폼 요소를 그룹으로 묶는 fildeset, legend 태그
- 폼 요소에 레이블을 붙이는 label 태그

### 1.4.2 사용자 입력을 위한 input 태그

- input 태그의 type 속성
    - text : 한줄 짜리 텍스트, 텍스트 박스
    - password : 비밀번호  필드
    - search : 검색
    - URL : URL 주소 입력
    - email : 이메일 주소
    - tal : 전화번호
    - checkbox : 체크박스(중복 체크 가능)
    - radio : 라디오버튼 (하나만 체크)
    - number : 숫자
    - range : 숫자를 조절할 수 있는 슬라이드 막대
    - date : 사용자 지역을 기준으로 날짜(연, 월, 일)
    - month : 연, 월
    - week : 연, 주
    - time : 시, 분, 초, 분할초
    - datetime : 국제표준시(UTC) 설정된 날짜와 시간 (연, 월, 일, 시, 분, 초, 분할초)
    - datetime-local : 사용자 지역을 기준으로 datetime
    - sumbit : 전송 버튼
    - reset : 리셋 버튼
    - image : sumbit 버튼 대신 사용할 이미지
    - button : 일반 버튼
    - file : 파일을 첨부할 수 있는 버튼
    - hidden : 사용자에게 보이지 않지만 서버로 넘겨주기 위한 값이 있는 필드

