## Quasar

### Layout
#### **- [QLayout](https://quasar.dev/layout/layout)**
전체 영역 관리
하위에 QPageContainer, QHeader, QFooter and QLayoutDrawer 등을 두어 레이아웃을 구성한다. (view 속성을 이용하여 배치)

> 주의사항 :
    css - margin을 사용하면 레이아웃이 깨지므로 padding을 사용한다.

#### **- [QHeader / QFooter](https://quasar.dev/layout/header-and-footer)**
고정된 Header와 Footer를 만들때 사용

#### **- [QDrawer](https://quasar.dev/layout/drawer)**
레이아웃 내에서 영역을 구분하고 싶을 때 사용 (ex. 왼쪽 영역과 오른쪽 영역이 나눠져서 각각 드래그영역이 필요한 경우)

#### **- [QLayoutContenr](https://quasar.dev/layout/page)**
QLayout내에서 QPage를 캡슐화 할때 사용

#### **- [QPageSticky](https://quasar.dev/layout/page-sticky)**
항상 위로 올라와있어야 하는 요소를 만들때 사용 (ex. Header / Footer 등)
> 주의사항 : 
    QLayout내에 위치해야함
    부모 내의 마지막 요소여야함

#### **- [QPageScroller](https://quasar.dev/layout/page-scroller)**
특정 스크롤에 위치하면 표시되는 요소를 만들때 사용
