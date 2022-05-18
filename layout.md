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
레이아웃 배치 방향 설정
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
레이아웃이 넘어가는 경우 줄넘김 설청
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
flex-direction + flex-wrap 

-----