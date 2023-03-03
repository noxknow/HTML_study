# HTML 작성법

```html
< 태그 속성 = "속성값" > 내용 < /태그 >
<p align = "center">내용</p>
```

# Container 태그

> 다른 태그를 집어 넣을 수 있는 태그를 `container 태그` 라고 한다.
> 

> 콘텐츠나 레이아웃에 아무런 영향도 주지 않고, 여러 요소들을 하나로 묶어 관리하기 편하게하는 태그를 컨테이너 태그라고 한다.
> 

## 시멘틱 태그

> 시멘틱 태그란 브라우저, 개발자와 사용자에게 태그에 종속되어있는 내용을 직설적으로 알려주는 태그이다. ( 의미가 있는 태그 )
> 
- **`header`** : 전체 사이트의 헤더, article에 관련된 헤더이다.
- **`nav**` : 로그인, 목차 네비게이터 등으로 사용된다.
- **`section**` : 뉴스헤드라인, 컨텐츠 분류, 본문바디에서 구간을 나눌 때, 본문안에서 본문끼리의 그룹을 지을 때 사용
- **`article**` : 페이지의 주요 내용정보를 담을 때 사용
- **`aside**` : 분몬 내용을 서포트 할 때 사용, aside가 어디에 포함되냐에 따라 사용 용도가 다르다.
- **`article 내 aside` :** article에 종속되어있는 내용을 서포트해주는 정보를 담을 때 사용, 사용검색엔진이 스캐닝을 할때 article에 관련된 aside인지 알수있다.
- **`외부 aside` :** 사이트 전체의 해당 되는 내용을 서포트 할 수 잇는 정보를 담은 aside, 간단한 네비 넣을 수 있음
- **`footer`** : 회사소개, 저작권 약관등의 정보를 넣음

![image](https://user-images.githubusercontent.com/122594223/222658010-dd78cd8d-30a0-4be2-8d89-f1259cb494b5.png)

---

## 논 시맨틱 태그

> 아무런 의미가 부여되지 않는 태그이다. 스타일(css)을 주거나, 서버에서 데이터를 받아서 그룹형 컨테이너(혹은 모듈)로 manipulate를 해야할 때 컨테이너형 태그를 사용한다. 논 시멘틱 태그는 `div` 와 `span` 이 있다.
> 

### 제목 태그 **: (h1) - (h6)**

> 이렇게 단계 별로 글씨 크기와 굵기에 차이가 생긴다. 그러나 글씨 크기를 위해 제목 태그를 사용하면 안된다. 나중에 `css` 로 다 조절이 가능하다.
> 

```html
<h1>Level 1</h1>
<h2>Level 2</h2>
<h3>Level 3</h3>
<h4>Level 4</h4>
<h5>Level 5</h5>
<h6>Level 6</h6>
```
![image](https://user-images.githubusercontent.com/122594223/222658074-b7d22a55-20d2-4801-9c20-f91ba0b53e96.png)

---

### **문단 태그 : (p)**

> `<p></p>` 태그는 paragraph, 즉 문단의 약자로, 하나의 문단을 만들 때 쓰인다.
> 

```html
<html>
	<body>
		<p>first paragraph</p>
		<p>second paragraph</p>
		<p>
			new line<br>
			third paragraph
		</p>
	</body>
</html>
```

```html
first paragraph

second paragraph

new line
third paragraph
```

---

### (div)(/div)

- 박스 형태로 영역이 설정되고 그 안에 정렬된다.
- width, height 크기 지정이 가능함.
- 자동으로 줄바꿈이 된다.
- margin 속성이 4방향 모두 적용이 되며 위 아래 겹쳐지는 여백은 상쇄된다. 즉 여백의 크기가 더해서 2배가 되는 것이 아니라 겹쳐지는 것.

```html
<html>
	<body>
		<div style="background-color:cyan">구역1</div>
		<div style="width:100px; height:100px; background-color:#CF0">구역2</div>
	</body>
</html>
```
![image](https://user-images.githubusercontent.com/122594223/222658183-d9eed58f-5a85-492c-839a-90aec94d7066.png)

---

### (span)(/span)

- `span` 은 줄 단위로 영역이 설정된다.
- inline 속성을 가지기 때문에 width 와 height 를 속성값으로 정해 줄 수 없다.
- 줄바꿈이 되지 않고 옆으로 나열된다.
- margin 속성이 양 옆으로만 적용되며 겹쳐지지 않는다. 가시적으로 더 넓어 보임.

```html
<html>
<body>
	<span style="background-color:red">span1</span>
	<span style="background-color:blue">span2</span>
	<span style="background-color:green">span3</span>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/122594223/222658234-38d630d7-e94e-409e-b863-7ddad9eb85dd.png)

---

# Meta 태그

> 메타태그 속성에는 `http-equiv, name, content` 3가지 속성이 있다.
> 
- `<meta>` 요소는 `<base>, <link>, <script>, <style>, <title>` 요소와 같은 다른 메타데이터 관련 요소들이 나타낼 수 없는 다양한 종류의 메타데이터를 제공할 때 사용되며, 이렇게 제공된 정보는 브라우저나 검색 엔진, 다른 웹 서비스에서 사용하게 된다.
- 이러한 `<meta>` 요소는 언제나 `<head>` 요소 내부에 위치해야 한다.
- 만약 `name` 속성이나 `http-equiv` 속성이 명시되었다면 반드시 `content` 속성도 함께 명시되어야 하며, 반대로 두 속성이 명시되지 않았다면 content 속성 또한 명시될 수 없다.
- HTML5에서는 `<meta>` 요소를 통해 웹 페이지에서 사용자가 볼 수 있는 영역인 뷰포트(viewport)를 제어할 수 있도록 `name` 속성에 `viewport` 속성값을 제공하고 있다.

> 검색 엔진을 위한 키워드(keyword)를 정의하는 예제
> 

```html
<meta name="keyword" content="HTML, meta, tag, element, reference">
```

> 웹 페이지에 대한 설명(description)을 정의하는 예제
> 

```html
<meta name="description" content="HTML meta tag page">
```

> 문서의 저자(author)를 정의하는 예제
> 

```html
<meta name="author" content="TCPSchool">
```

> 5초 뒤에 다른 페이지로 리다이렉트(redirect)시키는 예제
> 

```html
<meta http-equiv="refresh" content="5;url=http://www.tcpschool.com">
```

> 모든 장치에서 웹 사이트가 잘 보이도록 뷰포트(viewport)를 설정하는 예제 (반응형 웹)
> 

```html
<meta name = "viewport" content = "width = device-width, initial-scale=1, shrink-to-fit=no">
```

---

# & 특수문자

> `&nbsp;` 는 공백을 의미한다. 나머지는 순서대로
> 

![image](https://user-images.githubusercontent.com/122594223/222658314-04ea3b0e-2a81-49ca-a333-979fd8e22fba.png)

```html
&copy; &amp; &lt; &gt; &nbsp;
```

---

## **style 속성으로 자주 오는 속성값 예**

- 배경색상 지정 : `background-color`
- 텍스트 색상 : `color`
- 글꼴 모양 지정 : `font-family`
- 글꼴 크기 : `font-size`
- 텍스트 정렬 : `text-align`

---
