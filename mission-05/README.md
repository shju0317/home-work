# :fire: mission 5.

## :grey_question: sprite 과제
- sprite 실습을 위한 과제 파일은 mission-05/sprite.html 파일과 mission-05/sprite.css 파일을 생성 후 각각 마크업과 스타일을 작성한다.
- 더보기 링크 앞에 플러스 기호는 생략해도 무방하다.
- rank.png(webcafe-RWD/assets 폴더에 있음) 이미지를 활용하여 스프라이트 기법으로 스타일링 한다.
- 각 인기 사이트의 순위를 나타내는 영역은 기존 <ol> 요소에서 제공하는 기본 숫자를 보이지 않도록 한 후 CSS로 구현한다.
- mission-05/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

## :camera: 결과 스크린샷



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

