---
title: 개발자 블로그 2. 깃허브 블로그 내맘대로 바꾸기.
date: 2023-02-04 21:21:00 +0800
categories: [블로그, 블로그 만들기]
tags: [개발자 블로그]
math: true
mermaid: true
pin : false
image:
  path: /images/2023-02-04-start-github-blog/thumbnail.png
  alt: 개발자 블로그 2. 깃허브 블로그 내맘대로 바꾸기.
---
<!-- 소제목 -->
> ## 깃허브 블로그 템플릿 선정!
> 하려고 보니까 마음에 드는 템플릿이 없네..?!
> {: style="color:gray; font-size: 85%; text-align: left;"}

이전 게시글에 정리했던 <u>블로그 템플릿을 선정하는 조건에 따라</u> 열심히 뒤적뒤적 해본 결과,  
아쉽게도 제가 원하는 템플릿이 없었습니다.😹

아무래도 제가 주로 진행하는 프로젝트들의 게시글을 작성하려고 보면, 글보다는 사진이 많기 때문에  
블로그 홈에 프로젝트를 대표 사진들이 그리드 형태로 나열되어 있길 바랬는데, 마음에 드는 디자인 중에는 없더라구요!

다만, 마음에드는 템플릿인데 조금 수정하면 되어보이는 녀석이 있어 한번 뜯어 고쳐 보겠습니다.  
<strong>(진짜 내가 이거 하고싶어서 깃허브 블로그 시작함.. 헷)</strong>

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

우선 제가 고른 템플릿은 Jekyll의 Chirpy테마 입니다.

<!-- 이미지 -->
![Chirpy 템플릿 설명 캡쳐](/images/2023-02-04-start-github-blog/Screen Shot 2023-02-04 at 11.48.13 PM.png)
<!-- 이미지 설명 -->
Jekyll의 Chirpy 테마 템플릿, <a href="https://chirpy.cotes.page/">블로그 데모버전 미리보기</a>
{: style="color:gray; font-size: 85%; text-align: center;"}

무료 템플릿 이면서도 수정 및 커스텀 가능하고, 여러 기본 기능들을 제공해 준다고 합니다.  
예를 들면 '라이트/다크모드 설정', '댓글기능' 등등.

특히 프로젝트의 '_layouts'폴더에 Chirpy테마의 .html파일들이 있기 때문에,  
html태그를 조금 만져보신 분들이라면 손쉽게 커스텀 가능하다는 점이 있습니다!

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

<!-- 이미지 -->
![Chirpy 템플릿 설명 캡쳐](/images/2023-02-04-start-github-blog/Screen Shot 2023-01-24 at 1.16.16 AM.png)
<!-- 이미지 설명 -->
Jekyll의 Chirpy 테마 GitHub : <a href="https://github.com/cotes2020/jekyll-theme-chirpy">https://github.com/cotes2020/jekyll-theme-chirpy</a>
{: style="color:gray; font-size: 85%; text-align: center;"}

> ### Jekyll의 Chirpy테마 블로그 만들기 설명 관련글 :
> - <a href="https://j1mmyson.github.io/posts/StartingBlog/#installation">Jekyll의 Chirpy테마로 깃허브 블로그 만들기  [j1mmyson님 블로그]</a>  
> - <a href="https://www.irgroup.org/posts/jekyll-chirpy/">Jekyll Chirpy 테마 사용하여 블로그 만들기  [하얀눈길 블로그]</a>

<br>

동일한 Chirpy 테마를 활용해 깃허브 블로그 만드는 법에 대해 작성되어 있는 블로그 입니다.  
보다 설명글을 잘 작성할 자신이 없기 때문에, 만드는 법은 위의 게시글을 참고해 주세요!  

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

<!-- 이미지 2장 콜라주 -->
<div style="width: 49%; height: auto; float:left;">
  <img alt="text-focused(텍스트 중심) 블로그 디자인" src="/images/2023-02-04-start-github-blog/Screen Shot 2023-02-08 at 12.32.28 AM.png">
</div>
<div style="width: 49%; height: auto; float:right;">
  <img alt="image-focused(이미지 중심) 블로그 디자인" src="/images/2023-02-04-start-github-blog/Screen Shot 2023-02-08 at 12.31.49 AM.png">
</div><div style="clear:both;"></div>

<!-- 이미지 설명 -->
[왼쪽] text-focused(텍스트 중심)원래 디자인, [오른쪽] image-focused(이미지 중심) 바꾼 디자인
{: style="color:gray; font-size: 85%; text-align: center;"}

다만, 저는 기존 <strong>'text-focused(텍스트 중심)' 이었던 블로그의 형태를 'image-focused(이미지 중심)'</strong>로  
디자인을 커스텀 해 보았는데요, 그에 대한 이야기를 해보려고 합니다.

<!-- 소제목 -->
> ## 블로그 템플릿 뜯어 고칠곳 찾기.
> 뜯어 고치긴 할건데... 어디를 뜯어 고치면 되는걸까나?
> {: style="color:gray; font-size: 85%; text-align: left;"}

우선 디자인을 커스텀을 하기 위해서는, 커스텀을 할 페이지의 html파일이 어디 있는지 알아야 합니다.  
조금 더 고급진 방법이 있을지 모르겠지만, 일단 제가 한 방식을 소개해 드리겠습니다.

<!-- 이미지 -->
![개발자 도구 캡처](/images/2023-02-04-start-github-blog/Screen-Recording-2023-02-08-at-2.07.43-AM.gif)
<!-- 이미지 설명 -->
chrome브라우저의 '개발자 도구'. 현재 보고 있는 페이지의 html, css, js등등 에 대한 정보가 나온다.
{: style="color:gray; font-size: 85%; text-align: center;"}

요즘 제일 많이 쓰는 chrome브라우저에는 '개발자 도구'라는 것을 지원해 줍니다.  

<strong>[개발자 도구 단축키]</strong>  
Mac : `Command + Shift + c`  
윈도우 : `Window + Shift + c`  

단축키를 누르면 위에서 보다시피 html코드가 나오는데요, 그중 내가 바꾸고 싶은 부분을 지정해보며  
html 코드가 가장 복잡해 보이는(특징이 있어 보이는) 부분을 선택합니다.

```html
<div class="post-meta text-muted d-flex">
```

제가 찾은 가장 복잡해 보이는(특징이 있어 보이는) 문구는 위와 같고,  
이를 프로젝트 폴더 내의 모든 `html` 파일을 대상으로 검색을 해줍니다.  

```html
---
layout: page
# The Home page layout
---

...생략

<div id="post-list">

    <div class="post-preview">
      
      ...생략

      <div class="post-meta text-muted d-flex">
        <div class="mr-auto">

          ...생략

        </div>  
      </div> <!-- .post-meta -->

    </div> <!-- .post-review -->

</div> <!-- #post-list -->

```
{: file='프로젝트명/_layout/home.html'}

검색을 하다보니, `프로젝트명/_layout/home.html` 파일에 해당 문구가 있고,  
이제 이 파일을 잘 수정하면 우리가 원하는 디자인으로 바꾸어 낼 수 있다는 것도 알게되었습니다. 

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

그럼 `프로젝트명/_layout/home.html` 파일에서 어디 부부을 수정해야,  
우리가 원하는 템플릿을 완성시킬 수 있을까요?

<!-- 이미지 -->
![개발자 도구 사용 캡처](/images/2023-02-04-start-github-blog/Screen Shot 2023-03-05 at 11.11.06 PM.png)
<!-- 이미지 설명 -->
chrome브라우저의 '개발자 도구'를 사용하여, 내가 바꾸고 싶은 정확한 위치를 찾아낼 수 있다.
{: style="color:gray; font-size: 85%; text-align: center;"}

역시나, 개발자 도구를 사용해서 파일 내 어디를 뜯어 고칠지 정확한 위치를 찾아봅니다.  

저는 블로그 템플릿의 홈 화면에서 게시물들이 보여지는 영역(division)만 바꾸고 싶기 때문에,  
`<div id="post-list">`태그가 포함하고 있는 부분을 제 입맛에 맞게 바꾸어 보겠습니다!

<!-- 소제목 -->
> ## image-focused(이미지 중심) 형태로 바꾸기
> 진짜 내가 이거 하고싶어서 깃허브 블로그 한다 후..
> {: style="color:gray; font-size: 85%; text-align: left;"}

우선은 프로젝트 대표 이미지를 <strong>'반응형 그리드'</strong> 형태로 나열될 수 있도록 해보겠습니다. 

<!-- 이미지 -->
![개발자 도구 캡처](/images/2023-02-04-start-github-blog/ezgif.com-video-to-gif.gif)
{: style="width: 100%; height: 100% text-align: center;"}
<!-- 이미지 설명 -->
chrome브라우저의 '개발자 도구' 에서 모바일 화면 보기(Toggle device toolbar)기능을 사용하여 테스트.
{: style="color:gray; font-size: 85%; text-align: center;"}

<strong>'반응형 그리드'</strong> 형태로 하는 이유는,  
기기별로 지원하는 해상도에 따라 게시물들을 기분좋게(?) 딱 맞추어 보여지게 하기 위해서 입니다.  

> ### grid 반응형 layout 만들기 관련글 :
> - <a href="https://goddino.tistory.com/246">CSS grid 반응형 layout 적용  [코딩하는 갓디노님 블로그]</a>

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>
여러 고수분들의 블로그를 참고하여, 다음과 같이 `html`을 작성해 주었습니다!

```html
---
layout: page
# The Home page layout
---

...생략

<div id="post-list">
  <div class="post-preview">
    <div style="display:grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); grid-gap: 25px;">
      {% raw %}
      {% for post in posts %}
        <div style="width: auto; height: 340px;">
          <div style="height: 70%; position: relative; overflow: hidden;">
            <img src="{{ post.image.path }}" alt="썸네일">
          </div>
          <div style="height: 3%;"></div>
          <div style="height: 25%;">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
            {% include datetime.html date=post.date %}
            {% if post.pin %}
              <i class="fas fa-thumbtack fa-fw"></i>
            {% endif %}
          </div>
        </div>
      {% endfor %}
      {% endraw %}
    </div>
  </div>
</div> <!-- #post-list -->

```
{: file='프로젝트명/_layout/home.html'}

기존에 있던 템플릿 태그( {% raw %}{% 어쩌구 %}{% endraw %} )의 값들을 최대한 활용하여,  
블로그 홈에 보여지고자 하는 정보를 요약하여 볼 수 있도록 코드를 작성해 주었습니다.  

여기서 템플릿 태그란, `html`에 동적인 구문을 삽입할 수 있도록 해주는 태그 입니다.

<!-- 중간 바 -->
<br>
<hr style="width: 30%">
<br>

이제야 깃허브 블로그 다 만들었따!  
긴글 읽어주셔서 감사합니다 😉

