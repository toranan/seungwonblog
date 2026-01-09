---
title: "LoRa 프로젝트 시작: 나만의 KUIKI 만들기"
date: 2026-01-02 10:00:00 +0900
categories: [Stable Diffusion, Project]
tags: [LoRa, AI, Setup]
---

# LoRa 프로젝트를 시작하며

Stable Diffusion을 사용하여 나만의 캐릭터 **KUIKI**를 일관성 있게 생성하기 위한 LoRa(Low-Rank Adaptation) 학습 프로젝트를 시작했습니다.

이 프로젝트의 목표는 단순히 이미지를 생성하는 것을 넘어, 캐릭터의 고유한 특징(얼굴, 표정, 스타일)을 학습시켜 다양한 상황에서도 캐릭터가 유지되도록 하는 것입니다.

## 프로젝트 목표
1. **고품질 데이터셋 구축**: 캐릭터의 다양한 각도와 표정을 담은 데이터 수집.
2. **LoRa 학습**: `sd-scripts`를 활용한 효율적인 모델 학습.
3. **WebUI 통합**: Automatic1111 WebUI에서 쉽게 사용할 수 있도록 적용.

## 준비물
- Python 3.10
- NVIDIA GPU (CUDA 지원)
- Git
- `sd-scripts` 리포지토리

앞으로의 포스팅을 통해 데이터 처리부터 학습, 그리고 최종 이미지 생성까지의 과정을 기록할 예정입니다.
