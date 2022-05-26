### Vue.js & Quasar

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