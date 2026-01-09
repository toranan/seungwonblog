---
title: "LoRa 학습 설정: training_config.toml 분석"
date: 2026-01-05 11:00:00 +0900
categories: [Stable Diffusion, Tech]
tags: [LoRa, Config, TOML]
---

# 학습 파라미터 최적화

성공적인 LoRa 학습을 위해 `training_config.toml` 파일을 구성했습니다. 이 설정 파일은 `accelerate` 라이브러리와 `sd-scripts`가 학습을 어떻게 수행할지 정의합니다.

## 주요 설정 분석

```toml
[general]
resolution = 512
caption_extension = ".txt"
enable_bucket = true

[network]
network_module = "networks.lora"
network_dim = 32
network_alpha = 16

[optimizer]
learning_rate = 0.0001
text_encoder_lr = 5e-5
unet_lr = 0.0001
optimizer_type = "AdamW8bit"
```

### 핵심 포인트
1. **Network Dim (Rank)**: `32`로 설정했습니다. 너무 높으면 과적합(Overfitting)될 수 있고, 너무 낮으면 특징을 다 담지 못합니다.
2. **Optimizer**: `AdamW8bit`를 사용하여 메모리 효율을 높였습니다.
3. **Learning Rate**: `1e-4`로 시작하여 안정적인 수렴을 유도했습니다.

## 실행 스크립트 (PowerShell)
윈도우 환경에서 학습을 쉽게 돌리기 위해 `train_local.ps1` 스크립트를 작성하여 자동화했습니다. 이 스크립트는 설정 파일을 로드하고 `sd-scripts`의 `train_network.py`를 실행합니다.
