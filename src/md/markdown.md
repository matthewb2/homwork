# HTML 주요 태그 및 문법 정리

웹 개발 초보자부터 중급자까지 참고할 수 있는 HTML 기본 정리입니다.

---

## 1. HTML 기본 구조

HTML 문서는 기본적으로 아래와 같은 구조를 가집니다.
태그는 대소문자 구분이 없습니다.  
태그는 대부분 쌍으로 존재합니다 (&lt;div&gt;내용&lt;/div&gt;), 일부는 단독으로 존재하기도 합니다(&lt;br&gt;)  
속성 값은 따옴표 사용를 사용합니다 (&lt;img src="img.png"&gt;)  
중첩 구조가 중요합니다 (열린 태그 안에서 닫힌 태그 순서)  
HTML5에서는 시맨틱 태그 사용을 권장합니다

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>문서 제목</title>
  </head>
  <body>
    <h1>안녕하세요</h1>
    <p>HTML 문서 예제입니다.</p>
  </body>
</html>
```

&lt;!DOCTYPE html&gt; : 문서가 HTML5임을 선언합니다  
&lt;html&gt; : HTML 문서의 루트 요소입니다  
&lt;head&gt; : 헤더 태그 안에는 메타데이터, 제목, CSS, JS 링크 등을 포함시킬 수 있습니다  
&lt;body&gt; : 화면에 보여지는 콘텐츠입니다

## 2. 텍스트 관련 태그

```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>텍스트 태그 예제</title>
</head>
<body>
  <!-- 제목 태그 -->
  <h1>h1: 가장 큰 제목</h1>
  <h2>h2: 두 번째 제목</h2>
  <h3>h3: 세 번째 제목</h3>

  <!-- 문단 -->
  <p>p: 일반 문단 텍스트입니다.</p>

  <!-- 강조 -->
  <p><strong>strong:</strong> 중요한 내용은 굵게 표시됩니다.</p>
  <p><em>em:</em> 내용은 기울여 강조합니다.</p>

  <!-- 줄바꿈, 구분 -->
  <p>줄바꿈 전<br>줄바꿈 후</p>
  <hr>

  <!-- 인라인 텍스트 스타일 -->
  <p><b>b:</b> 굵은 글씨 (단순히 시각 효과)</p>
  <p><i>i:</i> 기울임꼴 (단순히 시각 효과)</p>
  <p><u>u:</u> 밑줄</p>
  <p><mark>mark:</mark> 형광펜처럼 강조</p>
  <p><small>small:</small> 작은 글씨</p>
  <p><del>del:</del> 삭제된 텍스트</p>
  <p><ins>ins:</ins> 새로 삽입된 텍스트</p>
  <p>위첨자: E = mc<sup>2</sup></p>
  <p>아래첨자: H<sub>2</sub>O</p>

  <!-- 인용문 -->
  <blockquote>blockquote: 문단 단위 인용문</blockquote>
  <q>q: 짧은 인라인 인용</q>

  <!-- 코드 -->
  <p>인라인 코드: <code>console.log("Hello")</code></p>
  <pre>
    여러 줄 코드 블록:
    for (let i=0; i<3; i++) {
      console.log(i);
    }
  </pre>
</body>
</html>
```

&lt;h1&gt; ~ &lt;h6&gt; 제목 태그, 숫자가 작을수록 큰 제목 `<h1>대제목</h1>`  
&lt;p&gt; 문단 `<p>문단 내용</p>`  
&lt;br&gt; 줄바꿈 `줄1<br>줄2`  
&lt;hr&gt; 수평선 `<hr>`  
&lt;strong&gt; 굵은 글씨, 의미 강조 `<strong>중요</strong>`  
&lt;em&gt; 기울임 글씨, 의미 강조 `<em>강조</em>`  
&lt;span&gt; 인라인 영역, 스타일 적용용 `<span style="color:red;">빨강</span>`  
&lt;div&gt; 블록 영역, 레이아웃용 `<div>블록 영역</div>`

## 3. 링크, 이미지, 리스트

```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>HTML 태그 예제</title>
</head>
<body>
  <!-- 링크 -->
  <p><a href="https://www.google.com" target="_blank">구글로 이동</a></p>

  <!-- 이미지 -->
  <p><img src="https://via.placeholder.com/150" alt="샘플 이미지"></p>

  <!-- 리스트 -->
  <h3>순서 없는 리스트</h3>
  <ul>
    <li>사과</li>
    <li>바나나</li>
    <li>포도</li>
  </ul>

  <h3>순서 있는 리스트</h3>
  <ol>
    <li>첫 번째</li>
    <li>두 번째</li>
    <li>세 번째</li>
  </ol>
</body>
</html>
```

&lt;a&gt; 링크 `<a href="https://www.example.com">예제 사이트</a>`  
&lt;img&gt; 이미지 `<img src="image.png" alt="설명">`  
&lt;ul&gt; 순서 없는 리스트 `<ul><li>아이템1</li></ul>`  
&lt;ol&gt; 순서 있는 리스트 `<ol><li>첫번째</li></ol>`  
&lt;li&gt; 리스트 아이템 `<li>항목</li>`

## 4. 테이블

```html
<table border="1">
  <thead>
    <tr>
      <th>이름</th>
      <th>나이</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>홍길동</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
<table>
  : 테이블 전체
</table>
```

&lt;tr&gt; : 테이블 행  
&lt;th&gt; : 헤더 셀  
&lt;td&gt; : 데이터 셀

## 5. 폼(form) 관련 태그

```html
<form action="/submit" method="post">
  <label for="name">이름:</label>
  <input type="text" id="name" name="name" required />
  <input type="submit" value="제출" />
</form>
```

&lt;form&gt; : 폼 영역  
action : 제출할 URL  
method : GET/POST  
&lt;input&gt; : 입력 필드 (type=text, password, submit 등)  
&lt;label&gt; : 입력 필드 설명  
&lt;textarea&gt; : 여러 줄 입력  
&lt;select&gt; / &lt;option&gt; : 드롭다운

## 6. 기타 유용한 태그

&lt;meta&gt; 문서 정보 &lt;meta charset="UTF-8"&gt;  
&lt;link&gt; CSS 파일 연결 &lt;link rel="stylesheet" href="style.css"&gt;  
&lt;script&gt; JS 파일/코드 &lt;script src="app.js"&gt;&lt;/script&gt;  
&lt;iframe&gt; 다른 페이지 삽입 &lt;iframe src="page.html"&gt;&lt;/iframe&gt;  
&lt;video&gt; / &lt;audio&gt; 미디어 삽입 &lt;video src="video.mp4" controls&gt;&lt;/video&gt;

## 7. HTML5 시맨틱 태그

##### 1. &lt;header&gt;

설명: 문서 전체나 특정 구역(예: section, article)의 머리말을 나타냅니다.  
용도: 로고, 제목, 소개글, 네비게이션 메뉴 등이 포함될 수 있음.  
주의: 페이지 전체에 하나만 쓰는 것이 아니라, &lt;article&gt;이나 &lt;section&gt; 안에도 들어갈 수 있습니다.

##### 2. &lt;footer&gt;

설명: 문서 전체나 특정 구역의 바닥글을 나타냅니다.  
용도: 저작권 정보, 연락처, 관련 링크, 저자 정보 등을 포함.  
주의: 페이지 전체의 footer뿐 아니라 각 &lt;article&gt;의 끝에도 둘 수 있습니다.

##### 3. &lt;main&gt;

설명: 문서의 주요 콘텐츠 영역을 나타냅니다.  
용도: 본문 내용이 들어가는 가장 핵심 부분.  
특징: 페이지에서 한 번만 사용 가능(반복 불가). 사이드바, 헤더, 푸터, 네비게이션은 포함하지 않음.

##### 4. &lt;section&gt;

설명: 문서의 주제별 구획을 정의합니다.  
용도: 관련 있는 콘텐츠 묶음. 예: "공지사항", "추천 글", "서비스 소개".  
특징: 일반 &lt;div&gt;와 달리 제목(&lt;h1&gt;~&lt;h6&gt;)을 함께 포함하는 것이 바람직합니다.

##### 5. &lt;article&gt;

설명: 독립적으로 배포 가능하거나 재사용 가능한 콘텐츠를 나타냅니다.  
용도: 블로그 글, 뉴스 기사, 포럼 글, 리뷰 등.  
특징: 문맥이 달라도 의미가 유지되는 독립적인 콘텐츠 단위.

##### 6. &lt;nav&gt;

설명: 내비게이션 링크 모음을 나타냅니다.  
용도: 메뉴, 목차, 페이지 네비게이션.  
특징: 주요 네비게이션에만 쓰는 것이 권장되며, 푸터 속 단순한 링크 모음에는 꼭 쓰지 않아도 됩니다.
