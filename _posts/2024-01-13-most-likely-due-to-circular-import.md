---
layout: single
title: "[Import Error] most likely due to a circular import"
categories: ES
---

# Problem
특정 라이브러리가 올바르게 동작하지 않았다.

다음은 torch를 import하여 사용하였을 때 발생했던 에러메세지다.

```console
AttributeError: partially initialized module 'torch' has no attribute 'tensor' (most likely due to a circular import)

AttributeError: partially initialized module 'torch' has no attribute '__version__' (most likely due to a circular import)
```

# Solution
파일명이 내가 import한 라이브러리와 이름이 같았다; ㅎ

torch.py에서 torch를 import하고 있었는데, 파일명을 다른 이름으로 고치니 해결되었다.
