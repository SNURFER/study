## React UI library 조사

### ui 컴포넌트 라이브러리란? 
주로 사용되는 button, input, dialog등과 같은 기본 UI component들의 집합. 모듈화 되어있기 때문에 다양한 조합으로 UI 디자인이 가능함. 각 라이브러리마다 독특한 모양의 특징을 가지고 있지만, 대부분은 테마를 제공하여 어느정도 커스터마이징이 가능함. 

* [필요성](https://sunscrapers.com/blog/when-to-use-a-ui-component-library-in-a-react-project/)
	* 개발속도에 이점 
		* 존재하는 컴포넌트들의 조합으로 빠른 구현 가능
		* 커스텀화가 필요하더라도 직접 스타일을 구현하는 것 보다 속도의 이점이 있음 
	* 사용성에 이점 
		* 문서화가 잘되어있음 
		* 코드 블록을 단순이 붙여넣는 것만으로도 구현이 가능
	* 브라우저 호환성 지원
	* 다국어 사용(i18n)
		* RTL 지원  
	* 필수 UI컴포넌트 지원
		* modal, toast or snackbar, input form, form validation
	* 모바일 반응형 페이지 지원
* 주의사항
	* library 스타일에 귀속되는 경향 
	* 디자인 방향의 변경이 힘듬 
	* 번들사이즈가 큼 

### 최근 동향
* 빠른 기술 동향으로 최근 5년간 점유율은 계속 바뀌고 있음
* 주로사용하는 상위 제품은 머테리얼, 부트스트랩, Ant 등등
---
### Material UI
* [특징](https://flatlogic.com/blog/bootstrap-vs-material-ui-which-one-to-use-for-the-next-web-app/)
	* MIT 라이센스
	* 2021년 가장 많이 사용되는 라이브러리 
		* 이슈가 생겼을 때 troubleshooting이 용이함 
	* 머테리얼 디자인 원리를 잘 따르는 리액트 ui 프레임워크
		* floating button, long shadow
		* 머테리얼 디자인은 구글의 모든 제품에 사용됨
		* 기존의 안드로이드 UX의 단점을 극복하여 통일성 있는 사용자 경험을 제공하고자 개발됨
			* 미니멀리즘
			* 플랫디자인에 입체감과 원근감을 더함
	* 구글에서 만들었음
		* long time support 가능
	* 나사, 아마존, 유니티, 구글, jp모건 등에 사용됨
	* 12 column 그리드 시스템  풀 반응형 디자인 제공
		* 그리드 시스템은 스마트폰과, 데스크톱을 위한거며 모든 플랫폼에 가독성 좋은 ui를 제공 
	* 사용자 친화적 (모바일 우선) 
	* jQuery를 사용안하고 있음 
		* jQuery를 사용하게 되면 React의 Virtual DOM개념과 섞여 문제가 발생할 수 있음 (어떤 문제인지 확인)
	* 테마 기반으로 제작 가능 
	* 여러 서드파티 라이브러리와 연동 가능 
	* 타입스크립트 플로우 타입 모두 지원  
	* 번들사이즈 314kb
* 단점
	* 리액트 베이스로만 가능
		* 머테리얼 디자인은 서드파티 없이 순수 css로 함
	* 개발 속도가 부트스트랩보다는 느림 하지만 템플릿을 사용하면 빨라질 수 있음
	* 수 많은 ui들이 존재해서 평균적인 ux와의 일관성은 떨어지지만 커스텀이 수월함 
---
### BootStrap
* [특징](https://flatlogic.com/blog/bootstrap-vs-material-ui-which-one-to-use-for-the-next-web-app/)
	* MIT 라이센스
	* 트위터에서 만들었음
	* 따로 디자인 규칙이 없음 
	* 반응형 웹 앱을 만드는데 도와주는 CSS, HTML, JS 프레임워크
	* 에어비앤비, 드롭박스, 애플 뮤직, 트위터, 블룸버그 등에 사용
* 장점
	* 12 column 그리드 시스템으로 풀 반응형 디자인을 제공
	* 재사용성으로 개발에 가속화 가능
	* ux의 친숙성과 일관성을 가지고 있고, 평균적인 커스텀화가 가능하다. 
	* IE 까지 지원 
* 단점
	* [부트스트랩 기반 앱은 무겁고 느릴 수 있음](https://www.upgrad.com/blog/bootstrap-vs-material/)
		* 필요없는 컴포넌트들과 js스크립트를 없애면 해결 가능 
	*  javascript framework(특히 jQuery), css class 등의 의존성을 가질 수 있음 
		* react용으로 나온게 ReactStrap, react bootstrap 임
			* 컴포넌트의 사용방식에 따라 보통 사용함
	
#### ReactStrap(bootstrap 4기반)
* [클래스 컴포넌트를 사용하여 state관리](https://www.geeksforgeeks.org/difference-between-reactstrap-and-react-bootstrap/)
* jQuery 의존성을 가지지 않음

#### React Bootstrap(더 많이 사용)
* 번들사이즈 180kb
* 2019년 이전에는 제일 많이 쓰였음
* stateless. 함수 컴포넌트와 hooks를 이용하고 있음 
* jQuery 의존성
	* [ 최근까진 의존성 있었으나 더이상은 의존성을 가지지 않는다고 함](https://www.geeksforgeeks.org/difference-between-reactstrap-and-react-bootstrap/)
* CSS 라이브러리를 기반으로 만들어짐
	* CSS에 대한 이해나 경험이 필요 
---
### Fluent UI 
* MIT license
	* [fabric assets 들중 MS office를 연상 시키는 것들에 대한 제약이 있음](https://static2.sharepointonline.com/files/fabric/assets/microsoft_fabric_assets_license_agreement_nov_2019.pdf)
* Fluent Design을 따르는 react UI 컴포넌트 라이브러리
* MS에서 개발 
	* long time support 가능
	* 오피스365, 원드라이브
* Material Design과 함께 UI/UX 개발에서 가장 핫한 디자인 
* 최근에 나왔고(2017년), 빠른 속도로 성장 중 
* Typescript와의 사용가능
* office ui-fabric 가 Fluent UI로 됨 
* [개발이 쉬움, 스타일 테마 적용 가능](https://github.com/microsoft/fluentui/wiki/How-to-apply-theme-to-Fluent-UI-React-components)
* [Fluent Design이 갖는 material 디자인과의 차별성](https://www.cygnismedia.com/blog/microsoft-fluent-vs-material-design-system/)
	* 현실과 혼합된 환경에서의 디자인을 제공
		* 미래지향적. 빛 기반 클릭과 터치
		* 공간감을 보여주는 UX 
		* 다양한 인풋에 대한 지원 
		* 공간감 있는 텍스트
	* virtual reality app을 위한 디자인을 제공할 예정
---
### Ant Design
* 중국 알리바바에서 개발 됨 
	* 텐센트, 알리바바 등에 사용됨
* Typescript 기반으로 제작된 라이브러리
* 개발이 쉬움 
* 커스터마이징 할 수 있는 버튼이 적음 
* 번들사이즈가 가장 큼 2.2mb
---


## 정리

|항목| Material UI| Bootstrap| fluent UI| Ant Design|
|:--:|:--:|:--:|:--:|:--:|
|점유율|제일 많음|많음|적음|많음|
|컴포넌트수|많음|[제일 많음](https://www.upgrad.com/blog/bootstrap-vs-material/)|보통|적음|
|커스터마이징|보통|보통이하|보통|보통|
|유지보수|좋음|[제일 좋음](https://jelvix.com/blog/bootstrap-vs-material)|좋음|좋음|
|편의성|좋음|좋음|좋음|좋음|
|호환성|좋음|[모름](https://techblog.woowahan.com/2599/)|좋음||

*  [커스터마이징은 각 디자인 원리에서 벗어나긴 힘들다.](https://stackoverflow.com/questions/55469841/react-is-using-ui-framework-still-benefical-when-you-to-customize-styles-heavil)
* Material/Bootstrap 혼합도 가능
	* mdbootstrap
	* 그냥 추가로 얹어서 써도됨

### React Virtualized
Windowing 라이브러리. 긴 목록을 렌더링 하는경우 최적화를 위해 사용.(스크롤)

