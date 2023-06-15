# :fire: mission 5.

## :grey_question: sprite 과제
- sprite 실습을 위한 과제 파일은 mission-05/sprite.html 파일과 mission-05/sprite.css 파일을 생성 후 각각 마크업과 스타일을 작성한다.
- 더보기 링크 앞에 플러스 기호는 생략해도 무방하다.
- rank.png(webcafe-RWD/assets 폴더에 있음) 이미지를 활용하여 스프라이트 기법으로 스타일링 한다.
- 각 인기 사이트의 순위를 나타내는 영역은 기존 <ol> 요소에서 제공하는 기본 숫자를 보이지 않도록 한 후 CSS로 구현한다.
- mission-05/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

## :camera: 결과 스크린샷
![mission5](https://github.com/shju0317/home-work/assets/31871923/8136e9fb-db3a-41df-9b68-8e8ab0492fd3)



## :speech_balloon: 코드리뷰
- mission-05/sprite.html 파일과 mission-05/sprite.css 파일을 생성 후 각각 마크업과 스타일을 작성
  ```html
  <section class="favorite gradient-effect">
    <h2 class="favorite-title">
      인기 <span class="accent-primary-color">사이트</span>
    </h2>
    <ol class="favorite__list">
      <li class="favorite__item">
        <a href="#">WC3</a>
          <div class="sprite spriteUp"><span class="a11yHidden">랭킹 상승</span></div>
      </li>
      <li class="favorite__item">
        <a href="#">Web Standards</a>
          <div class="sprite spriteDown"><span class="a11yHidden">랭킹 하락</span></div>
      </li>
      <li class="favorite__item">
        <a href="#">MDN</a>
          <div class=" sprite spriteFreeze"><span class="a11yHidden">랭킹 동결</span></div>
      </li>
      <li class="favorite__item">
        <a href="#">CSS ZenGarden</a>
          <div class=" sprite spriteUp"><span class="a11yHidden">랭킹 상승</span></div>
      </li>
    </ol>
    <a href="#" title="인기사이트" class="favorite__more">
      <span class="far fa-plus-square accentMore"
        aria-hidden="true"></span>더보기
    </a>
  </section>
  ```
- 'Pretendard' 폰트 설정
  ```html
    <link rel="preload" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.6/dist/web/static/pretendard-dynamic-subset.css" />css" />
  ```
  ```css
  body{
    font-family: "Pretendard Variable", Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, "Helvetica Neue", "Segoe UI", "Apple SD Gothic Neo", "Noto Sans KR", "Malgun Gothic", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
  }
  ```
(폰트설정 관련 참고: https://github.com/orioncactus/pretendard )

- linear-gradient를 사용하여 section(.favorite)의 배경색 지정
  ```css
  .gradient-effect {
  width: 200px;
  border: 1px solid #aaa;
  border-radius: 5px;
  background: linear-gradient(#ccc, #eee);
  }
  ```
- 가상요소(::before)를 사용하여 순위(1~4위)를 나타냄. 1부터 4까지의 숫자는 counter를 사용하여 설정
  ```css
  .favorite__item{
    display: flex;
    align-items: center;
    counter-increment: number;
    padding-top: 8px;
    line-height: 25px;
    font-size: 11px;
  }
  
  .favorite__item::before{
    display: inline-block;
    content: counter(number);
    background-color: #A3A3A3;
    width: 16px;
    height: 16px;
    line-height: 150%;
    text-align: center;
    padding: 4px;
    margin-right: 4px;
    font-size: 11px;
    color: #fff;
    border-radius: 5px;
  }
  ```
- 링크의 선택 영역을 넓히기 위해 flex-grow를 사용하여 링크의 너비를 넓힘
  ```css
  .favorite__item a{
  display: inline-block;
  flex-grow: 1;
  }
  ```
- sprite 기법으로 랭킹 변동을 나타내는 화살표 이미지 삽입
  ```css
  .sprite {
    display: inline-block;
    background: url(./images/rank.png) no-repeat;
    background-position: right;
    height: 10px;
    width: 9px;
  }
  
  .spriteUp{
    background-position: right 0;
  }
  
  .spriteFreeze{
    background-position: right -22px;
  }
  
  .spriteDown{
    background-position: right -45px;
  }
  ```
- 가운데 정렬하기 위해서 align-items:center 사용
  ```css
  .favorite__item{
    display: flex;
    align-items: center;
    counter-increment: number;
    padding-top: 8px;
    line-height: 25px;
    font-size: 11px;
  }
  ```
  - '더보기'의 위치가 상단 우측에 위치할 수 있도록 position:absolute 사용
  ```css
    .favorite{
      position: relative;
      padding: 12px;
    }
  
  .favorite__more{
    position: absolute;
    top: 12px;
    right: 12px;
    font-size: 11px;
  }
  ```
- fontawesome을 사용하여 '더보기' 앞의 '플러스(+)' 이미지 표현
  ```html
   <link rel="stylesheet"
    href="https://use.fontawesome.com/releases/v5.15.4/css/all.css"
    integrity="sha384-DyZ88mC6Up2uqS4h/KRgHuoeGwBcD4Ng9SiP4dIRy0EXTlnuz47vAwmeGwVChigm"
    crossorigin="anonymous" />
  ```
  ```html
    <a href="#" title="인기사이트" class="favorite__more">
      <span class="far fa-plus-square accentMore" aria-hidden="true"></span>더보기
    </a>
  ```
  ```css
  .accentMore{
    color: #447231;
  }
  ```
