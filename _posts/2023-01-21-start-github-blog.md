---
title: 개발자 블로그 1. 깃허브 블로그를 시작해보자.
date: 2023-01-22 22:29:00 +0800
categories: [블로그, 블로그 만들기]
tags: [개발자 블로그]
math: true
mermaid: true
pin : false
image:
  path: /images/2023-01-21-start-github-blog/thumnail.png
  alt: 개발자 블로그 1. Jekyll로 깃허브 블로그 만들기
---
<!-- 소제목 -->
> ## 깃허브 블로그의 시작.
> 블로그를 시작하게 된 이유
> {: style="color:gray; font-size: 85%; text-align: left;"}

<br>

사실 저는 <strong>'네이버 블로그'</strong>를 운영 하고 있었습니다.<br>
나름 첫 게시글 업로드 기준으로 <strong>무려 10년(2013년 ~ 2023년)간</strong> 블로그 활동을 했었죠!😗

<br>

<a href="https://blog.naver.com/siook12">네이버 블로그 '일단 질러보는 성격'</a>

<!-- 이미지 -->
![네이버 블로그 캡쳐](/images/2023-01-21-start-github-blog/Screen Shot 2023-01-29 at 12.27.31 PM.png)
<!-- 이미지 설명 -->
첫 게시글 업로드 2013. 9. 25. '미군꺼라고 우기고 쓰는 그냥 작은 탱크'
{: style="color:gray; font-size: 85%; text-align: center;"}

<br>

열심히 활동을 하고 있던 <strong>'네이버 블로그'</strong>를 떠나<br>
<strong>'git 블로그'</strong>를 시작하게 된 이유는 크게 3가지 정도인 것 같습니다.

<!-- 팁 callout -->
> 1. 내 입맛대로 만든 템플릿과 디자인.
> 2. git이라는 것과 조금 더 친해지기.
> 3. 데이터 아카이빙에서 2WAY DOOR를 확보!
{: .prompt-tip }

<br>

1번, 2번의 이유는 그렇다고 치고, 3번은 뭔소리인지?

점점 진행하는 프로젝트의 빈도수가 늘어나고, 증가하는 데이터의 양.<br>
손실 걱정 없이 프로젝트 데이터를 잘 아카이브 하고 싶지만, 언제 어떻게 될지도 모른다는 생각이 들었습니다.

💻

그리하여 데이터 아카이빙을 하나의 데이터 저장소에 의존하는 방식에서 벗어나<br>
'git저장소' & '로컬(local)저장소' 이렇게 두가지 경로를 확보 가능한 <strong>'깃허브 블로그'</strong>를 시작하게 되었습니다!



<!-- 소제목 -->
> ## 깃허브 블로그를 하려면 코딩을 잘 알아야 하나?
> 모르겠고, 일단 해봅니다.
> {: style="color:gray; font-size: 85%; text-align: left;"}

물론 코딩을 잘 하면, 도움이 될 수도 있습니다.<br>
저도 그렇게 코딩을 잘하지는 않지만, 하면서 충분히 배울 수 있다고 생각합니다.<br>

(진짜 솔직하게 여기까지 글 쓰는데 2주일 걸렸거든요..😩)
{: style="font-size: 70%;"}

<br>

모르겠고 일단 해보겠습니다.<br>
배우면 배우는대로 한번 적어보겠습니다.

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

일단, 구글에 '깃허브 블로그'라고 검색하고 블로그에 잘 정리되어 있는 글들을 쭉 읽어봅니다.

<!-- 이미지 -->
![구글에 '깃허브 블로그' 검색결과 캡처](/images/2023-01-21-start-github-blog/Screen Shot 2023-02-04 at 9.47.37 PM.png)
<!-- 이미지 설명 -->
진짜 구글에 '깃허브 블로그'라 검색해봄.
{: style="color:gray; font-size: 85%; text-align: center;"}

<a href="https://ahnslab.com/21-how-to-start-github-blog/">Github 블로그 시작하는 방법(로컬 설치 없이 쉽게 만들기)</a><br>
<a href="https://www.omdroid.com/338">간단하게 git hub(깃허브) 블로그 만들어보기</a><br>
<a href="https://www.youtube.com/watch?v=ACzFIAOsfpM">깃헙(GitHub) 블로그 10분안에 완성하기</a><br>

...

깃허브가 뭔지, 블로그 만드는법, 심지어 깃허브 계정을 생성하는 과정(?)까지 너무나도 잘 정리되어 있습니다.<br>
더 잘쓸 자신이 없기 때문에, 블로그를 만드는 법은 위의 잘 정리되어 있는 영상 또는 글들을 참고해주시면 되겠습니다.

다만, 간단하게 블로그 생성 과정과 알게된점들을 공유해보도록 하겠습니다.😗

<!-- 소제목 -->
> ## 깃허브 블로그 템플릿 선정.
> 역시 똑똑한 사람들이 많아~
> {: style="color:gray; font-size: 85%; text-align: left;"}

우선 깃허브 블로그를 쉽게 만들어 낼 수 있다는 Jekell 무료 블로그 템플릿을 사이트를 방문하여<br>
원하는 블로그 템플릿을 골라 주었습니다.

<!-- 이미지 -->
![Jekell 템플릿 사이트 캡처](/images/2023-01-21-start-github-blog/Screen Shot 2023-02-04 at 9.19.32 PM.png)
<!-- 이미지 설명 -->
Jekell 템플릿 공유 사이트 : 블로그, 포트폴리오, 비즈니스 등등 여러 템플릿들이 있다. (<a href="https://jekyllthemes.io/free">Jekell themes</a>)
{: style="color:gray; font-size: 85%; text-align: center;"}

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

위의 'Jekell themes' 에는 정말 많은 템플릿들이 공유되어 있는데요,<br>
내가 원하는 템플릿을 고를 때, 아래의 조건들을 참고하여 골라 보면 좋을 것 같습니다.

<!-- 팁 callout -->
> - 블로그 <strong>VS</strong> 포트폴리오
> - 게시물 단위 <strong>VS</strong> 프로젝트 단위
> - text-focused(텍스트 중심) <strong>VS</strong> image-focused(이미지 중심)
{: .prompt-tip }

### - 블로그 <strong>VS</strong> 포트폴리오

우선, 자신이 블로그를 작성하는 이유 또는 성향에 따라<br>
블로그의 형태가 될 수도 있고, 포트폴리오의 형태가 될 수도 있습니다.

저는 <u>무언가 새롭게 알게 된것을 공부하여 정리하고, 비슷한 누군가가 볼 수 있도록 정리</u>하는 블로그의 형태를 지향.<br>
다만, 블로그 자체가 포트폴리오가 될 수 있다는 것을 생각하며 템플릿을 선정하였습니다.

<br>

### - 게시물 단위 <strong>VS</strong> 프로젝트 단위

자신이 올리고자 하는 글들이 하나하나의 게시물 단위인지, <br>
프로젝트 단위로 게시물들이 정리될지에 따라 원하는 디자인의 형태가 달라질 수 있습니다.

저는 프로젝트 중심으로 게시물들을 작성하기 때문에, 프로젝트 단위로 목차를 나눌 수 있는 템플릿을 지향.<br>
<u>프로젝트별로 목차가 상단바, 배너에 잘 정리될 수 있는 블로그 템플릿</u>의 형태를 선정하였습니다.

<br>

### - text-focused(텍스트 중심) <strong>VS</strong> image-focused(이미지 중심)

자신이 올리고자 하는 글들이 글이 많으 게시글인지, <br>
이미지 중심으로 설명하는 게시글인지에 따라 메인 페이지(home.html)가 달라질 수 있습니다.

저는 주로 만드는것과 메커니즘 설명을 주로 하기 때문에, 자연스레 이미지가 많이 들어가고<br>
글도 잘 못쓰기(?) 때문에 <u>이미지를 깔끔하게 보여줄 수 있는 형태의 블로그 템플릿</u>을 선정하였습니다.

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

일단 끝.

(깃허브 블로그 글 하나 쓰기 정말 어렵네요...😩 한템포 쉬었다 가보겠습니다.)
{: style="font-size: 70%;"}