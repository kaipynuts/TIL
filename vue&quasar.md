### Vue.js & Quasar & Javascript & CSS

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
- v-bind : 단방향
- v-model : 양방향
- v-on : 이벤트

routes에 path로 지정을 하면 화면을 세팅할 수 있다.

1. Dispatch()
Vue컴포넌트는 Dispatch(‘[action메소드명]’)를 통해 Vuex store의 Action 그룹에 속한 메서드를 실행시킬 수 있습니다.

2. Actions
API서버 통신과 같은 역할을 수행하는 메소드 그룹입니다.
주로 state에 반영하기 전 데이터를 조회하고 가공하는 역할을 수행합니다.

3. Commit()
Action메소드 혹은 Vue컴포넌트에서 Commit(‘[mutation메소드명]’)을 통해 Mutation 그룹에 속한 메서드를 실행할 수 있습니다.
컴포넌트에서는 $store.commit(), Actions 메소드에서는 첫번째 인자로 넘겨받는 context.commit()으로 트리거시킵니다.

4. Mutations
Vuex store의 상태(state)를 변경시키기 위한 메서드 집합입니다.
Vuex는 state의 조작은 오로지 Mutation의 메소드를 통해 수행하길 권장합니다.
따로 mutate 메서드는 없고, 첫 번째 인자로 받는 state.[state요소]로 수정합니다.

5. state
사용자가 정의한 상태를 저장합니다
즉각반응형이기 때문에 v-model 의 computed 메서드중 get()이 선언되어 있다면 즉각적으로 반응합니다.
Vue컴포넌트의 watch처럼 $store.watch로 변화를 감지하고 핸들링할 수 있습니다.

6. getters
여러 컴포넌트에서 동일한 computed를 통해 하나의 state를 가져와야 한다면 Vuex store에 getters를 등록하여 computed처럼 활용할 수 있습니다.
첫 번째 인자로 state를 받습니다.

7. modules
하나의 스토어만을 사용해 모든 Dispatch, Commit을 처리한다면 전역 이벤트 버스와 다를 것이 없습니다.
따라서 각 목적에 맞는 항목을 module로 분리할 수 있고 namespaced속성을 true로 설정하여 각 모듈의 이름을 포함한 Dispatch, Commit, state조회 등을 수행할 수 있습니다.
[참고자료](http://labs.brandi.co.kr/2018/12/13/kangww.html)


[Vue.js 기초](https://joshua1988.github.io/web-development/vuejs/vuejs-tutorial-for-beginner/)

[이벤트 관련 정리](https://uxgjs.tistory.com/119)

[vue3용 swiper](https://swiperjs.com/vue)

[Vuex 개념 정리](https://webruden.tistory.com/340)

백오피스 CRUD 개발 시
components
-> form
pages
-> create (include form)
-> edit (include form)
-> list

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

### Javascript
- sort() 시간 순, 역순으로 정렬하기
[참조 링크](https://dkmqflx.github.io/frontend/2021/04/21/javascript-sortbydate/)

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

- input file 타입 예쁘게 만들기
[참조 링크](https://webdir.tistory.com/435)
[vue 참고자료](https://yiunsr.tistory.com/844)


[퍼블리싱 가이드](http://www.standard-ui.com/STD_GD/convention/rule_standard.html)

- CSS 코드 컨벤션 (BEM)
[참고자료](http://getbem.com/naming/)