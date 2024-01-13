---
layout: single
title: "[wget Error] 다운로드 중 끊기는 현상: Connection reset by peer"
categories: ES
---

# [wget] 다운로드 중 끊기는 에러 해결 - Connection reset by peer

## Problem
---
`wget`을 이용해서 다운로드 하던 중 이유 없이 끊김

-image1

## Solution
---
```
# Error 유발 command
# wget http://images.cocodataset.org/zips/train2017.zip

# 해당 error 해결 command 
wget --no-check-certificate https://images.cocodataset.org/zips/train2017.zip
```
