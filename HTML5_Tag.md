# HTML 태그

## 💻 목차
- [글자 태그](#&#128309;-글자-태그)
- [목록 태그](#&#128309;-목록-태그)
- [테이블 태그](#&#128309;-테이블-태그)
- [이미지 태그](#&#128309;-이미지-태그)
- [오디오 태그](#&#128309;-오디오-태그)
- [비디오 태그](#&#128309;-비디오-태그)
- [입력 양식 태그](#&#128309;-입력-양식-태그)
- [공간 분할 태그](#&#128309;-공간-분할-태그)

<br />

## &#128309; 글자 태그

### ◻️ 제목

| 태그 이름 | 설명 |
| --- | --- |
| h1 | 첫 번째로 큰 제목 글자 태그 |
| h2 | 두 번째로 큰 제목 글자 태그 |
| h3 | 세 번째로 큰 제목 글자 태그 |
| h4 | 네 번째로 큰 제목 글자 태그 |
| h5 | 다섯 번째로 큰 제목 글자 태그 |
| h6 | 여섯 번째로 큰 제목 글자 태그 |

<br />

### ◻️ 본문

| 태그 이름 | 설명 |
| --- | --- |
| p | 본문 글자 태그 |
| br | 줄바꿈 태그 |
| hr | 수평 줄 태그 (가로로 그어지는 줄) |

<br />

### ◻️ 앵커

- 서로 다른 웹 페이지 사이를 이동하거나 웹 페이지 내부에서 특정한 위치로 이동할 때 사용

| 태그 이름 | 설명 |
| --- | --- |
| a | 앵커 태그  |

```html
<a href="https://github.com/KimGaeun0806">GitHub</a>
```

- **빈 링크** → a 태그는 하이퍼링크 기능을 제거하고 사용하는 경우도 있음. 하지만 웹 표준을 따르려면 href 속성을 반드시 입력해야 함. 그러므로 이동하지 않는 a 태그를 만들 때는 href 속성에 #를 입력.

```html
<a href="#">HTML 앵커 태그</a>
```

- **페이지 내부 이동 →** a 태그를 이용하여 현재 페이지 내부에서 원하는 장소로 이동.이동하기를 원하는 태그에 id 속성을 부여하고, a 태그의 href 속서에 #id 형태의 문자열 입력.
    
    아래와 같은 코드에서 a 태그 부분을 클릭하면 지정햔 id 속성이 있는 위치로 스크롤바가 자동으로 이동.
    

```html
<a href="webPage">Move to WebPage</a>
<h1 id="webPage">WebPage</h1>
```

<br />

### ◻️ 글자 형태

| 태그 이름 | 설명 |
| --- | --- |
| b | 굵은 글자 태그 |
| i | 기울어진 글자 태그 |
| small | 작은 글자 태그 |
| sub | 아래에 달라붙는 글자 태그 |
| sup | 위에 달라붙는 글자 태그 |
| ins | 밑줄 글자 태그 |
| del | 가운데 줄이 그어진 글자 태그 |

<br />

### ◻️ 루비 문자

- 한자 위에 표시되는 글자

| 태그 이름 | 설명 |
| --- | --- |
| ruby | 루비 문자 선언 태그 |
| rt | 위에 위치하는 작은 문자 태그 |
| rp | ruby 태그를 지원할 경우 출력되지 않는 태그 (ruby 태그를 지원하지 않는 웹 브라우저에서 출력)  |

```html
<ruby>
	<span>大韓民國</span>
	<rp>(</rp>
	<rt>대한민국</rt>
	<rp>)</rp>
</ruby>
```

<br />

## &#128309; 목록 태그

### ◻️ 기본 목록

| 태그 이름 | 설명 |
| --- | --- |
| ul | 순서가 없는 목록 태그 (글머리에 기호 붙음) |
| ol  | 순서가 있는 목록 태그 (글머리에 숫자 붙음) |
| li  | 목록 요소  |

```html
<ol>
	<li>목록1</li>
	<li>목록2</li>
	<li>목록3</li>
</ol>

<ul>
	<li>목록1</li>
	<li>목록2</li>
	<li>목록3</li>
</ul>
```

<br />

### ◻️ 정의 목록

- 특정 용어와 그 정의를 표현할 때 사용하는 태그

| 태그 이름 | 설명 |
| --- | --- |
| dl | 정의 목록 태그 |
| dt  | 정의 용어 태그 |
| dd  | 정의 설명 태그 |

```html
<dl>
	<dt>용어</dt>
	<dd>설명</dd>
	<dd>설명</dd>
	<dd>설명</dd>

	<dt>용어</dt>
	<dd>설명</dd>
	<dd>설명</dd>
</dl>
```

<br />

## &#128309; 테이블 태그

### ◻️ 테이블 태그 기본

- 표를 만들 때 사용

| 태그 이름 | 설명 |
| --- | --- |
| tr | 표 내부의 행 태그  |
| th | 행 내부의 제목 셀 태그  |
| td | 행 내부의 일반 셀 태그  |

```html
<table border="1">
	<tr>
		<th>Header 1</th> <!-- 첫 번째 행 --> 
		<th>Header 2</th>
	</tr>
	<tr>
		<td>Data 1</td> <!-- 두 번째 행 -->
		<td>Data 1</td>
	</tr>
	<tr>
		<td>Data 2</td> <!-- 세 번째 행 -->
		<td>Data 2</td>
	</tr>
</table>
```

<br />

### ◻️ 테이블 태그 속성

| 속성 이름 | 설명 |
| --- | --- |
| border | 표의 테두리 두께 지정 (table 태그 속성) |
| rowspan | 셀의 높이 지정 (th, td 태그 속성) |
| colspan | 셀의 너비 지정 (th, td 태그 속성) |

```html
<table border="1">
	<tr>
		<th colspan="3">Table Data</th> <!-- 가로 3칸 차지 --> 
		<th rowwpan="3">Table Data</th> <!-- 세로 3칸 차지 --> 
	</tr>
	<tr>
		<td>Table Data</td>
		<td rowspan="2">Table Data</td> <!-- 세로 2칸 차지 --> 
		<td>Table Data</td>
	</tr>
	<tr>
		<td>Data Data</td>
		<td>Data Data</td>
	</tr>
</table>
```

<br />

## &#128309; 이미지 태그

| 속성 이름 | 설명 |
| --- | --- |
| src | 이미지의 경로 지정 |
| alt | 이미지가 없을 때 나오는 글자 지정 |
| width | 이미지의 너비 지정 |
| height | 이미지의 높이 지정 |

```html
<img src="Chocolate.jpg" alt="초콜릿" width="300" />
```

- 📄 ***[placehold.it](http://placehold.it)*** → 원하는 크기의 이미지를 제공해주는 사이트

```html
<img src="http://placehold.it/300x200" /> 
```

<br />

## &#128309; 오디오 태그

### ◻️ audio 태그

- 웹 브라우저에서 플러그인의 도움 없이 음악을 재생할 수 있게 만들어줌

| 속성 이름 | 설명 |
| --- | --- |
| src | 음악 파일의 경로 지정 |
| preload | 음악을 재생하기 전에 모두 불러올지 지정 |
| autoplay | 음악을 자동 재생할지 지정 |
| loop | 음악을 반복할지 지정 |
| controls | 음악 재생 도구를 출력할지 지정  |

```html
<audio src="Balloon.mp3" controls="controls" autoplay="autoplay"></audio>
<!-- <audio src="Balloon.mp3" controls autoplay></audio> 와 같이 써도 됨-->
```

<br />

### ◻️ source 태그

- 웹 브라우저마다 지원하는 확장자 형식이 다르기 때문에 사용. audio 태그나 video 태그 안에 입력.

```html
<audio controls="controls">
	<source src="Yesterday.mp3" type="audio/mp3" />
	<source src="Yesterday.ogg" type="audio/ogg" />
</audio>
```

<br />

## &#128309; 비디오 태그

### ◻️ video 태그

| 속성 이름 | 설명 |
| --- | --- |
| src | 비디오 파일의 경로 지정 |
| poster | 비디오 준비중일 때의 이미지 파일 경로 지정 |
| preload | 비디오를 재생하기 전에 모두 불러올지 지정 |
| autoplay | 비디오를 자동 재생할지 지정 |
| loop | 비디오를 반복할지 지정 |
| controls | 비디오 재생 도구를 출력할지 지정 |
| width | 비디오의 너비 지정 |
| height | 비디오의 높이 지정  |

```html
<!-- 웹 브라우저마다 지원하는 비디오 형식이 다르므로 필요할 시 source 태그 사용 -->
<video controls="controls">
	<source src="Toy.mp4" type="video/mp4" />
	<source src="Toy.webm" type="video/webm" />
</video>
```

```html
<video poster="http://placehold.it/640x360" 
		width="640" height="360" controls="controls">
	<source src="Toy.mp4" type="video/mp4" />
	<source src="Toy.webm" type="video/webm" />
</video>
```

- 📄 ***[video.js 플러그인](http://videojs.com)***  → 웹 브라우저마다 표시되는 video 태그 형태가 일관되지 않아서 문제가 될 수 있음. 이를 해결하기 위한 플러그인.

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>

	<!-- link 태그와 script 태그는 video.js 플러그인 홈페이지에서 복사 가능 -->
	<link href="https://vjs.zencdn.net/7.17.0/video-js.css" rel="stylesheet" />
	<script src="https://vjs.zencdn.net/ie8/1.1.2/videojs-ie8.min.js"></script>
</head>

<body>
	<!-- class 속성과 data-setup 속성 입력 -->
	<video controls="controls" width="640" height="360" class="video-js" data-setup="{}">
		<source src="Toy.mp4" type="video/mp4" />
		<source src="Toy.webm" type="video/webm" />
	</video>
</body>
</html>
```

<br />

## &#128309; 입력 양식 태그

### ◻️ 입력 양식 개요

- 입력 양식은 form 태그를 사용해 생성, 입력 양식 안에는 input 태그 입력

```html
<form>
	<input type="text" name="search" />
	<input type="submit" />
</form>
```

| 속성 이름 | 설명 |
| --- | --- |
| action | 입력 데이터의 전달 위치를 지정함 |
| method | 입력 데이터의 전달 방식을 선택함 |
- 자주 사용되는 method 속성은 GET과 POST

```html
<!-- GET 요청 -->
<form method="get">
	<input type="text" name="search" />
	<input type="submit" />
</form>

<!-- 데이터를 전송했을 때 URL이 변경됨. data라고 입력했다면 
http://localhost:포트번호/폴더이름/파일이름?search=data 
형태로 변경됨. GET 방식은 이렇게 주소에 데이터를 입력해서 보내는 방식 -->
```

```html
<!-- POST 요청 -->
<form method="post">
	<input type="text" name="search" />
	<input type="submit" />
</form>

<!-- 주소가 변경되지 않음. GET 방식과 달리 비밀스럽게 데이터 전달. 
GET 방식은 데이터 크기가 한정되어 있지만 POST 방식은 용량 제한 x -->
```

<br />

### ◻️ 기본 input 태그

- 입력 양식의 형태를 지정할 때는 input 태그의 type 속성을 사용
- input 태그의 내부에 글자를 넣고 싶으면 value 속성값 입력

| 속성값 | 설명 |
| --- | --- |
| button | 버튼을 생성함 |
| checkbox | 체크박스를 생성함 |
| file | 파일 입력 양식을 생성함  |
| hidden | 보이지 않음 |
| image | 이미지 형태를 생성함 |
| password | 비밀번호 입력 양식을 생성함 |
| radio | 라디오 버튼을 생성함 |
| reset | 초기화 버튼을 생성함 |
| submit | 제출 버튼을 생성함 |
| text | 글자 입력 양식을 생성함 |
- **label 태그** → input 태그를 설명하는 데 사용됨. 어떤 input 태그를 설명하고 있는지 표시해줘야 하므로, input 태그에 id 속성을 입력하고 label 태그에 for 속성 입력.

```html
<form>
	<label for="name">이름</label>
	<input id="name" type="text" />
</form>
```

<br />

### ◻️ HTML5 입력 양식 태그

| 속성값 | 설명 |
| --- | --- |
| color | 색상 선택 양식을 생성함 |
| date | 일 선택 양식을 생성함 |
| datetime | 날짜 선택 양식을 생성함 |
| datetime-local | 지역 날짜 선택 양식을 생성함 |
| email | 이메일 입력 양식을 생성함  |
| month | 월 선택 양식을 생성함 |
| number | 숫자 생성 양식을 생성함  |
| range | 범위 선택 양식을 생성함 |
| search | 검색어 입력 양식을 생성함 |
| tel | 전화번호 입력 양식을 생성함 |
| time | 시간 선택 양식을 생성함 |
| url | URL 주소 입력 양식을 생성함 |
| week | 주 선택 양식을 생성함 |

<br />

### ◻️ textarea 태그

- 여러 줄의 글자를 입력할 때 사용

| 속성 이름 | 설명 |
| --- | --- |
| cols | 태그의 너비를 지정 |
| rows | 태그의 높이를 지정 |
- textarea 태그 안에 미리 글자를 입력하고 싶으면 textarea 태그에 글자 입력

```html
<form>
	<textarea>TextArea Text</textarea>
</form>
```

- textarea 태그에 여러 줄의 글자를 입력할 때는 아래와 같이 해야 함

```html
<form>
	<textarea>TextArea Text
TextArea Text</textarea> 
</form>
```

<br />

### ◻️ select 태그

- 여러 개의 목록에서 몇 가지를 선택할 수 있는 입력 양식 요소

| 태그 이름 | 설명 |
| --- | --- |
| select | 선택 양식을 생성함 |
| optgroup | 옵션을 그룹화함 |
| option | 옵션을 생성함 |
- 여러 개의 목록을 선택하고 싶을 때는 select 태그의 multiple 속성 사용

```html
<select multiple="multiple">
	<option>초코라떼</option>
	<option>아이스티</option>
	<option>자바칩 프라페</option>
	<option>오레오 버블티</option>
</select>
```

- outgroup 태그는 선택 옵션을 묶을 때 사용

```html
<select>
	<optgroup label="bubbleTea">
		<option>타로 버블티</option>
		<option>딸기요거트 버블티</option>
		<option>말차 버블티</option>
	</optgroup>
	<optgroup label="Latte">
		<option>바닐라 라떼</option>
		<option>딸기라떼</option>
	</optgroup>
</select>
```

<br />

### ◻️ fieldset 태그와 legend 태그

- 입력 양식을 설명하는 태그
- legend 태그는 fieldset 태그 내부에서만 사용가능

```html
<form>
	<fieldset>
		<legend>입력 양식</legend>
		<table>
			<tr>
				<td><label for="name">이름</label></td>
				<td><input id="name" type="text" /></td>
			</tr>
			<tr>
				<td><label for="mail">이메일</label></td>
				<td><input id="mail" type="email" /></td>
			</tr>
		</table>
		<input type="submit" />
	</fieldset>
</form>
```

<br />

## &#128309; 공간 분할 태그

### ◻️ div 태그와  span 태그

| 태그 이름 | 설명 |
| --- | --- |
| div | block 형식으로 공간을 분할함 |
| span | inline 형식으로 공간을 분할함 |
- block 형식은 차곡차곡 쌓아올려지는 형식임. 글자가 웹 페이지의 너비만큼 차지함.
- inline 형식은 한 줄 안에 차례차례 위치하는 형식. 글자가 한 줄에 여러 개 들어감.

| block 형식 태그 | inline 형식 태그  |
| --- | --- |
| div 태그 | span 태그 |
| h1 태그 ~ h6 태그 | a 태그 |
| p 태그 | inpur 태그 |
| 목록 태그 | 글자 형식 태그 |
| 테이블 태그 |  |
| form 태그 |  |

<br />

### ◻️ HTML5 시멘틱 구조 태그

- 기계적인 검색 엔진은 어떠한 태그가 어떠한 기능을 하는지 분별할 수 없고 웹 페이지에서 데이터를 효율적으로 추출할 수 없음
    
    → 이를 해결하고자 (기계적인 동작들이 웹 페이지를 쉽게 이해할 수 있게 하고자) 특정한 태그에 의미를 부여 
    

| 태그 이름 | 설명 |
| --- | --- |
| header | 헤더를 의미 |
| nav | 내비게이션을 의미 |
| aside | 사이드에 위치하는 공간을 의미 |
| section | 여러 중심 내용을 감싸는 공간을 의미 |
| article | 글자가 많이 들어가는 부분을 의미 |
| footer | 푸터를 의미 |