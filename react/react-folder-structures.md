
# 리액트의 폴더 구조

1. Container/Presentational 폴더 구조
- 2019년 이전에 많이 사용했던 폴더 구조
- 함수형 컴포넌트가 나오기 이전에 사용했습니다.

**board**
*Container.js (logic) - 기능*
*Presenter.js (View) - 화면*

- React 16이 발표되면서 hooks function 등장 이후 사용하지 않는 패턴
- 특수한 경우에는 사용하면 좋은 패턴

2. Hooks 폴더 구조
- 최근에 가장 많이 사용하는 폴더 구조

*components -> 모든 페이지에 공유 가능한 컴포넌트 (버튼)*
*hooks -> 상태 관련도니 재사용 리액트 함수*
*pages -> 웹 내 페이지*
*main*
*ㄴhooks -> 해당 페이지에서만 사용하는 리액트 함수*
*ㄴcomponents -> 해당 페이지에서만 사용되는 컴포넌트*
*ㄴindex.js(main.js) -> 컴포넌트들이 조립되는 공간*
*todo*
*board*
*my-page*

*utils -> 유틸 함수 (halper)*
*libs -> 라이브러리 관련된 함수나 폴더가 구성*
*app.js -> 다른 라이브러리를 사용하는 설정이나, 루트 설정*

3. Atomic 폴더 구조
- 이론 상으로는 가장 완벽한 패턴, 어떠한 컴포넌트든 재사용
- atom(원자) 단위로 쪼개서 더이상 분리할 수 없게끔 컴포넌트를 분리


*atoms -> 더 이상 쪼갤 수 없는 컴포넌트*
*molecules -> 여러 개의 atom이 모여 하나의 의미를 갖는 컴포넌트*
*organisms -> 여러 개의 molecules이 모여서 하나의 기능을 갖는 컴포넌트*
*templates -> 여러 개의 organisms가 모여서 하나의 프레임을 갖춘 컴포넌트*
*pages -> 최종본 

4. FSD(Feature, Sliced Design) 폴더 구조

- 프로젝트의 도메인 혹은 기능을 분배하여 폴더 구조를 작성