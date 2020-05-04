# 반찬서비스

## 반찬서비스 - 요구사항

[요구사항](https://lucas.codesquad.kr/course/%EB%A7%88%EC%8A%A4%ED%84%B0%EC%A6%88-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/%EC%98%A8%EB%9D%BC%EC%9D%B8%EB%B0%98%EC%B0%AC%EC%84%9C%EB%B9%84%EC%8A%A4/%EA%B3%B5%ED%86%B5-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)

## 프로그래밍 요구사항

- React framework 기반으로 개발한다.
- CRA(Create React App) 을 사용해서 기본 개발 환경을 구성한다.
- React기반 스타일링은 emotion과 같은 'css in js' 방식의 라이브러리를 사용한다. 가장 인기있는 라이브러리를 찾아서 사용한다.
- Slide 기능은 라이브러리를 사용할 수 있다.
- 3가지 반찬 종류의 슬라이드 UI를 구성하기 위해서 서버에 3개의 API요청을 병렬로 각각 보내야 한다.

## 회고

이번미션에서 react와 styled component를 처음 사용해봤는데 두가지 모두 잘 알지 못하고 쓴 것 같아서 많이 아쉽다. 이번 주말에 열심히 공부해서 다음미션때는 react를 좀 더 깊게 이해할 수 있도록 해야겠다.

- ui를 직접 변경하지 않는다.
- 데이터를 바꾸면 렌더링은 react가 해준다. 즉 데이터가 바뀌면 상태가 바뀌며 상태가 바뀌면 렌더링이 된다.

두가지가 중요한 포인트같다. 또한 이번 미션에서는 oAuth라는 새로운 개념을 공부했다. access token을 받기위한 복잡한 과정과 각각의 관계에 대해 공부했지만 이또한 추가 공부가 필요하다는 것을 느꼈다. 이번 미션에서 토큰을 활용해서 로그인과 로그아웃 여부를 확인하는 코드를 구현하지 못해 아쉬움이 크다. 이번 미션은 전반적으로 아쉬움이 큰 미션이었다. 반성을 통해 다음에는 이런 아쉬움이 남지 않도록 더 발전해야겠다.

## 공부한 키워드

- react
- styled component
- oAuth

## 추가로 공부할 것

- 인증, 쿠키, 세션 등...
- react (hooks)
- material-ui
- axios

## 잘한 점

- 공부에 집중하며 기능 구현도 완료 한 것
- 배포시간을 맞춘 것
- 매일 빌드파일을 생성 한 것
- 매일 스크럼을 통해 팀원들과 소통한 것
- 새로운 개념을 많이 배우고 적용한 것

## 아쉬운 점

- 초반에 react 공부에 집중했는데 생각보다 효율적으로 공부를 한 것 같지 않아서 아쉽다.
  공부 방법을 잘못한 것 같다. 주말에 다시 react 공부를 제대로 할 계획이다.

- 이번 주 공부할 키워드가 많아서 이것저것 다 얕게만 알고 적용한 것 같다. 더 깊은 공부가 필요

- 학원에 많이 못 나와서 팀원들과 이야기를 많이 못 나눈 것 같다. 앞으로는 학원 나오는 날을 좀 더 늘려야겠다.

- 좀 더 디테일한 부분도 신경쓰며 구현 할 필요가 있다.

[회고](https://docs.google.com/spreadsheets/d/1ochEHhdpodDV29CX_8cA_X2NDwgcH2VXLZidgj4cxlE/edit#gid=490556856)

[issue](https://github.com/codesquad-member-2020/sidedish-04/issues?page=2&q=is%3Aissue+sort%3Aupdated-desc+is%3Aclosed)

## 코드리뷰

[코드리뷰](https://github.com/codesquad-member-2020/sidedish-04/pull/58)

### 잘한 점

- 컴포넌트 단위가 적당하고 좋다.

- app.js (entry point)가 깔끔한 점

### 아쉬운 점

- Global.jsx파일은 css문자열을 담고 있는 js기 때문에 확장자를 jsx로 하기보단 /src/styles/global.js 이런식의 path로 할 수도 있다.

- 공통적으로 사용되는 값들은 css variables 를 활용
  [참고](medium.com/fbdevclagos/how-to-leverage-styled-components-and-css-variables-to-build-truly-reusable-components-in-react-4bbf50467666)

- Carousel.jsx파일에서 onClick의 핸들러 함수를 분리해서 선언하도록 하자
