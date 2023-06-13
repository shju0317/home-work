# :fire: mission 4.

## :grey_question: grid 과제
- grid 실습을 위한 과제 파일은 mission-04/grid.html 파일과 mission-04/grid.css 파일을 생성 후 각각 마크업과 스타일을 작성한다.
- 더보기 링크 앞에 플러스 기호는 생략해도 무방하다.
- 이미지는 “W3C 리뉴얼”이라는 캡션 위에 썸네일 이미지를 사용한다.<br>
  (해당 이미지는 배경으로 지정하지 말고 <img> 요소를 사용하여 콘텐츠 이미지로 배치)
- grid를 활용하여 레이아웃을 구현한다.
- mission-04/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

## :camera: 결과 스크린샷


## :speech_balloon: 코드리뷰
- mission-04/grid.html 파일과 mission-04/grid.css 파일을 생성 후 각각 마크업과 스타일을 작성
```html
  <section class="news">
    <h2 class="news-title">새소식</h2>
    <div class="more">더보기</div>
    <figure class="news-thumbnail">
      <img src="./images/wc3_main_capture.PNG" alt="W3C 리뉴얼" />
      <figcaption>W3C 리뉴얼</figcaption>
    </figure>
    <div class="news-info">
      <p>W3C 사이트가 리뉴얼 되었습니다.</p>
      <span>2022.07.18</span>
    </div>
    <div class="news-content">
      디자인 및 다양한 view 환경을 고려하여 구성되어 있으며, 기존보다 최신 정보 및 개발자를 위한 기술 가이드도 찾기 쉽도록 구성되어 있습니다.
    </div>
  </section>
```
- 'Pretendard' 폰트 설정
```html
<link rel="stylesheet preload" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.6/dist/web/static/pretendard.css" />
```
```css
body{
  font-family: "Pretendard Variable", Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, "Helvetica Neue", "Segoe UI", "Apple SD Gothic Neo", "Noto Sans KR", "Malgun Gothic", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
}
```
(폰트설정 관련 참고: https://github.com/orioncactus/pretendard )
