# :fire: mission 3.

## :grey_question: transition 과제
- transition 실습을 위한 과제 파일은 mission-03/transition.html 파일과 mission-03/transition.css 파일을 생성 후 각각 마크업과 스타일을 작성한다
- 관련 사이트는 제목으로 각각 항목은 링크로 구현한다.
- 링크 목록은 5개이며 CSS를 사용하여 화면에 1개의 목록만 보이도록 구현한다.
- 목록에 마우스를 올리면 5개의 목록이 펼쳐지도록 구현한다.
- transition 속성을 활용하여 애니메이션 효과를 적용한다.
- mission-03/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

## :camera: 결과 스크린샷
![transition_screenshot](https://github.com/shju0317/home-work/assets/31871923/ecc92e19-4363-4573-9dd8-2002a3a299ee)

## :speech_balloon: 코드리뷰
- mission-03/transition.html 파일과 mission-03/transition.css 파일을 생성 후 각각 마크업과 스타일을 작성
```html
  <section class="sites">
    <h2 class="sites-title">관련 <span>사이트</span></h2>
    <ul class="site-list">
      <li><a href="#">제로베이스</a></li>
      <li><a href="#">MDN</a></li>
      <li><a href="#">웹접근성 연구소</a></li>
      <li><a href="#">Web Standards</a></li>
      <li><a href="#">W3C</a></li>
    </ul>
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
- transition을 사용하여 리스트(.site-list)에 마우스가 올라가면(hover) 리스트가 아래로 펼쳐지면서 리스트 항목이 보이게 함
- 리스트가 접혀있을 땐 리스트 항목이 보이지 않도록 overflow: hidden을 적용
```css
.site-list{
  height: 30px;
  transition: height 300ms linear;
  overflow: hidden;
}

.site-list:hover{
  height: 160px;
  transition: height 300ms linear;
}
```
- 리스트가 펼쳐지고 접힐 때 바깥 영역(.sites)의 크기도 함께 움직일 수 있도록 섹션(.sites)의 높이를 auto로 적용
- linear-gradient를 사용하여 두 가지 배경색(#ccc, #ddd) 적용
```css
.sites{
  height: auto;
  background-image: linear-gradient(to bottom, #ccc 50%, #ddd 50%);
}
```
- transition을 적용하여 margin-top을 조정
- 리스트가 펼쳐지거나 접힌 다음에 transition이 적용될 수 있도록 delay값을 줌
```css
.site-list li{
  margin-top: 0px;
  transition: margin-top 300ms linear 300ms;
}

.site-list li:first-child:hover{
  margin-top: 5px;
  transition: margin-top 300ms linear 300ms;
}
```
