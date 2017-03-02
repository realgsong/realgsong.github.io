---
layout: post
title:  "신입 웹개발자를 위한 개념 장착 가이드"
date:   2017-03-01 18:00:00 +0009
categories: dev
tags: []
image: /assets/article_images/computer.jpg
comments: true
---
웹개발자로 커리어를 시작하는 신입 개발자들에게 유용할 리소스들을 모아서 정리해봤다.

# 자바스크립트 프로그래밍

<div class="ttbReview"><table><tbody><tr><td><a href="http://www.aladin.co.kr/shop/wproduct.aspx?ItemId=78862734&amp;ttbkey=ttbgsong791557002&amp;COPYPaper=1" target="_blank"><img src="http://image.aladin.co.kr/product/7886/27/cover/8966261795_1.jpg" alt="" border="0"/></a></td><td align="left"  style="vertical-align:top;"><a href="http://www.aladin.co.kr/shop/wproduct.aspx?ItemId=78862734&amp;ttbkey=ttbgsong791557002&amp;COPYPaper=1" target="_blank" class="aladdin_title">자바스크립트 완벽 가이드</a> - <img src="http://image.aladin.co.kr/img/common/star_s8.gif" border="0" alt="8점" /><br/>데이비드 플래너건 지음, 구경택 외 옮김/인사이트</td></tr></tbody></table></div>

프로그래밍의 기초를 다지려면, 해당 언어의 레퍼런스 책 하나 정도는 구비하고 있는 것이 좋다. 가격과 두께가 만만찮지만, 자바스크립트의 상승세를 생각해본다면 위 책은 아깝지 않은 투자가 될 것이다.

자바스크립트 개발환경은 사용하는 운영체제와 에디터에 맞게 직접 꾸미면 된다. 웹을 검색해보면 관련 자료들이 넘쳐나니 자신에게 맞는 걸 찾아서 적용해보자. [이 문서](http://javascript.info/tutorial/setup-your-environment) 에 있는 내용을 참고해도 좋다. 단 상용 소프트웨어 사용시에는 회사에서 사용가능한지 라이센스를 체크하고 필요하다면 구매 요청을 하도록 하자.

자바스크립트는 많은 파생 언어들을 낳고 있다. 그 중에서도 [타입스크립트](http://www.typescriptlang.org)는 기존 자바스크립트가 가지고 있는 언어적 약점들을 많이 보완해주어 인기가 날로 상승하는 중이니, 살펴보도록 하자.

# 개발업무
요즘 개발자의 협업은 git 으로 시작해서 끝난다고 보면 된다. 버전 관리 도구에 대한 기본 이해와 함께 Git 사용법 그리고 풀리퀘스트등을 통한 git 기반 협업 방식을 반드시 숙지하도록 하자.

* [A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-ko.html)
* [git - 간편 안내서](https://rogerdudler.github.io/git-guide/index.ko.html)
* [Github를 이용하는 전체 흐름 이해하기](https://blog.outsider.ne.kr/865), [#2](https://blog.outsider.ne.kr/866)

우선은 웹에 있는 자료들로 기초 활용에 필요한 정도만 공부하도록 하자. 시니어가 되려면 아래 책을 한번 읽어 보는 게 필요하다.

<div class="ttbReview"><table><tbody><tr><td><a href="http://www.aladin.co.kr/shop/wproduct.aspx?ItemId=79232604&amp;ttbkey=ttbgsong791557002&amp;COPYPaper=1" target="_blank"><img src="http://image.aladin.co.kr/product/7923/26/cover/8966261787_1.jpg" alt="" border="0"/></a></td><td align="left"  style="vertical-align:top;"><a href="http://www.aladin.co.kr/shop/wproduct.aspx?ItemId=79232604&amp;ttbkey=ttbgsong791557002&amp;COPYPaper=1" target="_blank" class="aladdin_title">프로 Git 2판</a> - <img src="http://image.aladin.co.kr/img/common/star_s8.gif" border="0" alt="8점" /><br/>스캇 샤콘.벤 스트라웁 지음, 박창우.이성환.최용재 옮김/인사이트</td></tr></tbody></table></div>

깃 사용에 익숙해지면 커맨드라인이 제일 편할 테지만, 우선은 여러가지 비쥬얼 툴들을 활용하는 걸로도 충분하다. [깃오피셜 사이트](https://git-scm.com/download/gui/linux)에 여러가지 비쥬얼 툴들을 소개하고 있으니 참고하자.

깃은 branch / merge 에 대해서 무척 관대하다. 그 말인 즉슨 code conflicts 를 다루는 법을 배워야 한다. 신입일 때 당장 필요하진 않더라도, 미리 merge tool 중 하나를 손에 익혀두면 나중에 큰 도움이 될 것이다. 다양한 머지툴에 대한 소개는 [이 링크](http://stackoverflow.com/questions/137102/whats-the-best-visual-merge-tool-for-git)를 참고하기 바란다.

## 버그 리포팅
직접 코드를 쓰는 것도 좋지만 방금 입사한 입장에서 제품 코드에 손을 댈 기회는 많지 않을 수 있다. 그럴 때는 버그리포트를 올리면서 제품과 코드에 대해 익혀나가면 좋다. 버그 리포트 올릴 때는 아래 가이드를 한번만 읽어보자.

* [Bug_writing_guidelines](https://developer.mozilla.org/ko/docs/Mozilla/QA/Bug_writing_guidelines)
* [The ideal bug report](http://blog.testlio.com/the-ideal-bug-report)

# 일반 업무
회사의 모든 일은 이메일로 진행된다. 요즘은 채팅서비스 등을 이용해서 이메일을 조금 덜 쓰고자 하는 움직임도 있지만, 그래도 기본은 이메일이다. 이메일에 격식을 차려 쓰는 건 옛말이고, 간결하게 핵심을 짚어주는 이메일 에티켓을 익혀두는 것이 좋을 것이다.  아래 링크를 참고하자.

* [이메일 쓰는 요령](http://ppss.kr/archives/101094)
* [이메일로 업무 잘 하는 법](https://medium.com/@iox/%EC%9D%B4%EB%A9%94%EC%9D%BC%EB%A1%9C-%EC%97%85%EB%AC%B4-%EC%9E%98-%ED%95%98%EB%8A%94-%EB%B2%95-fff2915145cc#.mjmi6fz0w)

