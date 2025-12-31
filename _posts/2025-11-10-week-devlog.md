---
title: "DevLog 2025-11-10"
date: 2025-11-10
categories: [CodeBrainer]
tags: [TIL, DevLog, 주간요약]
permalink: /posts/codebrainer-week-2025-11-10/
---

## AI 코드 리뷰 고도화와 Gemini API 연동 삽질기 (2025년 11월 10일 주간 개발 로그)

이번 주는 AI 코드 리뷰 기능 고도화와 Google의 Gemini API 연동에 집중했습니다. 특히 Supabase와의 연동 과정에서 생각보다 많은 시간을 쏟았네요. 쉽지 않았지만, 그만큼 얻어가는 것도 많은 한 주였습니다.

**요약:**

*   AI 코드 리뷰 기능에 문제 ID 기반 검색 기능 추가 및 AI 성능 개선
*   Gemini API를 활용한 AI 코드 리뷰 기능 통합 및 Supabase 연동
*   Supabase 배포를 위한 프론트엔드 업데이트 및 API 문서 업데이트

**주요 작업:**

*   **✨ 새로운 기능: 문제 ID 기반 검색 엔드포인트 추가 및 AI 코드 리뷰 기능 개선**
    *   `feat: Add problem ID-based lookup endpoint and enhance AI code review` 커밋에서 확인할 수 있듯이, 이제 특정 문제 ID를 사용하여 코드 리뷰를 요청할 수 있습니다. 이를 통해 사용자가 원하는 코드에 대해 보다 빠르고 정확하게 리뷰를 받을 수 있도록 했습니다. 또한, AI 코드 리뷰의 전반적인 성능을 개선하기 위해 몇 가지 추가적인 최적화를 진행했습니다.
*   **✨ 새로운 기능: Gemini AI 코드 리뷰 통합 및 Supabase 연동**
    *   `feat: Gemini AI code review integration with Supabase` 커밋들을 통해 Gemini API를 활용한 AI 코드 리뷰 기능을 통합했습니다. 이 과정에서 Supabase와의 연동이 핵심적인 부분이었습니다. Supabase를 사용하여 코드 리뷰 결과를 저장하고 관리하며, 사용자 인증 및 권한 관리에도 활용했습니다. (두 번 커밋된 것을 보면... 삽질의 흔적이 느껴지는군요 😅)
*   **📝 문서화: API 문서 업데이트**
    *   `docs: Update BACKEND_API_DOCS.md with correct API specifications` 커밋에서 확인할 수 있듯이, 변경된 API 스펙에 맞춰 `BACKEND_API_DOCS.md` 파일을 업데이트했습니다. 꼼꼼한 문서화는 협업의 기본이죠!
*   **🔩 기타 작업: Supabase 배포를 위한 프론트엔드 업데이트**
    *   `chore: Update frontend for Supabase deployment` 커밋에서는 Supabase 배포를 위한 프론트엔드 설정을 업데이트했습니다. 특히, 환경 변수 설정 및 API 엔드포인트 주소 변경에 집중했습니다.

**기술적 도전:**

*   **Supabase와의 연동**: Gemini API와 Supabase를 효율적으로 연동하는 것이 가장 큰 과제였습니다. 특히, 데이터베이스 스키마 설계, API 엔드포인트 구현, 그리고 사용자 인증 및 권한 관리를 통합하는 과정에서 다양한 문제에 직면했습니다. 예를 들어, Supabase의 Row Level Security (RLS)를 이용하여 특정 사용자만 특정 코드 리뷰 결과에 접근할 수 있도록 설정하는 데 많은 시간을 할애했습니다.
*   **Gemini API 사용량 관리**: Gemini API의 사용량 제한을 효율적으로 관리하는 것도 중요한 고려 사항이었습니다. 코드 리뷰 요청 빈도를 제한하고, 캐싱 전략을 도입하여 API 호출 수를 최소화하려고 노력했습니다.

**다음 계획:**

*   Gemini API를 활용한 코드 리뷰 기능의 성능 및 정확도 향상
*   사용자 인터페이스 개선을 통해 코드 리뷰 요청 및 결과 확인 과정 간소화
*   새로운 프로그래밍 언어 및 프레임워크에 대한 지원 추가
*   더욱 상세한 코드 리뷰 보고서 제공 (예: 보안 취약점, 성능 개선 제안 등)

이번 주에는 AI 코드 리뷰 기능 고도화에 많은 노력을 기울였습니다. Gemini API 연동은 생각보다 어려웠지만, 앞으로 더 많은 기능들을 추가하고 개선해나가면서 개발자들의 생산성을 높이는 데 기여할 수 있도록 노력하겠습니다. 다음 주에는 코드 리뷰 결과 분석 및 시각화 기능을 추가하는 것을 목표로 하고 있습니다. 기대해주세요! 😉
