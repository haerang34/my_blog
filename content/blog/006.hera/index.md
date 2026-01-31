---
title: "Argo workflow를 Python 코드로 - Hera"
date: 2025-11-05
lastmod: 2025-11-05
description: "Argo workflow를 Python 코드로 작업하는 방법"
slug: "Hera"
draft: false
---

# Hera
### [Python Hera Site](https://hera.readthedocs.io/en/latest/#what-is-hera)

## Hera 란?
> Hera는 Argo Workflows를 간편하고 직관적으로 만들어 주는 Python SDK.  
> Python 함수를 Kubernetes에서 실행되는 컨테이너화된 템플릿으로 쉽게 변환가능하며,
> Kubernetes의 모든 기능을 활용할 수 있음.

## Hera 설치
```
$ pip install hera
```

## YAML vs Hera 비교 예시

### YAML로 작성 시
```yaml
apiVersion: argoproj.io/v1alpha1
kind: Workflow
metadata:
  generateName: example-
spec:
  entrypoint: main
  templates:
  - name: main
    steps:
      - - name: echo
          template: echo-template
  - name: echo-template
    container:
      image: alpine:latest
      command: [echo]
      args: ["Hello, World!"]
```

### Hera로 작성 시
```python
from hera.workflows import Workflow, Task, script

@script()
def echo():
    print("Hello, World!")

with Workflow("example") as w:
    t = Task("echo", echo)

w.create()
```

## 사용하면서 느낀 장단점
### 1. YAML에 비해 구조적 이점
  - 프로그래밍적 유연성
  - 변수 설정으로 반복 사용성 증가
  - 공통 함수, 모듈화, 상속 등을 활용 가능
  - 대규모 워크플로우를 코드로 관리하기 용이
  
### 2. Argo 공식 문서와의 직접 대응이 비교적 어려움
  - 대부분 문서는 YAML 기반
  - 실제 응용하면서 사용하기엔 한계점이 있음
  - Argo Workflow 내에서 WOW(workflow of workflow) Create 방식을 사용하려면 Hera로는 구현이 어려움

### 3. 가장 좋았던것은 YAML에 비해 가독성 측면에서 큰 이점이 있었음