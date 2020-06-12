---
title: JEKYLL _posts 파일이름에 한글 쓰기
tags:
- jekyll
- minimal-mistakes
- encoding
categories:
- jekyll
toc: true
toc_label: posts 한글이름
---

# _posts에 파일이름쓰기
jekyll  포스팅을 할때 포스팅 파일이름에 한글을 쓰고 local에서 해당 페이지에 접속해보면 404오류가 뜬다.  그래서 이거 가지고 url에 percent encoding  적용 해보고 별짓을 다해봤으나 실패하였다.   
이 문제는 알고보니 내 window의 encoding이 한글(MS949) 이여서 생긴 문제였다. ㅡㅡ  
결과적으로 한글이 들어간 파일을 만들고 github.io에 업로드하면 거기선 아무 문제없이 실행된다...

# local에서의 해결법
만약 로컬에서도 한글이름을 가진 포스팅을 보고 싶다면 window의 로컬 encoding을 변경하면 된다. 변경 법은 다음과 같다.
1. 제어판
2.국가 또는 지 설정
3.  관리자 옵션
4. 시스템 로캘 변경
5. Beta 세계언어 지원을 위해 Unicode UTF-8 사용 체크

![](/assets/images/jekyll-posts-hangul-set.PNG)

이후 재부팅하면 된다.
