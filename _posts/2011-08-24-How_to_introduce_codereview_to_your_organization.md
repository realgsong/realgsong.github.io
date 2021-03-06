---
layout: post
title: 코드 리뷰 도입 전 주의해야 할 사항
date: 2011-08-24 17:42:09.000000000 +09:00
type: post
published: true
status: publish
categories:
- Dev
tags:
- code review
- 코드 리뷰
meta:
  _publicize_pending: '1'
  _edit_last: '16961716'
  original_post_id: '4254'
  _wp_old_slug: '4254'
author:
  login: realgsong
  email: realgsong@hotmail.com
  display_name: realgsong
  first_name: Ki-Sung
  last_name: Bae
---
<p>스타트업에 조인하면서 어느 정도 강제성을 가지고 시작했던 것 중 하나가 코드 리뷰 였다. 이 프락티스가 가지고 있는 장점을 알고 있기에, 나중에 큰 비용을 치르며 도입하기 보다 조금 무리가 되더라도 프로젝트 초반부터 익혀두는 편이 좋겠다고 판단되었기 때문이다.</p>
<p>그러나 한 가지 간과했던 것이 있었으니, 프로세스를 행하는 것은 결국 사람이라는 것이다. 하나 둘 수행하면서 배우리라 생각했던 내 기대와는 달리, 함께 코드리뷰를 하던 동료는 거기에서 받는 스트레스를 참고 있었던 것이다.</p>
<p>참고로 동료는 다른 개발자와 함께 일하는 환경을 매우 낯설어 했다. 개발했던 프로젝트 들이 많은 인원이 함께 하는 경우가 별로 없었기 때문이다. 이런 와중에 가장 필요 했던 것은 코드 리뷰에 대한 이해도를 높이는 작업이었는데, 내가 이 점을 놓치고 있었다.</p>
<p>코드 리뷰를 수행하려면 먼저 몇 가지 동의가 우선 되어야 한다. 첫째는 <strong>팀의 코드에 대한 공유 의식</strong>이다. 코드 리뷰는 기본적으로 코드에 대한 공유 의식을 바탕으로 진행된다. 각자의 코드 영역이 분명히 나눠져 있다면, 코드를 쓴 개발자가 따로 부탁하지 않는 한 리뷰를 자제하거나 아주 조심해서 하는 것이 좋다.</p>
<p>두 번째는 왜 코드리뷰가 <strong>필요한지에 대한 공감대 형성</strong>이다. 코드 리뷰의 목적은 쓰여진 코드가 correct 한지 다른 사람의 눈을 통해 검증함으로써 software quality 를 아주 이른 시기에 높이려는 노력이다. 코드 리뷰의 결과는 코드에서 숨겨진 버그를 찾는 것으로 나타나야 한다.</p>
<p>셋째는 코드 리뷰를 <strong>어떻게 해야 하는 지에 대해 공부해야</strong> 한다. 코드 리뷰에서 쓰는 표현들에 대해 리뷰를 하는 사람과 받는 사람 모두 받아들이는 과정이 필요하다. 즉 코드 리뷰 도메인에서 사용할 언어를 세팅하는 것이 필요하다. 예를 들어 리뷰어는 어떻게 해라 라는 결과 보다는 이 코드에 이런 문제가 있지 않나요? 라는 식의 질문을 사용할 것. 코드 리뷰를 받는 사람은 문제 제기가 옳지 않을 경우 거기에 대한 설명이 아니라면, 해당 지적 사항을 개선했는지에 대한 결과만 알려줄 것과 같은 기본 원칙들이다.</p>
<p>마지막으로 이 모든 사항은 팀원 전체와 대화하면서 진행되어야 한다. 대화의 대전제는 팀이 보다 좋은 제품을 만들기 원한다는 것이다.</p>
<p>이에 익숙하지 않은 팀원이 있다면, 강제로 시행하기 보다 교육의 문제로 풀 수가 있는지 여부를 먼저 판단하고, 그것이 어려울 것 같다면 다른 차원에서 문제를 풀 수 있도록 하는 것이 좋다.</p>
