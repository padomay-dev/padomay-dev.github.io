---
title: JEKYLL minimal-mistakes 사이드바 좌우 여백 줄이기 및 없에기
categories:
- jekyll
tags:
- jekyll
- minimal-mistakes
- algorithm
toc: true
---

# minimal-mistakes 사이드바
minimal-mistatkes 사이드바가 넓고 메인이 작이 글이 짤리는게 안좋아 변경할 점을 찾아보았다.  

그래서 관련방법을 찾아보았는데 방법은 다음과 같다.

## 1.좌우 사이드바 크기 줄이기
### _sass/minimal-mistakes/_variables.scss 수정

mmistatkes 사용자에 따라 반응형 레이아웃을 변화 시키는데  
창이 좁을떄 ,보통, 넓을때로 3가지로 변화한다.  

![](/assets/images/minimal-mistakes-sidbar-variables.PNG)


레이아웃을 바꿀려면 위 설정에서 px를 바꾸면 된다. 나는 width와 wide의 px값을 50줄였다. 
  
right-sidebar라는 명칭을 가지고 있지만 실제론 양쪽 사이드바에서 사용되는 설정이다. 

## 2. 메인 페이지 오른쪽 사이드바 없에기
메인 페이지에서는 딱히 쓰지도 않는데 기본설정으로 오른쪽 패딩이 존재한다.
이 부분이 거슬려서 없에주었다.
### _sass/minimal-mistakes/_archive.scss 수정
![](/assets/images/minimal-mistakes-main-right-padding.PNG)  
위 padding-right 부분을 주석처리하면된다.
