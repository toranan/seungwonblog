---
title: "LoRa 학습을 위한 데이터셋 전처리 가이드"
date: 2026-01-03 14:30:00 +0900
categories: [Stable Diffusion, Tutorial]
tags: [LoRa, Dataset, Preprocessing]
---

# 데이터셋이 품질을 결정한다

LoRa 학습에서 가장 중요한 것은 **양질의 데이터셋**입니다. 이번 글에서는 KUIKI 캐릭터 학습을 위해 데이터를 어떻게 준비하고 전처리했는지 공유합니다.

## 데이터 디렉토리 구조
데이터셋은 다음과 같은 구조로 정리했습니다.
```
dataset/
├── processed/
│   └── 10_kuiki/
│       ├── image_01.png
│       ├── image_01.txt
│       └── ...
└── unused/
```

- **processed**: 학습에 실제로 사용될 이미지가 들어갑니다. `10_kuiki`는 `반복횟수_트리거워드` 형식을 따릅니다.
- **unused**: 품질이 낮거나 중복되는 이미지는 이곳으로 분류하여 학습에서 제외했습니다.

## 캡션 작업 (Captioning)
이미지마다 `.txt` 파일을 생성하여 해당 이미지를 묘사하는 태그를 작성했습니다.
예시: `1girl, kuiki, solo, blue eyes, white hair, smiling, upper body`

이 태그들은 AI가 이미지를 이해하는 데 도움을 주며, 학습 시 특정 프롬프트에 반응하도록 만듭니다. 우리는 `lilpa_avatar` 등의 기존 태그와의 충돌을 피하기 위해 고유 트리거 워드를 신중히 선정했습니다.
