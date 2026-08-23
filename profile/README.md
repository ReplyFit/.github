# 리플핏 ReplyFit

> **반복 문의는 AI 초안으로, 최종 결정은 셀러가 직접.**

의류·잡화 온라인 셀러를 위한 문의 응대 자동화 B2B SaaS를 만듭니다.
문의·리뷰 CSV 하나로 ① 개인정보 마스킹 → ② 유형 자동분류 → ③ 정책 기반 AI 답변 초안 → ④ 셀러 승인·발송 → ⑤ 주간 VOC 리포트까지.

## 저장소

| 저장소 | 스택 | 설명 |
|---|---|---|
| [replyfit-backend](https://github.com/ReplyFit/replyfit-backend) | Java 21 · Spring Boot 3 · PostgreSQL · Redis · Kafka · OpenAI | REST API + AI 파이프라인 워커 |
| [replyfit-frontend](https://github.com/ReplyFit/replyfit-frontend) | Next.js 15 · TypeScript · Tailwind v4 | 랜딩 + 셀러 대시보드 |
| [replyfit-infra](https://github.com/ReplyFit/replyfit-infra) | Docker Compose · Kubernetes | 전체 스택 실행·배포 |

## 원칙

- **AI는 직접 발송하지 않습니다** — 셀러 승인 구조로 오답·개인정보·플랫폼 약관 리스크를 설계 단계에서 차단
- **등록된 정책 문구만 인용** — 정책 검증 로직(PolicyGuard)이 출처 없는 수치를 잡아냅니다
- **개인정보 최소 수집** — 업로드 즉시 마스킹, 보관기간 제한·자동 삭제

## 팀

최용주 (기획/풀스택) · 기승현 (기획/PM) · 권성호 (백엔드/고객검증) — 2026 SW중심대학 AI/SW 창업 프로젝트
