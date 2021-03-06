---
layout: post
title:  "난감한 버그와 소프트웨어 방법론"
date:   2015-07-28 19:00:00 +0900
categories: Dev
tags: 
image: /assets/article_images/computer.jpg
comments: true
---
선과 모터사이클 관리술에서 일부를 발췌하여 소프트웨어와 연관지어 보려는 글의 다음 편이다. [품질에 관한 지난번의 글](/dev/2015/07/22/how_to_choose_for_quality_and_insight.html)에 비해 이번 글의 주제는 보다 명확하다.

"**아주 어려운 버그를 고치려면 어떻게 접근해야 되는가?** 다시 말해 당신의 버그 픽스 능력을 높이는 효과적인 방법은 무엇인가?"

# 귀납적 추론과 연역적 추론 사이
> 일반 상식으로 해결하기에 너무도 복잡한 문제를 해결하는 데는 귀납적 추론과 연역적 추론이 뒤섞인 일련의 기다란 사유 작업이 요구된다. 예컨대, 모터사이클 관리의 경우, 기계를 직접 눈으로 관찰하는 일과 사용 지침서를 통해 입수한 기계의 계층 체계를 머릿속으로 확인하는 일 사이를 왔다 갔다 하며 양자를 엮어나가는 작업이 요구된다.

버그 픽스 또한 마찬가지이다. 귀납적 추론이라 함은 현재 동작하고 있는 소프트웨어를 관찰하는 일을 말하며, 연역적 추론이라 함은 알고리즘과 코드의 흐름에 대한 계층 체계를 이해하는 것을 말한다. 소프트웨어의 버그를 수정하기 위해서는 이 둘 사이를 왔다갔다 하게 된다.

문제는 여기에서 발생한다. 귀납적 추론이라 함은 사소한 반증 하나만으로도 그 체계가 모두 무너져 버린다. 한편 연역적 사고는 몇 개의 확고한 진실에 기반해서 사고의 체계를 넓혀가게 된다. 바꿔 말해, 프로그래머는 현재 동작 또는 오동작하는 버그의 형태를 면밀히 관찰한 후 나름의 가설을 세우게 되는데, 이 가설에 바탕하여 문제의 근본 원인에 대한 연역적 사고를 진행하게 되는 것이다.

바로 이때 만약 프로그래머가 아주 사소한 실수를 하나 했다고 하자. 예를 들어 로그에 찍힌 중요한 디버깅 메세지 하나를 보지 못하고 지나쳤다고 하자. 이후에 프로그래머가 버그를 수정하기 위해 취한 방법들은 어느 한순간 와르르 무너져 내리고 말 것이다. 왜냐하며 놓쳐버린 사소한 관찰 하나 때문에 연역적 사고에 의해 만든 체계의 밑바탕이 거짓이 되어 버리기 때문이다.

# 과학적 방법
> 따라서 자연을 상대로 할 때 당신은 극도로 조심해야 하고 엄격하게 논리적이어야 한다. 논리적으로 단 한번의 실수라도 하는 경우, 과학이라는 엄청난 성채는 순식간에 몽땅 와해될 것이기 때문이다. 기계에 대한 연역을 단 한번이라도 잘못하는 경우 당신은 끝이 보이지 않는 진퇴양난 속에 빠져들 수밖에 없다.

이런 상황에서 선택할 수 있는 효과적인 것이 바로 과학적 방법이다.

> 정말로 어려운 문제에 부닥쳐서 모든 방법을 다 써보고 또 온통 머리를 쥐어짜보기도 하지만 전혀 해결의 기미가 보이지 않는다고 하자. 그러면 이번에는 자연이 당신에게 정말로 대단한 어려움을 안겨주기로 작정했다는 사실을 깨닫고 당신은 자연에게 이렇게 말할 수도 있겠다. "좋소이다! 나도 이젠 더 이상 부드러운 사람만은 아니라는 걸 보여주겠소." 그런 다음 당신이 동원하는 것이 바로 공인된 과학적 방법이다.   
> ...   
> 과학적 방법의 진정한 목적은 자연이 당신을 잘못 인도하지 않도록 단속을 하는 데 있다. 자연은 당신이 실제로는 모르는 것을 알고 있다는 식으로 착각하도록 당신을 홀릴 수도 있기 때문이다. 

자 그럼 과학적 방법에서 소프트웨어 버그 픽스 작업에 대한 어떤 걸 배워올 수 있을까? 그 배움 중에 어떤 것이 어려운 버그를 수정하는 작업에 있어서 실수를 미연에 방지하는 데 도움을 줄까?

# 기록, 기록, 기록
> 이런 때를 대비해 당신은 관찰 기록부와 같은 것을 따로 마련하여, 여기에다가 모든 것을 공식적인 기록으로 남겨둘 수 있다.   
> ...   
> 과학적 작업 또는 전자공학 기술 분야에서 이 같은 기록 활동은 반드시 필요한 것이다. 그렇게 하지 않으면, 갈수록 문제들이 너무도 복잡해져서 종국에는 그 안에서 길을 잃고 정신이 혼란해질 것이기 때문이다.   
> ...   
> 하지만 혼란이 일기 시작하면 어떻게 해야 할까. 모든 것을 공식적으로 정확하게 기록함으로써 혼란을 억제하는 것이 당신이 취할 수 있는 현명한 처사다.

질문의 답은 기록하는 것이다. 작업 과정에 대한 세세한 기록을 남김으로써 스스로 혼란의 도가니에 빠지는 것을 방지할 수 있다. 보통 과학정 방법론에서 관찰 기록부에 남기는 사안들은 인용한 다음 문단과 같다.

> 관찰 기록부에 들어갈 논리적 진술들은 여섯 개의 범주로 나눌 수 있다. (1) 문제 자체에 대한 진술, (2) 문제의 원인에 대한 가설들, (3) 각각의 가설을 테스트하기 위해 고안된 실험 방법들, (4) 실험을 거쳤을 때 예상되는 결과들, (5) 실험을 통해 관찰된 결과들, (6) 실험의 결과에서 얻은 결론.

기록을 바탕으로한 과학적 방법에서 가장 필요한 핵심 역량이 하나 있다. 그것은 모르는 것에 대해 함부로 언급하지 않는 것, 즉 모르는 것을 모르는 상태로 인정하는 일이다.

> 공인된 과학적 방법의 제1항목에 해당하는 문제 자체에 대한 진술과 관련해서 핵심적 역할을 하는 것은 당신이 알고 있다고 확신하는 것 이상은 절대로 진술하지 않는 역량이다.

# 다시 소프트웨어 개발로 돌아와서
소프트웨어 개발의 과정에서 기록에 대한 중요성도 마찬가지다. 어려운 버그를 고치기 위해 과학적 방법을 택한 경우라면, 그 작업 과정에 대한 상세한 기록이 함께 해야 한다. 사고의 흐름을 쫓아 갈 수 있는 기록이 뒷받침 된다면, 복잡하고 불가능해 보였던 버그 픽스도 더 이상 비현실적인 일이 아니게 될 수 있다는 것이다.

다행스럽게도 현재의 소프트웨어 개발 도구에는 이와 같은 목적을 달성할 수 있도록 해당 기능을 구비한 것들이 많이 있다. 이제 문제는 이 도구들을 어떻게 활용하여 효과를 볼 것인가 결정하는 것이다. 이는 또 다시 방법론의 문제이기도 하다.

나에게 맞는 개발 방법론을 찾는 것, 그 중에서도 개발 과정의 기록을 담당하는 도구에 대한 이해도를 높이고, 활용을 경험해 보는 것. 이 정도가 어려운 버그를 고치기 위한 역량을 갖추기 위한 스텝이라고 할 수 있겠다. 이를 통해 품질을 알아 볼 수 있는 직관을 키울 수 있도록 경험을 늘리게 된다면 그 방향이 옳다고 할 수 있을 것이다.
