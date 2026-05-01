# Motivation ≠ Novelty

**명작 논문에서 배우는 novelty 확보 — 신입생을 위한 case-based 가이드**

> APRL · Autonomous Perception and Robot Learning · DGIST

🔗 **Live:** [gisbi-kim.github.io/motivation-is-not-novelty](https://gisbi-kim.github.io/motivation-is-not-novelty/)

---

## 한 줄 요약

"기존이 X를 못한다 → 우리가 모듈을 붙였다"는 **motivation이지 novelty가 아니다.**  
Top-tier 논문은 항상 **"왜 그 모듈이 그 형태여야 하는가"** 에 원리적으로 답한다.

---

## 무엇을 배울 수 있나

ResNet · Transformer · NeRF 세 명작을 해부하여,  
각 논문이 motivation에서 novelty로 어떻게 도약했는지 단계별로 분석한다.

| 논문 | Motivation (관찰) | Novelty (해법의 원리) |
|------|-------------------|----------------------|
| **ResNet** (CVPR 2016 Best) | Plain network를 깊게 쌓으면 training error가 오히려 증가 | Identity mapping이 학습하기 어렵다 → residual reparameterization으로 identity를 default로 |
| **Transformer** (NeurIPS 2017) | RNN은 sequential → 병렬화 불가 + long-range path O(n) | Recurrence 제거 시 path length O(1) → positional encoding + multi-head로 보완 |
| **NeRF** (ECCV 2020 Best) | Voxel/Mesh 한계 → MLP로 continuous scene 표현 시도했으나 detail 손실 | MLP의 spectral bias → 입력 frequency lifting(positional encoding)으로 극복 |

---

## 구성

- **Motivation vs Novelty 신호 비교** — 어느 단계에서 멈춰있는지 진단
- **Case 1. ResNet** — degradation의 원인 진단과 skip connection의 필연성
- **Case 2. Transformer** — recurrence 제거라는 단일 선택이 모든 component를 강제하는 방식
- **Case 3. NeRF** — spectral bias 진단이 positional encoding 형태를 도출하는 과정
- **Top-tier vs 2티어 비교표** — 6단계(motivation → failure analysis)로 패턴 대조
- **8문항 자가진단 체크리스트** — 제출/미팅 전 점검용
- **위험 신호 표현 목록** — 미팅에서 피해야 할 12가지 표현
- **한 문장 자가검증** — 명작의 한 줄 insight처럼 내 논문을 요약할 수 있는가

---

## 대상

- APRL Lab 신입 대학원생
- Top-tier 논문과 incremental 논문의 차이를 감각적으로 익히고 싶은 연구자
- 리뷰어의 "그래서 뭐가 새로운가?" 질문에 30초 안에 답하고 싶은 모든 이

---

## 사용

별도 빌드 없이 브라우저에서 바로 열 수 있는 단일 HTML 파일.

```bash
git clone https://github.com/gisbi-kim/motivation-is-not-novelty.git
open motivation-is-not-novelty/index.html
```

또는 위 [Live 링크](https://gisbi-kim.github.io/motivation-is-not-novelty/)에서 바로 확인.

---

<div align="right">
  <em>"Motivation은 문제를, Novelty는 해법의 필연성을 정의한다."</em>
</div>
