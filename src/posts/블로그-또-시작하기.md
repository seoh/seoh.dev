---
layout: layouts/post.njk
title: 블로그 또 시작하기
date: 2019-09-23T02:02:02.493Z
tags:
  - blog
  - twis
---
단순히 '알고 있다'라고 본인이 생각하는 것과 알고 있는 것을 정리하는 것은 다른 일이고 그걸 공개하는 것은 또 다른 일이다. 공개를 위해 정리하면서 얻는 것들을 알고 있어서 계속 시도는 하지만 귀찮음과 핑계로 계속 썼다 말았다 올렸다내렸다 했고, 바로 직전의 블로그는 노트북을 바꾼 뒤에 간만에 다시 쓰려고 세팅하니 제대로 안돌아가길래 보니까 메이저 업데이트도 아닌데 호환불가능한 변화로 깨지길래 그냥 내렸다. 이런저런 경험으로 새로 블로그를 하면 이렇게 해야지 싶었던 생각들이 있었고 이번엔 최대한 지켜서 덜 귀찮고 오래 쓰는 환경을 만들고 싶었다. 그런 의미에서

1. 소스 수정은 하지 말자. 최대한은 테마/템플릿까지만
2. 모바일에서 포스팅 가능한 환경 구축

프레임워크는 일단 둘째치고 이런 기준으로 환경을 고민했을 때 당시엔 [GitLab의 CI Pipeline][GitLab]은 커밋 기준으로 배포도 가능하고 레시피도 많지만 git push/pull도 느리고 파일이 많아지면 더 느려지기도하고 정적페이지인데도 느려서 계속 고민만 하다가 [GitHub Actions][GitHub]가 열렸길래 고민하다 익숙하지 않은 환경이라 문서 읽으면서 차일피일 미뤘고 그러다 [Netlify CMS][Netlify]를 알게 됐는데 괜찮아보였다. 일단 Netlify에 대한 글을 많이 읽어서 한번 써보고 싶었고, 정적페이지에서도 관리페이지를 붙일 수 있는데 GitHub 계정과 연결해서 자동으로 커밋을 해준다. 그래서 이걸 어떻게 붙이지 고민하던중에 블로그 플랫폼은 뭘 쓸까 고민하다 Gatsby 많이 쓰니 한번 써보고 싶어서 써볼까 잠정적 확정이었는데, 요새 종종 보는 [Every Layout](https://every-layout.dev/)의 저자 중 하나인 [Andy Bell](https://twitter.com/hankchizljaw)이 [Eleventy][11ty](이하 11ty) 기반의 [Hylia][Hylia]라는 블로그 플랫폼을 만들었다길래 봤더니 Netlify CMS를 쓰길래 이거다싶었다. 11ty는 예전에 페이스북이 만든 라이브러리의 대체 라이브러리들 소개인 [NPM Uninstall Facebook][alt-facebook]에서 Gatsby 대체로 나와있던게 생각나서 바로 결정했다.

아직 0.5라 변경이 많이 될꺼같고 블로그, 테마, 메타데이터가 한곳에 섞여있어서 나중에 테마 설정이 생기면 변경하느라 고생할 것 같은 느낌이라 위에서 말한 조건에는 맞지 않지만 11ty 기반으로 뭔가 만져보고 싶다는 생각이 들어서 그냥 이걸로 결정했다. 단점보다는 Netlify CMS 연동이 마음에 들고 더 미루다간 아무것도 못할 것 같다는 생각에 다음에 또 옮기더라도 일단 다시 시작해보려고 한다.

블로그를 만들면 가장 큰 고민 두가지가 뭘로 만들지와 뭘 쓰지인데 일단 큰 하나는 해결했고 정기적으로 쓸 글이 있었으면 좋겠다고 생각했는데 TIL(Today I Learned)를 쓰려다가 매일 뭘 배울 정도로 부지런하지 않은데 트위터에 관심있는 링크는 매일 남기니 이걸 차라리 정기적으로 공개하는게 좋겠다고 생각해서 TWIS(This Week I've Seen) 정도로 이름 붙여서 매주 정리를 해보려고 한다. 물론 얼마나 갈 지는 모르겠지만.



[GitLab]: https://docs.gitlab.com/ee/ci/yaml
[GitHub]: https://github.com/features/actions
[Netlify]: https://www.netlifycms.org/

[11ty]: https://www.11ty.io/
[Hylia]: https://hylia.website/
[alt-facebook]: https://npm-uninstall-facebook.com/
