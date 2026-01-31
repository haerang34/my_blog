---
title: "n8n - 이벤트 기반 자동화 도구"
date: 2026-01-31
lastmod: 2026-01-31
description: "n8n 설명"
slug: "n8n"
draft: false
---

# n8n - 이벤트 기반 자동화 도구

* * *

### 1\. n8n이란?

- 이벤트 기반 자동화 도구
- 다양한 앱·서비스를 노드(Node) 로 연결
- 조건 분기, 반복, 코드 실행까지 가능
- 오픈소스 (Self-host 가능)

<br>

### **2\. 활용 예시**

1. 업무 자동화

- 이메일 수신 → 첨부파일 저장 → Slack 알림
- Google Sheets 업데이트 → 보고서 생성 → 메일 발송
- 서버 로그 발생 → 필터링 → 장애 알림  

2. API 오케스트레이션

- 여러 REST API 호출
- 인증 토큰 처리
- 응답 파싱 후 다음 API에 전달

  

3. 데이터 처리 파이프라인

- 크롤링
- 데이터 정제
- DB 저장 (MySQL, PostgreSQL, MongoDB 등)

  

4. AI 연계 자동화

- OpenAI / LLM 호출
- 텍스트 요약, 분류, 번역 자동화
- 챗봇 백엔드 워크플로우

<br>

### 3\. 핵심 개념

1. Node

- 하나의 작업 단위
- 예: HTTP Request, IF, Function, Webhook, Slack

<br>

2. Workflow

- 노드들을 연결한 전체 자동화 시나리오

<br>

3. Trigger

- 워크플로우를 시작시키는 조건
- Webhook, Cron, 이메일 수신, 앱 이벤트 등

<br>

4. Execution

- 워크플로우가 실제로 한 번 실행된 기록

### 4\. n8n의 강점

1. 개발자 친화적

- JavaScript 코드 직접 작성 가능 (Function / Code 노드)
- JSON, HTTP, 인증 흐름을 그대로 다룸

<br>

2. Self-host 가능

- 데이터 외부 유출 없이 내부 서버 운영 가능
- 보안·비용 통제에 유리

<br>

3. 자유도 높음

- Zapier보다 **조건/반복/커스텀 로직**이 강력
- 복잡한 워크플로우 구성 가능

<br>

4. 비용 효율

- 자가호스팅 시 실행 횟수 제한 없음
- SaaS 대비 비용 절감

<br>