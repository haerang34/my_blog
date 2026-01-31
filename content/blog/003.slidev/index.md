---
title: "Slidev 소개"
date: 2025-09-22
lastmod: 2025-09-22
description: "프레젠테이션 라이브러리 Slidev에 대한 소개 및 에제 사용"
slug: "slidev"
draft: false
---

> 파워포인트 대신 쓸 수 있는 개발자용 파워포인트가 있을까?


~~찾아보니 있다~~

## Slidev란?
- 프레젠테이션 슬라이드를 개발자가 사용하기 편한 Markdown 문법을 통해 작성 가능한 라이브러리
- Markdown 외 프론트엔드 라이브러리 사용도 가능한 것으로 보임.(Vue.js, UnoCSS)
- [Slidev 링크](https://sli.dev/)

### 설치
- 설치는 간단한 편
- node.js 및 npm이 우선 설치되있어야 함
```bash
# If you haven't installed pnpm
npm i -g pnpm

pnpm create slidev
```

### 사용법
```markdown
    <!-- Page 1 -->
    # Title
    Hello, **Slidev**!

    <!-- ---로 페이지 나눔 -->
    ---

    <!-- Page 2 -->
    # Slide 2
    Use code blocks for highlighting:

    ```ts
    console.log('Hello, World!')
    ```
    ---
```

### 실행
![slidev1](./slidev1.png)
![slidev2](./slidev2.png)

- 더 사용하면서 사용법 추가 예정