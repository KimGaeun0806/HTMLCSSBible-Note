# CSS3 스타일 속성

## 💻 목차
- [CSS3 단위](#-css3-단위)
- [가시 속성](#-가시-속성)
- [박스 속성](#-박스-속성)
- [테두리 속성](#-테두리-속성)
- [배경 속성](#-배경-속성)
- [폰트 속성](#-폰트-속성)
- [위치 속성]
- [float 속성]
- [clear:both를 사용한 레이아웃]
- [그림자 속성]
- [그레이디언트]
- [벤더 프리픽스]

<br/>

## 🔵 CSS3 단위

### ◻️ 크기 단위

| 단위 | 설명 |
| --- | --- |
| % | 백분율 단위 (기본 설정된 크기인 100% 에서 상대적으로 크기 지정) |
| em | 배수 단위 (1배 = 1em = 100%, 1.5배 = 1.5em = 150%) |
| px | 픽셀 (절대적으로 크기 지정) |
- **크기 단위의 복합 사용** → 크기 단위를 섞어서 사용할  때

```css
/* 전체 폰트 크기에 절대 크기 지정, 각각의 태그에 상대 크기 지정 */
* { font-size: 12px; }
h1 { font-size: 3.0em; }
h2 { font-size: 1.5em }
```

- **제로** → 크기 단위 0을 입력하는 경우 단위를 입력하지 않아도 됨

<br />

### ◻️ 색상 단위

| 단위 형태 | 설명  |
| --- | --- |
| #000000 | HEX 코드 단위  |
| rgb (red, green, blue) | RGB 색상 단위  |
| rgba (red, green, blue, alpha) | RGBA 색상 단위 |
| hsl (hue, saturation, lightness) | HSL 색상 단위 |
| hsla (hue, saturation, lightness, alpha) | HSLA 색상 단위  |
- **알파 값** → A는 투명도를 의미하는 알파 값. 0.0 (완전히 투명한 상태)부터 1.0 (불투명한 상태) 사이의 숫자 입력.

```css
/* RGB 색상 -> 각각의 숫자는 0부터 255까지 입력 가능 */
h1 { background-color: rgb(255, 255, 255); } 

/* HEX 코드 -> 16진수(00부터 FF)로 RGB 색상 조합을 순서대로 입력(red, green, blue) */
h1 { background-color: #0094FF; }

/* HSL 색상 -> 색상, 채도, 명도 이용 */
h1 { background-color: hsl(33, 100%, 50%); }
```

<br />

### ◻️ URL 단위

- 이미지 파일이나 폰트 파일을 불러올 때 사용

```css
body {
	background-image: url('Yellow.jpg') /* 현재 폴더의 Yellow.jpg */
}
body {
	background-image: url('Sources/Yellow.jpg') /* 현재 폴더 내부에 있는 Sources 폴더의 Yellow.jpg */
}
body {
	background-image: url('/Yellow.jpg') /* 루트 폴더의 Yellow.jpg */
}
```

<br />

## 🔵 가시 속성

- 태그가 화면에 보이는 방식을 지정하는 속성

### ◻️ display 속성

| 키워드 이름 | 설명 |
| --- | --- |
| none | 태그를 화면에서 보이지 않게 만듦 (화면에서 사라짐) |
| block | 태그를 block 형식으로 지정함 |
| inline | 태그를 inline 형식으로 지정함 |
| inline-block | 태그를 inline-block 형식으로 지정함 |

```css
#box {
	display: none;
}

#box {
	display: block;
}

/* inline 형식과 inline-block 형식은 width,height 속성과 margin 속성을 사용할 때 차이가 있음 */
#box {
	display: inline;
	background-color: red;
	width: 300px; /* width 속성이 적용되지 않음 */
	height: 50px; /* height 속성이 적용되지 않음 */
	margin: 10px; /* div 태그의 좌우로만 지정됨 */
}

#box {
	display: inline-block;
	background-color: red;
	width: 300px; /* width 속성이 적용됨 */
	height: 50px; /* height 속성이 적용됨 */
	margin: 10px; /* 상하좌우로 적용됨 */
}
```

<br />

### ◻️ visibility 속성

| 키워드 이름 | 설명 |
| --- | --- |
| visible | 태그를 보이게 만듦 |
| hidden | 태그를 보이지 않게 만듦 (자리는 차지하지만 보이지 않음) |
| collapse | table 태그를 보이지 않게 만듦 |
- **collapse 키워드** → 인터넷 익스플로러와 파이어폭스에서만 작동하며 table 태그에 사용함.
collapse 키워드를 적용하면  table 태그가 차지하는 영역이 없어지지만, hidden 키워드를 적용하면 차지하는 영역은 그대로이고 보이지 않기만 함.

<br />

### ◻️ opacity 속성

- 태그의 투명도를 조절하며 0.0 (투명한 상태)부터 1.0 (불투명한 상태) 사이의 숫자 입력 가능

```css
#box {
	background-color: black;
	color: white;
	opacity: 0.2; /* 약간 투명한 상태로 보임 */
}
```

<br />

## 🔵 박스 속성

### ◻️ width 속성과 height 속성

- 글자를 감싸는 영역의 크기를 지정하는 스타일 속성

```css
div {
	width: 100px; /* div 태그의 너비 100픽셀로 지정 */
	height: 100px; /* div 태그의 높이 100픽셀로 지정 */
}
```

<br />

### ◻️ margin 속성과 padding 속성

- margin 속성은 마진의 너비를 지정, padding 속성은 패딩의 너비를 지정

```css
div {
	width: 100px;
	height: 100px;
	background-color: skyblue;
	border: 20px solid gray;
	margin: 10px;
	padding: 30px;
} 
```

<img src="/sources/마진패딩.png" width="300px">

- 태그 전체 너비 = width + 2 x (margin + border + padding)
태그 전체 높이 = height + 2 x (margin + border + padding)
- margin 속성과 padding 속성은 네 방향을 별도로 지정 가능

```css
/* 위쪽, 아래쪽, 왼쪽, 오른쪽 각각 지정 */
div {
	margin-top: 10px;
	margin-bottom: 10px;
	margin-left: 10px;
	margin-top: 10px;
}

/* margin: [margin-top] [margin-right] [margin-bottom] [margin-left] */
div {
	margin: 10px 10px 10px 10px;
}

/* margin: 위아래 왼쪽오른쪽 */
div {
	margin: 0 30px;
}
```

<br />

### ◻️ box-sizing 속성

- width 속성과 height 속성이 차지하는 범위 지정

```css
div {
	margin: 10px;
	padding: 10px;
	width: 100px;
	height: 100px;
	border: 10px solid black;
}

div:first-child {
	background: red;
	box-sizing: content-box; 
}
/* 기본으로 적용됨
박스 너비 = width + 2 x (margin + border + padding)
박스 높이 = height + 2 x (margin + border + padding) */

div:last-child {
	background: orange;
	box-sizing: border-box;
}
/* width 속성과 height 속성이 테두리를 포함한 영역의 크기 지정
박스 너비 = width + 2 x margin
박스 높이 = height + 2 x margin */
```

<br />

## 🔵 테두리 속성

### ◻️ border-width 속성과 border-style 속성

- border-width 속성은 테두리의 너비를 지정, border-style 속성은 테두리의 형태 지정

```css
.box {
	border-width: thick;
	border-style: dashed;
	border-color: black;
}

/* border-width, border-style, border-color 속성을 띄어쓰기로 구분해서 한 번에 입력 가능 */
.box {
	border: thick dashed black; 
}
```

- **부분 스타일 지정** → border 속성은 left, top, right, bottom 부분 값 적용 가능

```css
.box {
	border-top: thick dashed black;
	border-bottom: thick dashed red;
	border-left: thick dashed green;
	border-right: thick dashed blue;
}
```

<br />

### ◻️ border-radius 속성

- 테두리가 둥근 사각형 또는 원을 만들 수 있음

```css
.box {
	border: thick dashed black;
	border-radius: 20px;
}

.box {
	border: thick dashed black;
	border-radius: 50px 40px 20px 10px; /* 네 모서리에 서로 다른 크기 적용 가능 */
}
```

<br />

## 🔵 배경 속성

- 특정 태그의 배경 이미지 또는 색상 지정

### ◻️ background-image 속성

- 배경에 넣을 그림을 지정하는 속성으로,URL 단위나 그레이디언트 등을 입력

```css
body {
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	/* 여러 개의 배경을 적용하면 왼쪽에 위치한 이미지가 앞으로 나옴. */
}
```

<br />

### ◻️ background-size 속성

- 1개 또는 2개의 크기 단위를 적용하며 각각 너비와 높이 의미

```css
body {
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100% 250px; /* 너비는 꽉 참, 높이는 250픽셀 */
}
```

- 띄어쓰기가 아닌 쉼표로 구분하면, 각각의 배경에 서로 다른 크기를 적용하는 것

```css
/* BackgroundFront.png 파일은 너비가 100%, BackgroundBack.png 파일은 너비가 200% */
body {
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100%, 200%;
}
```

- **background-size 속성의 키워드** → background-size 속성에 contain 키워드를 적용하면 너비를 100%로 적용한 것과 같은 효과. cover 키워드를 적용하면 높이를 100%로 적용한 것과 같은 효과.

<br />

### ◻️ background-repeat 속성

- repeat 키워드를 적용하면 이미지가 패턴을 이루고, repeat-x키워드를 적용하면 x축 방향으로 이미지가 반복되며 repeat-y 키워드를 적용하면 y축 방향으로 이미지 반복
- background-repeat 속성의 기본 키워드는 repeat임

```css
body {
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100%;
	background-repeat: no-repeat; /* 반복 없이 배경 이미지 적용 */
}
```

<br />

### ◻️ background-attachment 속성

- 배경 이미지를 어떠한 방식으로 화면에 붙일 것인지 지정하는 스타일 속성
- background-attachment 속성의 기본 키워드는 scroll 키워드 → 화면 스크롤에 따라 배경 이미지가 함께 이동함

```css
body {
	background-color: #E7E7E8;
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100%;
	background-repeat: no-repeat;
	background-attachment: fixed; /* 스크롤을 내려도 배경 이미지가 고정됨 */
}
```

<br />

### ◻️ background-position 속성

- background-position: 키워드;
background-position: x축위치;
background-position: x축위치 y축위치; 
와 같은 형태로 값을 적용

```css
body {
	background-color: #E7E7E8;
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100%;
	background-repeat: no-repeat;
	background-attachment: fixed; 
	background-position: bottom; /* 배경 이미지가 아래에 붙음 */
}

body {
	background-color: #E7E7E8;
	background-image: url('BackgroundFront.png'), url('BackgroundBack.png');
	background-size: 100%;
	background-repeat: no-repeat;
	background-attachment: fixed; 
	background-position: 0px 50%; /* x축 위치 0픽셀, y축 위치 50% */
}
```

<br />

## 🔵 폰트 속성

### ◻️ font-size 속성

- 글자의 크기 지정

```css
.a { font-size: 32px; }
.b { font-size: 2em; }
.c { font-size: large; }
.d { font-size: small; }
```

<br />

### ◻️ font-family 속성

- 폰트 지정
- 사용자에게는 폰트가 설치되지 않았을 수도 있으므로 font-family 속성 여러 개 사용함
- font-family 속성의 가장 마지막 폰트에는 Serif 폰트(명조체), Sans-serif 폰트(고딕체), Mono space 폰트(고정폭 글꼴) 적용 (generic-family)

```css
.font_arial { font-family: '없는 폰트', Arial; }
.font_roman { font-family: 'Times New Roman', Arial; }
/* 한 단어로 이루어진 폰트는 따옴표를 사용하지 않지만, 두 단어 이상으로 이루어진 폰트는 따옴표 사용 */
```

<br />

### ◻️ font-style 속성과 font-weight  속성

- 폰트의 기울기와 두께 조정

```css
.font_italic { font-style: italic; } /* 기울어짐 */
.font_bold { font-weight: bold; } /* 굵어짐 */

/* 일반 폰트 두께는 400, 두꺼운 폰트 두께는 700 */
```

<br />

### ◻️ line-height 속성

- 글자의 높이 지정
- 글자를 수직 중앙 정렬할 때 자주 사용

```css
.font_center { text-align: center; } /* 글자 수평 중앙 정렬 */

.button {
	width: 150px;
	height: 70px;
	background-color: #FFFFFF;
	border: 10px solid #000000;
}

.button > a {
	display: block;
	line-height: 70px; /* 글자를 감싸는 박스의 높이와 같은 크기의 line-height 속성 사용 -> 글자 수직 중앙 정렬*/
}
```

```html
<div class="button">
	<a href="#" class="font_center">Click</a>
</div>
```

<br />

### ◻️ text-align 속성

- 글자 정렬

```css
.font_center { text_align: center; } /* 중앙 정렬 */
.font_right { text_align: right; } /* 오른쪽 정렬 */
```

- **text-align 속성과 영역** → span 태그는 text-align 속성을 적용할 수 없음. span 태그는 inline 형식을 가지므로 너비가 존재하지 않기에 중앙의 개념이 없기 때문.

<br />

### ◻️ text-decoration 속성

```css
a { text-decoration: none; } /* href 속성을 사용했을 때 생기는 글자의 밑줄 제거 */
```

```html
<h1>
	<a href="#">Orange Color Orange</a>
</h1>
```