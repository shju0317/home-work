# :fire: mission 2.

## :grey_question: position 과제
- position 실습을 위한 과제 파일은 mission-02/login.html 파일과 mission-02/login.css 파일을 생성 후 각각 마크업과 스타일을 작성한다.
- 마크업 순서는 1. 로그인(제목), 2. 아이디 레이블과 입력서식, 3. 비밀번호 레이블과 입력서식, 4. 로그인 버튼, 5. 회원가입 및 아이디/비밀번호 찾기 링크 순으로 구현한다.
- 이미지 assets 없이 모든 디자인을 CSS로 구현한다. (회원가입 앞에 특수문자는 구현하지 않아도 됨)
- 일부 요소의 배치를 position 속성을 활용하여 구현한다.
- 회원가입, 아이디/비밀번호 찾기 영역은 float을 활용하여 구현한다.
- mission-02/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

## :camera: 결과 스크린샷
![mission02](https://github.com/shju0317/home-work/assets/31871923/97dd3941-07e3-4db6-b62b-3de96842e261)

## :speech_balloon: 코드리뷰
- 주어진 조건에 맞게 1. 로그인(제목), 2. 아이디 레이블과 입력서식, 3. 비밀번호 레이블과 입력서식, 4. 로그인 버튼, 5. 회원가입 및 아이디/비밀번호 찾기 링크 순으로 마크업
- 'Pretendard' 폰트 설정
```html
<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.6/dist/web/static/pretendard.css" />
```
```css
body{
  font-family: "Pretendard Variable", Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, "Helvetica Neue", "Segoe UI", "Apple SD Gothic Neo", "Noto Sans KR", "Malgun Gothic", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
}
```
(폰트설정 관련 참고: https://github.com/orioncactus/pretendard )
- 아이디, 비밀번호 입력란(input 요소)을 우측에 위치시키기 위해 position: absolute 활용
```css
.userEmailInput, .userPasswordInput{
  box-sizing: border-box;
  position: absolute;
  right: 0;
  padding: 0px 0px 0px 8px;
}
```
- '로그인'버튼을 우측에 위치시키기 위해 position: absolute 활용
```css
.button{
  position: absolute;
  top: 8px;
  right: 8px;
  }
```
- '회원가입'은 좌측으로, '아이디 비밀번호 찾기'는 우측으로 정렬하기 위해 각각 float:left와 float:right 활용
- 회색선을 표현하기 위해 memberOnly 클래스에 가상요소 추가
