# v3.0.0b (February 9, 2014)
v3.0.0b는 pre-release입니다. history.md에 기재하지 않은 수정 또는 변경 사항이 있을 수 있습니다. 

- (티스토리 제외) Bootstrap 3 for IE7(beta) 추가.  https://github.com/coliff/bootstrap-ie7 `Requirements`  Boostrap 3 uses the box-sizing property for layouts which is not natively supported by IE7. The polyfill 'boxsizing.htc' is required: https://github.com/Schepp/box-sizing-polyfill
- (티스토리 제외) respond-1.4.2.min.js v1.1.0에서 v1.4.2로 업데이트 https://github.com/scottjehl/Respond
- jquery 업데이트 v1.10.1에서 v1.10.2로 업데이트 https://developers.google.com/speed/libraries/devguide
- html5shiv 업데이트 v3.6.2에서 v3.7.0으로 업데이트 https://github.com/aFarkas/html5shiv
	IE7, IE8에서 `main` HTML5 태그지원 스크립트 삭제 
- flaunt.min.js 메뉴 스크립트 추가 
- script.js 수정 
- 링크 `#none` 없애고 `#`만으로 수정 script.js
- bootstrap 자바스크립트는 min으로 변경
- ie.css 수정 `.ie7`, `.ie8` 브라우저 감지
- ie7부터 `해피브라우저` 적용, 한글 추가 http://browsehappy.com/ 
- bootstrap3 v3.1.0 업데이트 http://blog.getbootstrap.com/2014/01/30/bootstrap-3-1-0-released/
- bootstrap3 `.container-fluid` 추가(정규 클래스) 
- bootstrap3 `col-*-nospace-*` 개별 nospace 클래스 삭제 
- bootstrap3의 navbar 사용 시 navbar.less에서 `border` 각주 처리 
- bootstrap3의 navbar 대신 flaunt 내비게이션 메뉴로 변경, 티스토리에서 IE7, IE8 지원  `skeleton-nav` 
	티스토리에서는 `navbar.less`와 `navs.less`는 각주 처리 
- 사이트 헤더에 커버 이미지(1170px * 400px) 적용, 이미지는 백그라운드 CSS  `skeleton-header`
	백그라운드 이미지를 반응형웹에 대응, 400/1170 = 0.3418% =  `padding-top: 34.18%`
- 사이트 헤더의 hgroup `h1`, `h2`는 text-indent: -9999로 적용 
- 사이트 헤더는 메인 페이지에서만 출력. 개별 페이지에서는 감춤
- 사이트 미들 배너 추가. 폰트 리사이즈, 폰트 패밀리 변경, 프린트 버튼 적용 
	티스토리의 제한된 개별 페이지마다의 중복 코드 삭제 
	내비게이션 메뉴 적용했던 검색 input을 미들 배너로 변경 
- 사이트 내 중요 링크들에 `.global-links` 적용
- 최신글 위젯 IE7 CSS 버그 수정
- 아이콘 font-awesome v3.2.1 대신에 개별 아이콘 적용. `SVG` 파일. IE9 이하에서는 `png` 파일로 대체
    > font-awesome v3.2.1 사용 시 skin.html의 &lt;head&gt;에 코드 추가(유저 선택)
    > &lt;link href="//netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.min.css" rel="stylesheet"&gt;
	> &lt;!--[if IE 7]&gt;
	>   &lt;link href="//netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome-ie7.min.css" rel="stylesheet"&gt;
	> &lt;![endif]--&gt;
	
- style.css 파일에서 ie.css에 넣지 않는 속성은 `\9`로 적용 
- style.css에서 `.text-justify` 삭제. bootstrap.less에 정규 클래스로 추가됨
- style.css에서 `.img-center` 삭제. bootstrap.less에 정규 클래스로 추가됨
- license-links를 `footer-links`로 수정 
- `.entry-content img {}`에 IE 핵 추가 
- 파비콘 링크수정./images/favicon.ico
- print.less에 추가  
	  >.skeleton-nav,.skeleton-header,.skeleton-mid-banner,.alert,.actionTrail,.paging,form,aside,.tistorytoolbar,.scrollup {display: none !important;}

- npm tistory-spidersweb-grunt와 tistory-doobedoo-grunt 버전 `1.1.0`으로 업데이트 
- grunt에서 `grunt-recess` 삭제, `grunt-contrib-less` 추가, 참고 bootstrap 3 blog http://blog.getbootstrap.com/2014/01/30/bootstrap-3-1-0-released/
	> nodejs v0.10.24
	> "grunt": "~0.4.2",
	> "grunt-contrib-clean": "~0.5.0",
	> "grunt-contrib-jshint": "~0.8.0",
	> "grunt-contrib-uglify": "~0.3.2",
	> "grunt-contrib-watch": "~0.5.3",
	> "grunt-contrib-less": "~0.9.0"
- CSS `grunt` 실행 후 bootstrap.css 파일 사이즈 81KB (정규 123KB)
- JavaScript `grunt` 실행 후 bootstrap.min.js(부트스크랩 외 기타 자바스크립트 포함) 파일 사이즈 35KB (정규 25KB)

# v1.2.2 (October 20, 2013)

- `admin`, `local`, `tags` 등 링크 추가

# v1.2.1 (October 6, 2013)

- 카테고리 소분류 CSS 추가
- 위젯 타이틀 오류 수정

# v1.2.0 (September 29, 2013)

- `grunt.js` 추가.
- `widget-inner` 썸네일 지원 최신글목록에서는 변경. (thanks 막쿼러버님)

# v1.0.2 (September 14, 2013)

- `티에디션` 지원. 단, 작은 썸네일 포함된 리스트 (유저선택)
-`.imageblock` 위지윅에디터 이미지 삽입가능 (thanks for an anonymous tip)
- `Media Queries` 콘텐츠와 사이드바 영역 구분선 768px 이하 삭제
- `col-lg-*` bootstrap v3 공식 업데이트 전 사용하던 불필요한 grid 삭제
- `figure`, `figcaption` 여백 재설정 caption에 margin:10px 0; 
- `문단간격 없음 사용` 설정 해제. 기존의 콘텐츠에서는 에디터모드에서 체크 해제
- `entry-title` 본문 제목 폰트 사이즈 18px로 설정 
- `pagination`의 `interword` 오류 수정
- `video` `iframe` `object` `embed`에 max-width:100%; `.media-container` 추가

# v1.0.1 (September 3, 2013)

- `bootstrap.css` 레이아웃 추가 및 수정
- `ie.css` for IE8 support. 티스토리에서는 respond.js 사용불가
- `html5shiv.js` 링크 변경
- `Media Queries` 미디어쿼리 변경
- `.img-center` 이미지 가운데 정렬 class 추가 (@정재복 http://jaebok.tistory.com/)

# v1.0.0 (July 1, 2013)

- **Initial release**

