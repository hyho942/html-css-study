# [Semantic Markup] / 시멘틱 마크업

## [Markup tag]

##### header

    <div id=”header”>
    <header class="header">

header는 html 문서에 첫 머리말로 사용이 가능하여 여러번 사용이 가능하다. 즉 section, body 안에 header을 사용하여 구분을 짓기 위해 사용이 가능하다.

##### footer

    <div id="footer">
    <footer class="footer">

Webpage의 Copyright이나 회사 주소 정보를 사용 할 수 있다.
section에 꼬리말로 사용하고 html 내에서 다수 사용이 가능하다.

##### section

    <div id="section" class="section"></div>
    <section id="#" class="#"></section>

콘텐츠를 grouping 할 때 사용. Section 안에 section을 사용 할 수 있어서 중첩 사용이 가능하다.

##### nav

    <div id="nav" class="nav"></div>
    <nav id="#" class="#"></nav>

Navigation의 줄임말. navigation 메뉴를 나타낸다. 주로 헤딩 부분에 사용하지만, body 내부에 navigation 섹션에도 사용이 가능하다.

##### article

    <div id="article" class="article"></div>
    <article id="#" class="#"></article>

독립적인 글들을 나타낼 때 사용. 블로그 포스팅 표현 할 때 사용하지만, RSS feed로 배포할 가치가 있는 컨텐츠에 사용한다.

##### aside

    <div id="aside" class="aside"></div>
    <aside id="#" class="#"></aside>

콘텐츠와 관계 있는 부가 정보들을 표시 할 때 사용한다. 주로 side-bar콘텐츠들을 담기 위해 사용하기도 한다.

##### main

    <div id="main" class="main"></div>
    <main id="#" class="#"></main>

주로 웹 페이지를 구성하는 메인 콘텐츠를 담는 태그이다. body 태그를 사용하여 구분할 수 있다.
