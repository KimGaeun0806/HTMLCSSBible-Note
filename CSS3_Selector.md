# CSS3 선택자

## 💻 목차
- [CSS3 선택자](#css3-선택자)
	- [💻 목차](#-목차)
	- [🔵 전체 선택자](#-전체-선택자)
	- [🔵 태그 선택자](#-태그-선택자)
	- [🔵 아이디 선택자와 클래스 선택자](#-아이디-선택자와-클래스-선택자)
		- [◻️ 아이디 선택자](#️-아이디-선택자)
		- [◻️ 클래스 선택자](#️-클래스-선택자)
	- [🔵 속성 선택자](#-속성-선택자)
		- [◻️ 기본 속성 선택자](#️-기본-속성-선택자)
		- [◻️ 문자열 속성 선택자](#️-문자열-속성-선택자)
	- [🔵 후손 선택자와 자손 선택자](#-후손-선택자와-자손-선택자)
		- [◻️ 후손 선택자](#️-후손-선택자)
		- [◻️ 자손 선택자](#️-자손-선택자)
	- [🔵 동위 선택자](#-동위-선택자)
	- [🔵 반응 선택자](#-반응-선택자)
	- [🔵 상태 선택자](#-상태-선택자)
	- [🔵 구조 선택자](#-구조-선택자)
		- [◻️ 일반 구조 선택자](#️-일반-구조-선택자)
		- [◻️ 형태 구조 선택자](#️-형태-구조-선택자)
	- [🔵 문자 선택자](#-문자-선택자)
		- [◻️ 시작 문자 선택자](#️-시작-문자-선택자)
		- [◻️ 전후 문자 선택자](#️-전후-문자-선택자)
		- [◻️ 반응 문자 선택자](#️-반응-문자-선택자)
	- [🔵 링크 선택자](#-링크-선택자)
	- [🔵 부정 선택자](#-부정-선택자)

<br />

## 🔵 전체 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| * | HTML 페이지 내부의 모든 태그를 선택 |
- body 태그 내부에 있는 요소에만 스타일 속성이 적용되는 것이 아니라 html 태그, head 태그, title 태그, style 태그까지 선택함

<br />

## 🔵 태그 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| 태그 | 특정한 태그를 선택함  |

```css
h1 { color: red; }
p { color: blue; }
```

- **여러 개의 선택자 적용 →** 여러 개의 선택자를 한꺼번에 선택해서 스타일 속성을 적용할 때는 쉼표 사용

```css
body, p, h1, h3, h6 { margin: 0; padding: 0; }
```

## 🔵 아이디 선택자와 클래스 선택자

### ◻️ 아이디 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| # 아이디  | 아이디 속성을 가지고 있는 태그를 선택함  |
- 웹 표준에 "id 속성은 웹 페이지 내부에서 중복되면 안된다”라는 규정이 있으므로 아이디 선택자는 특정한 하나의 태그를 선택할 때 사용

```css
/* 일반적으로 공간 분할 태그에 id 속성 적용하여 레이아웃 구성 */
#header { 
	width: 800px;
	margin: 0 auto;
	background: red;
} /* id 속성값으로 header을 가지는 태그의 스타일 지정 */

#wrap {
	width: 800px;
	margin: 0 auto;
	overflow: hidden;
}

#aside {
	width: 200px;
	float: left;
	background: blue;
}

#content {
	width: 600px;
	float: left;
	background: green;
}
```

```html
<div id="header">
	<h1>Header</h1>
</div>

<div id="wrap">
	<div id="aside">
		<h1>Aside</h1>
	</div>

	<div id="content">
		<h1>Content</h1>
	</div>
</div>
```

<br />

### ◻️ 클래스 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| .클래스 | 특정한 클래스를 가지고 있는 태그를 선택함 |

```css
.select { color: red; } /* class 속성값으로 select를 가지는 태그의 스타일 지정 */
```

```html
<ul>
	<li class="select">Ice Tea</li>
	<li>Hot Tea</li>
	<li class="select">Ice Tea</li>
	<li>Hot Tea</li>
</ul>
```

- **여러 개의 클래스 선택자 사용** → class 속성은 공백으로 구분해서 여러 클래스 사용 가능

```css
.item { color: red; }
.header { background-color: blue; }
```

```html
<h1 class="item header">Header</h1> /* item 클래스와 header 클래스가 함께 사용됨 */
```

- **태그 선택자와 클래스 선택자** → class 속성이 서로 다른 태그에 사용된다면, 태그 선택자와 클래스 선택자를 함께 사용해 더 정확하게 태그 선택 가능

```css
li.select { color: red; } 
/* li 태그 중 class 속성값으로 select를 가지는 태그의 스타일 지정 */
```

```html
<h1 class="select">Title</h1>

<ul>
	<li class="select">Explain</li>
	<li>Explain</li>
	<li>Explain</li>
	<li>Explain</li>
</ul>
```

## 🔵 속성 선택자

### ◻️ 기본 속성 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| 선택자[속성] | 특정한 속성이 있는 태그 선택 |
| 선택자[속성=값][속성=값] | 특정한 속성 안의 값이 특정 값과 같은 문서 객체 선택  |

```css
input[type=text] { background: red; }
input[type=password] { background: blue; }
```

```html
<!-- input 태그는 type 속성값에 따라 형태가 달라짐. 
그래서 input 태그를 선택할 때 기본 속성 선택자 많이 사용함 -->
<form>
	<input type="text" />
	<input type="password" />
</form>
```

- **기본 속성과 속성 선택자** → input 태그에 type 속성을 입력하지 않으면 자동으로 text 속성값을 적용한 형태로 출력됨. 하지만 속성 선택자는 type 속성값을 정확히 text로 입력한 태그에만 스타일 적용.

<br />

### ◻️ 문자열 속성 선택자

- 태그에 지정한 속성의 특정 문자열 확인

| 선택자 형태 | 설명 |
| --- | --- |
| 선택자[속성~=값] | 속성 안의 값이 특정 값을 단어로 포함하는 태그 선택 (ko-kr을 ko-kr로 인식) |
| 선택자[속성\|=값] | 속성 안의 값이 특정 값을 단어로 포함하는 태그 선택 (ko-kr을 ko와 kr로 인식) |
| 선택자[속성^=값] | 속성 안의 값이 특정 값으로 시작하는 태그 선택 |
| 선택자[속성$=값] | 속성 안의 값이 특정 값으로 끝나는 태그 선택 |
| 선택자[속성*=값] | 속성 안의 값이 특정 값을 포함하는 태그 선택  |

```css
img[src$=png] { border: 3px solid red; } /* img 태그 중에서 src 속성값이 png로 끝나는 태그에 스타일 지정 */
img[src$=jpg] { border: 3px solid green; }
img[src$=gif] { border: 3px solid blue; }
```

```html
<img src="zico.png" width="200" height="250" />
<img src="onew.jpg" width="200" height="250" />
<img src="winter.gif" width="200" height="250" />
```

<br />

## 🔵 후손 선택자와 자손 선택자

<img src="/sources/자손후손.png" width="300px">

```html
<div>
	<h1>CSS3 Selector</h1>
	<h2>Basic</h2>
	<ul>
		<li>Universal selector</li>
		<li>Type selector</li>
		<li>Id & Class selector</li>
	</ul>
</div>

<!-- 자손 -> div 태그를 기준으로 바로 한 단계 아래에 위치한 태그 (h1, h2, ul) -->
<!-- 후손 -> div 태그 아래에 위치한 모든 태그 (h1, h2, ul, li, li, li) -->
```

<br />

### ◻️ 후손 선택자

- 특정한 태그 아래에 있는 후손을 선택할 때 사용

| 선택자 형태 | 설명 |
| --- | --- |
| 선택자A 선택자B | 선택자A의 후손에 위치하는 선택자B를 선택 |

```css
#header h1 { color: red; } /* id 속성값으로 header를 가지는 태그의 후손 위치에 있는 h1 태그에 스타일 지정 */
#section h1 { color: orange; }
```

```html
<div id="header">
	<h1 class="title">Title</h1> <!-- red -->
	<div id="nav">
		<h1>Navigation</h1> <!-- red -->
	</div>
</div>

<div id="section">
	<h1 class="title">Title</h1> <!-- orange -->
	<p>Contents</p>
</div>
```

- **후손 선택자와 관련된 주의 사항**

```css
#header h1, h2 { color: red; }
/* #header 태그의 후손에 위치하는 h1 태그와 일반적인 h2 태그를 선택 */

#header h1, #header h2 { color: red; }
/* #header 태그의 후손에 위치하는 h1 태그와 #header 태그의 후손에 위치하는 h2 태그 선택 */
```

<br />

### ◻️ 자손 선택자

- 특정 태그 아래에 있는 자손을 선택할 때 사용

| 선택자 형태 | 설명 |
| --- | --- |
| 선택자A > 선택자B | 선택자A의 자손에 위치하는 선택자B를 선택  |

```css
#header > h1 { color: red; } 
#section > h1 { color: orange; }
```

```html
<div id="header">
	<h1 class="title">Title</h1> <!-- red -->
	<div id="nav">
		<h1>Navigation</h1> 
	</div>
</div>

<div id="section">
	<h1 class="title">Title</h1> <!-- orange -->
	<p>Contents</p>
</div>
```

- **table 태그와 자손 선택자 주의 사항** → table 태그의 요소를 선택할 때는 자손 선택자를 사용하지 않는 것이 좋음. 웹 브라우저가 table 태그에 자동으로 tbody 태그를 추가하기 때문.

<br />

## 🔵 동위 선택자

- 동위 관계에서 뒤에 위치한 태그를 선택할 때 사용

<img src="/sources/동위.png" width="300px">

```html
<ul>
	<li>Hot Chocolate</li>
	<li>Hot Chocolate</li>
	<li>Hot Chocolate</li>
	<li>Hot Chocolate</li>
	<li>Hot Chocolate</li>
</ul>

<!-- li 태그를 기준으로 할 때 모든 li 태그는 동일한 위치에 있는 동위 상태 -->
```

| 선택자 형태 | 설명 |
| --- | --- |
| 선택자A + 선택자B | 선택자A 바로 뒤에 위치하는 선택자B를 선택함 |
| 선택자A ~ 선택자B | 선택자A 뒤에 위치하는 선택자B를 선택함 |

```css
h1 + h2 { color: red; } /* h1 태그 바로 뒤에 위치하는 h2 태그 하나 선택 */
h1 ~ h2 { background-color: orange; } /* h1 태그 뒤에 위치하는 모든 h2 태그 선택 */
```

```html
<!-- 모든 태그가 동위 상태에 위치 -->
<h1>Header 1</h1>
<h2>Header 2</h2> <!-- color: red, background-color: orange -->
<h2>Header 2</h2> <!-- background-color: orange -->
<h2>Header 2</h2> <!-- background-color: orange -->
<h2>Header 2</h2> <!-- background-color: orange -->
```

<br />

## 🔵 반응 선택자

- 사용자의 반응으로 생성되는 특정한 상태 선택

| 선택자 형태 | 설명 |
| --- | --- |
| :active | 사용자가 마우스로 클릭한 태그 선택 |
| :hover | 사용자가 마우스를 올린 태그 선택 |

```css
h1:hover { color: red; }
h1:active { color:blue; }
```

<br />

## 🔵 상태 선택자

- 입력 양식의 상태를 선택할 때 사용

| 선택자 형태 | 설명 |
| --- | --- |
| :checked | 체크 상태 (type 속성값이 checkbox 혹은 radio인 input 태그가 선택된 상태)의 input 태그를 선택함  |
| :focus | 초점이 맞추어진 (사용자가 초점을 맞추고 있는 입력 양식) input 태그를 선택함 |
| :enabled | 사용 가능한 input 태그를 선택함 |
| :disabled | 사용 불가능한 input 태그 선택  |

```css
input:enabled { background-color: white; }
input: disabled { background-color: gray; }
input:focus { background-color: orange; }
```

```html
<h2>Enabled</h2>
<input />
<h2>Disabled</h2>
<input disabled="disabled" />
```

<br />

## 🔵 구조 선택자

### ◻️ 일반 구조 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| :first-child | 형제 관계 중에서 첫 번째에 위치하는 태그 선택 |
| :last-child | 형제 관계 중에서 마지막에 위치하는 태그 선택 |
| :nth-child(수열) | 형제 관계 중에서 앞에서 수열 번째에 태그 선택 (:nth-child(2n+1)라면 첫 번째, 세 번째, 다섯 번째 ... 에 위치하는 태그 선택) |
| :nth-last-child(수열) | 형제 관계 중에서 뒤에서 수열 번째에 태그 선택  |

```css
ul { overflow: hidden; }
li {
	list-style: none;
	float: left;
	padding: 15px;
}

li:first-child { border-radius: 10px 0 0 10px; }
li:last-child { border-radius: 0 10px 10px 0; }

li:nth-child(2n) {background-color:#FF0003; }
li:nth-child(2n+1) {background-color:#800000; }
```

```html
<ul>
	<li>First</li>
	<li>Second</li>
	<li>Third</li>
	<li>Fourth</li>
	<li>Fifth</li>
	<li>Sixth</li>
	<li>Seventh</li>
</ul>
```

![Untitled](CSS3%20%E1%84%89%E1%85%A5%E1%86%AB%E1%84%90%E1%85%A2%E1%86%A8%E1%84%8C%E1%85%A1%20cf52845606384025ba2ad7370d5502b5/Untitled%202.png)

- **구조 선택자와 관련된 주의 사항**

```css
li > a:first-child { color: red; }
/* a태그가 모두 선택됨 */

li:first-child > a {color: red; }
/* 첫 번째 li태그의 a태그를 선택 */
```

```html
<ul>
	<li><a href="#">Link</a></li>
	<li><a href="#">Link</a></li>
	<li><a href="#">Link</a></li>
	<li><a href="#">Link</a></li>
	<li><a href="#">Link</a></li>
</ul>
```

<br />

### ◻️ 형태 구조 선택자

- 일반 구조 선택자와 비슷하지만 태그 형태를 구분함

| 선택자 형태 | 설명  |
| --- | --- |
| :first-of-type | 형제 관계 중에서 첫 번째로 등장하는 특정 태그 선택  |
| :last-of-type | 형제 관계 중에서 마지막으로 등장하는 특정 태그 선택  |
| :nth-of-type(수열) | 형제 관계 중에서 앞에서 수열 번째로 등장하는 특정 태그 선택 |
| :nth-last-of-type(수열) | 형제 관계 중에서 뒤에서 수열 번째로 등장하는 특정 태그 선택  |

```css
h1:first-of-type { color: red; }
h2:first-of-type { color: red; }
h3:first-of-type { color: red; }
```

```html
<h1>Header 1</h1> <!-- red -->
<h2>Header 2</h2> <!-- red -->
<h3>Header 3</h3> <!-- red -->
<h3>Header 3</h3>
<h2>Header 2</h2>
<h1>Header 1</h1>
```

<br />

## 🔵 문자 선택자

- 문자 가상 요소 선택자는 태그 내부 특정 조건의 문자를 선택

<br />

### ◻️ 시작 문자 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| ::first-letter | 첫 번째 글자를 선택 |
| ::first-line | 첫 번째 줄을 선택 |

```css
p::first-letter { font-size: 3em; }
p::first-line { color: red; }
```

<br />

### ◻️ 전후 문자 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| ::after | 태그 뒤에 위치하는 공간을 선택 |
| ::before | 태그 앞에 위치하는 공간을 선택  |
- content 속성을 사용할 수 있음
- **data 속성** → 속성 앞에 문자열 data- 를 붙이면 사용자 지정 속성이 됨

<br />

### ◻️ 반응 문자 선택자

- 사용자가 문자와 반응해서 생기는 영역 선택

| 선택자 형태 | 설명 |
| --- | --- |
| ::selection | 사용자가 드래그한 글자를 선택함 |

```css
p::selection { 
	background: black;
	color: red; 
} /* 사용자가 드래그한 부분에 이 스타일이 적용됨 */
```

<br />

## 🔵 링크 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| :link | href 속성을 가지고 있는 a 태그 선택 |
| :visited | 방문했던 링크를 가지고 있는 a 태그 선택 |

```css
a { text-decoration: none; }
a:visited { color: red; }

a:link::after { content: ' - ' attr(href); } 
/* href 속성을 가지고 있는 a 태그 뒤의 공간에 "- (href 속성)"을 추가 */
```

<br />

## 🔵 부정 선택자

| 선택자 형태 | 설명 |
| --- | --- |
| :not(선택자) | 선택자를 반대로 적용함 |

```css
input:not([type=password]) {
	background: red;
} /* input 태그 중에서 type 속성값이 password가 아닌 태그의 스타일 지정 */
```

```html
<input type="password" />
<input type="text" /> <!-- red -->
<input type="password" />
<input type="text" /> <!-- red -->
```