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
* flex-basis와 flex-grow 값을 같이 지정할 경우 크기는 flex-basis + flex-grow 가 된다.
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

<br>

-----
## **grid**

### **기본 사용법**
2차원 레이아웃 시스템
부모(div.container) / 자식(div.item) 요소로 구성

* 용어
그리드 컨테이너 : 틀
그리드 아이템 : 틀 내의 자식들
그리드 트랙 : 행 또는 열
그리드 셀 : 한 칸
그리드 라인 : 행과 열을 구분하는 선
그리드 번호 : 각 그리드의 번호
그리드 갭 : 그리드 셀 사이의 간격
그리드 영역 : 그리드 라인으로 둘러싸인 사각형 영역


```html
<div class="container">
	<div class="item">A</div>
	<div class="item">B</div>
	<div class="item">C</div>
	<div class="item">D</div>
	<div class="item">E</div>
	<div class="item">F</div>
	<div class="item">G</div>
	<div class="item">H</div>
	<div class="item">I</div>
</div>
```

<br>

### **display: grid :**
grid 레이아웃을 사용하기 위한 속성

```css
.container {
	display: grid;
}
```

<br>

### **grid-template-rows / grid-template-columns :**
트랙의 크기를 지정하는 속성 (표 만들기)
* 비율을 지정하는 단위 	fr

```css
.container {
	grid-template-columns: 200px 200px 500px;
	/* grid-template-columns: 1fr 1fr 1fr */
	/* grid-template-columns: repeat(3, 1fr) */
	/* grid-template-columns: 200px 1fr */
	/* grid-template-columns: 100px 200px auto */

	grid-template-rows: 200px 200px 500px;
	/* grid-template-rows: 1fr 1fr 1fr */
	/* grid-template-rows: repeat(3, 1fr) */
	/* grid-template-rows: 200px 1fr */
	/* grid-template-rows: 100px 200px auto */
}
```
* 함수
- repeat : 반복 처리
	repeat(반복횟수, 반복값)
	ex. repeat(5, 1fr) : 1fr 5개, repeat(3, 1fr 4fr 2fr) 1fr, 4fr, 2fr 3개 (총 9개)
- minmax : 최소값, 최대값 지정
	minmax(최소값, 최대값)
	ex. minmax(100px, auto) : 최소 100px, 최대 자동으로 늘어나게

* 자동 지정 값 : 갯수를 미리 지정하지 않고 설정된 너비가 허용하는한 최대로 셀을 만든다
- auto-fill : 설정된 너비만큼 셀의 크기를 설정하되 남은 공간은 비워둔다
- auto-fit : 설정된 너비만큼 셀의 크기를 설정한 후 남은 공간이 있는 경우 꽉 채워서 맞춘다

<br>

### **row-gap / column-gap / gap :**
그리드 셀 사이 간격을 설정하는 속성
! IE에는 gap 대체 속성이 없다.

```css
.container {
	row-gap: 10px;
	/* row의 간격을 10px로 */
	column-gap: 20px;
	/* column의 간격을 20px로 */
}
```

```css
.container {
	gap: 10px 20px;
	/* row-gap: 10px; column-gap: 20px; */
}
```
<br>

### **grid-auto-columns / grid-auto-rows :**
그리드 형태를 자동으로 정의하는 속성 (크기를 자동으로 정의)
글자가 있는경우에 그 글자크기에 맞춰서 칸이 늘어나거나 줄어든다.
* minmax 함수와 같이 쓰는 경우, 최소크기를 자동으로 정의한다. 

```css
.container {
	grid-auto-rows: minmax(100px, auto);
}
```
<br>

### **grid-column-start / grid-column-end / grid-column :**
### **grid-row-start / grid-row-end / grid-row :**
그리드 라인 번호를 이용하여 셀의 영역을 지정하는 속성
grid-column과 grid-row는 축약형

```css
.item:nth-child(1) {
	grid-column-start: 1;
	grid-column-end: 3;
	grid-row-start: 1;
	grid-row-end: 2;
}
```
위와 동일한 효과를 내는 코드
```css
.item:nth-child(1) {
	grid-column: 1 / 3;
	grid-row: 1 / 2;
}
```
<br>

### **grid-template-area :**
영역에 이름을 붙인 후 배치하는 속성
셀 구분은 공백
빈셀은 .(마침표)나 none

```css
.container {
	grid-template-areas:
		"header header header"
		"   a    main    b   "
		"   .     .      .   "
		"footer footer footer";
}
```
위와 같이 레이아웃 정의 후 영역 이름 매칭

```css
.header { grid-area: header; }
.sidebar-a { grid-area: a; }
.main-content { grid-area: main; }
.sidebar-b { grid-area: b; }
.footer { grid-area: footer; }
/* 이름 값에 따옴표가 없는 것에 주의하세요 */
```
<br>

### **grid-auto-flow :**