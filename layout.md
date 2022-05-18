# CSS

## **flex**

### **기본 사용법**
부모(div.container) / 자식(div.item) 요소로 구성

```html
<div class="container">
	<div class="item">helloflex</div>
	<div class="item">abc</div>
	<div class="item">helloflex</div>
</div>
```

<br>

### **[부모 속성]**
### **display: flex :**
flex 레이아웃을 사용하기 위한 속성

```css
.container {
	display: flex;
}
```
<br>

### **flex-direction :**
레이아웃 배치 방향 속성
- row : Horizontal 가로방향
- column : Vertical 세로방향
- row-reverse : Horizontal reverse 역가로방향
- column-reverse : Vertical reverse 역세로방향

```css
.container {
	flex-direction: row;
	/* flex-direction: column; */
	/* flex-direction: row-reverse; */
	/* flex-direction: column-reverse; */
}
```
<br>

### **flex-wrap :**
레이아웃이 넘어가는 경우 줄넘김 속성
- nowrap : 아무처리하지않음
- wrap : 다음 줄로 넘김
- wrap-reverse : 윗 줄로 넘김

```css
.container {
	flex-wrap: nowrap;
	/* flex-wrap: wrap; */
	/* flex-wrap: wrap-reverse; */
}
```
<br>

### **flex-flow :**
flex-direction + flex-wrap을 동시에 사용할 수 있는 속성
flex-direction 한칸띄고 flex-wrap 입력

```css
.container {
	flex-flow: row wrap;
	/* 아래의 두 줄을 줄여 쓴 것 */
	/* flex-direction: row; */
	/* flex-wrap: wrap; */
}
```
<br>

### **justify-content :**
메인축 방향으로 정렬하는 속성
- flex-start : 시작점으로 정렬
- flex-end : 끝점으로 정렬
- center : 가운데로 정렬
- space-between : 아이템 사이에 균일한 간격을 만들어 정렬
- space-around : 아이템 둘레에 균일한 간격을 만들어 정렬
- space-evenly : 아이템 사이와 양끝에 균일한 간격을 만들어 정렬

```css
.container {
	justify-content: flex-start;
	/* justify-content: flex-end; */
	/* justify-content: center; */
	/* justify-content: space-between; */
	/* justify-content: space-around; */
	/* justify-content: space-evenly; */
}
```
<br>

### **align-items :**
수직축 방향으로 정렬하는 속성
- stretch : 수직축 방향으로 꽉 채움
- flex-start : 시작점으로 정렬
- flex-end : 끝점으로 정렬
- center : 가운데 정렬
- baseline : 텍스트 베이스라인 기준으로 정렬

```css
.container {
	align-items: stretch;
	/* align-items: flex-start; */
	/* align-items: flex-end; */
	/* align-items: center; */
	/* align-items: baseline; */
}
```
<br>

### **align-content :**
flex-wrap:wrap; 이 설정된 상태에서 아이탬들의 행이 2줄 이상 되었을 때의 수직축 방향 정렬을 결정하는 속성
- stretch : 2줄을 수직축 방향으로 꽉 채움
- flex-start : 2줄을 시작점으로 정렬
- flex-end : 2줄을 끝점으로 정렬
- center : 2줄을 가운데로 정렬
- space-between : 2줄 사이에 균일한 간격을 두어 정렬
- space-around : 2줄 둘레로 균일한 간격을 두어 정렬
- space-evenly : 2줄 사이와 양끝에 균일한 간격을 두어 정렬

```css
.container {
	flex-wrap: wrap;
	align-content: stretch;
	/* align-content: flex-start; */
	/* align-content: flex-end; */
	/* align-content: center; */
	/* align-content: space-between; */
	/* align-content: space-around; */
	/* align-content: space-evenly; */
}
```

<br><br>

### **[자식 속성]**
### **flex-basis :**
아이템의 기본 크기 설정 (flex-direction이 row일 때는 너비, column일 때는 높이)
아이템이 기본 크기보다 작을 경우 기본 크기에 맞춰주는 속성
* width 속성과 같이 사용할 경우 기본 크기보다 클 경우에도 기본 크기에 맞춰진다.
```css
.item {
	flex-basis: auto; /* 기본값 */
	/* flex-basis: 0; */
	/* flex-basis: 50%; */
	/* flex-basis: 300px; */
	/* flex-basis: 10rem; */
	/* flex-basis: content; */
}
```

width 속성과 같이 사용하여 기본 크기보다 큰 아이템의 글자가 삐져나온 경우 아래의 속성을 이용하여 아랫줄로 글자를 넘겨준다
```css
word-wrap: break-word;
```

<br>

### **flex-grow :**
flex-basis를 제외한 여백 부분을 설정한 비율만큼 채우는 속성

```css
.item {
	flex-grow: 1;
	/* flex-grow: 0; */ /* 기본값 */
}
```

<br>

### **flex-shrink :**
아이템이 flex-basis보다 작아질 수 있는지 설정하는 속성 (1>= Y, 0: N)
0으로 설정할경우 flex-basis보다 작아지지 않고 유지시킬 수 있다.

```css
.item {
	flex-basis: 150px;
	flex-shrink: 1; /* 기본값 */
}
```

<br>

### **flex :**
flex-grow + flex-shrink + flex-basis를 동시에 사용할 수 있는 속성
flex-grow 한칸띄고 flex-shrink 한칸띄고 flex-basis 입력

```css
.item {
	flex: 1;
	/* flex-grow: 1; flex-shrink: 1; flex-basis: 0%; */
	flex: 1 1 auto;
	/* flex-grow: 1; flex-shrink: 1; flex-basis: auto; */
	flex: 1 500px;
	/* flex-grow: 1; flex-shrink: 1; flex-basis: 500px; */
}
```

<br>

### **align-self :**
수직축 방향으로 아이템 정렬
- auto : 부모의 align-items를 상속
- stretch : 수직축 방향으로 꽉 채움
- flex-start : 시작점으로 정렬
- flex-end : 끝점으로 정렬
- center : 가운데 정렬
- baseline : 텍스트 베이스라인 기준으로 정렬

```css
.item {
	align-self: auto;
	/* align-self: stretch; */
	/* align-self: flex-start; */
	/* align-self: flex-end; */
	/* align-self: center; */
	/* align-self: baseline; */
}
```

<br>

### **order :**
시각적 나열 순서를 설정하는 속성
```css
.item:nth-child(1) { order: 3; }
.item:nth-child(2) { order: 1; }
.item:nth-child(3) { order: 2; }
```

<br>

### **z-index :**
z축 정렬
z-index를 설정 안하면 0이므로, 1만 설정해도 나머지 아이템을 보다 위로 올라옴
```css
.item:nth-child(2) {
	z-index: 1;
	transform: scale(2);
}
```
-----