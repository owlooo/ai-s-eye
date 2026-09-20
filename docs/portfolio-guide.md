# 실행·설계 문서 안내

[개인 기여 요약](../README.md)

## 실행 환경

- [미니PC 개발 환경](minipc-runbook.md): Docker Compose, 공용 API·DB 운영 절차.
- [GCP 배포 환경](gcp-runbook.md): Compute Engine, 환경변수, 마이그레이션, 서비스 점검·백업.
- [개발 Compose](../docker-compose.yml) · [GCP Compose](../compose.gcp.yml)

GCP 구성은 CPU VM 기준입니다. GPU 추론 없이 저장된 Vision 결과를 재생할 수 있으며, 실제 추론 환경과 구분합니다.
환경변수와 외부 서비스 인증을 준비한 뒤 해당 실행 안내를 따릅니다. 저장소만 복제해 모든 기능이 즉시 실행되는 구성은 아닙니다.

## 코드 입구

| 영역 | 코드·문서 |
|---|---|
| 자동 배포 | [GitHub Actions](../.github/workflows) · [GCP 스크립트](../scripts/deploy-gcp.sh) |
| API·DB | [FastAPI](../services/api) · [API 계약](api-contract.md) |
| 화면 | [Dashboard](../apps/dashboard) |
| AI 분석 | [AICC](../services/aicc) |

## 기록과 해석

- 2026.08.12 GCP 자동 배포 성공은 프로젝트 수행 당시 기록입니다.
- README의 Agent 화면은 합성 주문 기반 시뮬레이션이며, 실제 고객 성과나 자동 인력 배치 실적이 아닙니다.
- 개인 포크는 코드·문서 열람용이며 GitHub Actions를 비활성화했습니다. 팀 운영 환경과 별개입니다.
- [정리 전 팀 README](https://github.com/aivle-b-t24/ai-s-eye/blob/553926c8658f2b4f4db232b23b30b78ee5260695/README.md)는 당시 개발 문서입니다. 초기 계획·상태 표현을 현재 완료 범위로 사용하지 않습니다.
