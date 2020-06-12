---
title: JEKYLL-ADMIN 설치 및 오류 수정
toc: true
tags:
- jekyll
- minimal-mistakes
---

# jekyll-admin 설치
JEKYLL를 설치하고 포스팅을 할려는데 그냥 마크다운으로 포스팅을 하기에는 힘들어서 쉽게 포스팅을 할 수 있는 방법을 찾아보았다.   
그 중 jekyll-admin을 설치하면 쉽게 포스팅을 할 수 있다는 것을 알게 되어 공유한다.

### 1.Gemfile에 다음을 추가하자
```
gem 'jekyll-admin', group: :jekyll_plugins
```
### 2. 그 다음엔 다음 명령어를 치면 된다.
```
bundle
jekyll serve
```

### 3. 적용확인
적용을 확인해보자 [http://localhost:4000/admin](http://localhost:4000/admin)

![](/assets/images/jekyll-admin.PNG)

# jekyll-admin 빈화면 오류
설치후 접속해보았는데 그냥 덜렁 빈화면만 나왔다 한국어 자료는 암만 찾아봐도 없어서 영어로 뒤져보다가  
관련 문제가 [jekyll issue#595](https://github.com/jekyll/jekyll-admin/issues/595)에 등록 된걸 찾아볼 수가 있었다.

알고보니 이번에 버전업을 하면서 생긴 버그였다.  수정 방법은 다음과 같다.

### 1. _config.yml 에 다음을 추가하자

```
ignore_theme_config: true
```
### 2. bundle 업데이터
```
bundle
jekyll serve
```

### 3. 적용확인
적용을 확인해보자 [http://localhost:4000/admin](http://localhost:4000/admin)
