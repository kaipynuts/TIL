### Vue.js & Quasar & CSS

폴더구조
- public
- src
    1. assets : 정적 파일들 (폰트, 이미지, 영상)
    2. boot : api 관련 처리 부분
        api 연결을 위한 axios
        국제화를 위한 i18n
    3. components : 화면 컴포넌트 파일
    4. css
    5. i18n : 국제화 옵션 자세한 설정 부분
    6. layouts : 레아이웃용 뷰 파일
    7. pages : 화면 파일
    8. router : 라우터 설정부분
    9. store

#### Vue
routes에 path로 지정을 하면 화면을 세팅할 수 있다.

[Vue.js 기초](https://joshua1988.github.io/web-development/vuejs/vuejs-tutorial-for-beginner/)

[이벤트 관련 정리](https://uxgjs.tistory.com/119)

[vue3용 swiper](https://swiperjs.com/vue)

##### **문제해결**
> import Vue from 'vue'

해결 : es6 문법 수정으로 인하여 변경해줌
    import ~ from -> const ~ require([file name])
[참고자료](https://stackoverflow.com/questions/65978209/vue-router-import-not-working-with-require)

#### Quasar
props = attribute

- Quasar CLI
- $q : 전역변수
- quasar 홈페이지 > style. identity 공부
- quaser.variables.scss 브랜드컬러 변경 위치

- spacing syntax (신기신기 외워두기 홈페이지에 잘 나와있음)
    p = padding
    a = all

- positioning
    fullscreen (화면 꽉채우는거 맞나?)

- carousel (회전목마))

- chip
    무슨말이지..?

- skeleton
    뼈다구. 데이터 로딩전에 프레임을 미리 만들어준다

- Notify
    = toast


#### **Layout**
- **flex**
클래스 규칙 맨 아래 정규식 참고[Quasar 링크](https://quasar.dev/layout/grid/introduction-to-flexbox)

- **q-page-sticky**
    특정 위치에 고정된 컨테이너를 만들 수 있다. (ex. 상단에 고정된 헤더)
    * q-header와 다른점 : background-color가 없다. q-header는 background-color가 있기 때문에 아래 컨테이너와 동일한 background-color를 사용해야 하는 경우 어려움이 있음.

    속성 :
    - expand : full-width
    - position : top / bottom / left / right (* 두개를 조합하여 설정 가능 ex.top-left)


### CSS
- 비율에 따라 사이즈가 조정되는 svg 이미지 구현하기
[참조 링크](https://im-developer.tistory.com/200)

- svg 소스 수정하기
[참조 링크](https://code-masterjung.tistory.com/108)
preserveAspectRatio="none" 으로 설정해야 필요없는 여백이 안나온다.
transform = translate(0,0) 으로 지정하면 좌표가 0,0으로 이동한다.

- 매번 봐도 어려운 position: absolute / relative
relative 는 원래 위치 기준으로 얼마나 움직일지 정해주는것
absolute 는 부모 컨테이너 기준으로 얼마나 움직일지 정해주는것
[참조 링크](https://www.daleseo.com/css-position/)

- 이것도 매번 봐도 어려운 상대적 사이즈 em / rem
[참조 링크](https://www.daleseo.com/css-em-rem/)

- rem 보다 더 쓸만한 반응형 사이즈 vw / vh
[참조 링크](https://nykim.work/85)