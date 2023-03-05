# 블록 요소

> 블록요소는 너비를 아무리 작게 설정해도 가로 영역을 모두 차지하기 때문에 다른 요소가 옆으로 올 수 없다.
> 
- 사용 가능한 최대 너비를 가진다. 높이는 내부 컨텐츠 크기 만큼 설정됨
    - `{width: 100%; height: auto;}` 와 같은 css 속성을 default로 가진다고 생각하면 됨
- `width`, `height` 로 크기를 지정할 수 있음
- `padding`, `margin`으로 상하좌우 여백을 지정할 수 있음
- 여러개의 블록 요소들이 있을때, 수직으로 쌓임 (한 줄에 하나의 블록 요소만 위치할 수 있음)
- 위와 같은 특징으로 블록요소는 보통 레이아웃을 잡을때 자주 사용한다
- 블록 요소의 종류: `div`, `h1`, `p`
    
    ![image](https://user-images.githubusercontent.com/122594223/222967381-75d3f218-fb36-4d0c-a610-3dc2f45dee6e.png)
    

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .block1 {
            background-color: tomato;
        }
        .block2 {
            background-color: yellowgreen;
        }
    </style>
</head>
<body>
    <div class="block1">이것은</div>
    <div class="block2">블록 요소입니다</div>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/122594223/222967402-a898bc3c-2e4a-47de-9655-be742bc12380.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .block1 {
            width: 300px;
            background-color: tomato;
        }
        .block2 {
            height: 200px;
            background-color: yellowgreen;
        }
    </style>
</head>
<body>
    <div class="block1">너비 300px</div>
    <div class="block2">높이 200px</div>
</body>
</html>
```

## 블록 요소에 ****padding, margin 값 지정****

> `Margin`은 Object와 화면과의 여백(외부여백)을 말하며 `Padding`은 Object내의 내부여백을 의미합니다.
> 

> `margin-left`, `padding-top` 여백 방향 지정
> 

![image](https://user-images.githubusercontent.com/122594223/222967424-e6c7b9cc-ac7c-4bcf-8f1d-c1d7b10d307e.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .block1 {
            padding: 10px;
            background-color: tomato;
        }
        .block2 {
            margin: 20px;
            background-color: yellowgreen;
        }
        .block3 {
            padding: 20px 10px;
            margin: 5px 30px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <div class="block1">padding</div>
    <div class="block2">margin</div>
    <div class="block3">padding & margin</div>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/122594223/222967451-049976aa-cb2d-4323-b32b-34385367a079.png)

---

# **인라인 요소 (Inline element)**

- 너비와 높이를 내부 컨텐츠 크기만큼 설정됨
    - {width: auto; height: auto;}와 같은 css 속성을 default로 가진다고 생각하면 됨
- `width`, `height`로 크기를 지정할 수 없음
- `padding`, `margin`으로 좌우에만 여백을 지정할 수 있음 (위, 아래는 안됨)
- 여러개의 인라인 요소가 있을때, 수평으로 쌓임
- 위와 같은 특징으로 인라인 요소는 보통 Text를 작성할 때 사용한다
- 인라인 요소의 종류: `span`, `img`
    
 ![image](https://user-images.githubusercontent.com/122594223/222967469-f94b1f45-749b-42b7-b187-b65514aaed1f.png)


```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .span1 {
            width: 100px;
            background-color: tomato;
        }
        .span2 {
            height: 500px;
            background-color: yellowgreen;
        }
        .span3 {
            width: 1000px;
            height: 1200px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <span class="span1" >이것은</span>
    <span class="span2">인라인 요소</span>
    <span class="span3">입니다.</span>
    <span class="span1" >이것은</span>
    <span class="span2">인라인 요소</span>
    <span class="span3">입니다.</span>
</body>
</html>
```

## ****인라인요소에 padding, margin 지정****

> `margin`을 지정해보면 위, 아래에는 적용이 안되고, 좌, 우에만 적용이 된다.
> 

![image](https://user-images.githubusercontent.com/122594223/222967489-c95e2e32-2f0a-4284-abe1-150ed81e244d.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .span1 {
            margin: 20px;
            background-color: tomato;
        }
    </style>
</head>
<body>
    <span class="span1">margin</span>
    <div>test</div>
</body>
</html>
```

> 이번엔 `padding`값을 지정해보면 상하좌우에 패딩 값이 들어가게되긴하는데, 위, 아래의 경우 padding으로 늘어난 부분이 공간을 차지하지 않는다. 따라서, 위, 아래는 의도하는대로 동작하지 않고, 좌, 우에만 padding 값이 제대로 적용이 된다.
> 

![image](https://user-images.githubusercontent.com/122594223/222967502-71ad1dd1-b47a-4faa-b0d0-8d8172827d4a.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .span1 {
            padding: 50px;
            background-color: tomato;
        }
        .span2 {
            background-color: yellowgreen;
        }
        .span3 {
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <span class="span1">padding</span>
    <div>인라인 요소에서 padding 값으로 위, 아래 값을 늘려도 공간을 차지하지 않음</div>
</body>
</html>
```

---

# ****인라인 블록 요소(Inline-Block Element)****

- 인라인 요소처럼 너비와 높이가 내부 컨텐츠 크기만큼 설정 된다
- 블록 요소처럼 width와 height로 너비와 높이를 설정할 수 있음
- 블록 요소처럼 padding과 margin으로 상하좌우 여백을 지정할 수 있음
- 인라인 요소처럼 여러개의 인라인블록 요소가 있을때, 수평으로 쌓인다
- 인라인블록 요소를 생성하려면, css의 {display: "inline-block";}으로 스타일을 적용해야 함

![image](https://user-images.githubusercontent.com/122594223/222967520-424c73c7-b38a-46e5-8f19-c52cec3a7495.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .inline-block {
            display: inline-block;
            width: 300px;
            height: 200px;
            background-color: tomato;
        }
    </style>
</head>
<body>
    <div class="inline-block">인라인 블록에 너비, 높이 지정</div>
</body>
</html>
```

## ****인라인 블록 요소에 margin과 padding 적용****

![image](https://user-images.githubusercontent.com/122594223/222967531-f5d63c31-0064-4980-a3da-df21fdecd844.png)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <title>block, inline, inline-block</title>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
        .inline-block {
            display: inline-block;
            margin: 30px;
            padding: 50px 60px;
            background-color: tomato;
        }
    </style>
</head>
<body>
    <div class="inline-block">인라인 블록에 margin, padding 지정</div>
</body>
</html>
```
