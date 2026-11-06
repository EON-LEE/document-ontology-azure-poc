# Azure Ontology Lab

Azure/Microsoft에서 비정형 문서를 온톨로지와 지식 그래프로 연결하고, 네 가지 RAG 구성의 품질과 운영성을 비교하기 위한 실험 저장소입니다.

**현재 상태:** 개발·방법론·검증 계획을 작성한 단계입니다. 계약과 금융 PDF를 초기 범위에 포함하되, 데이터 버전·표본·이용 조건은 확인 전입니다. 구현, Azure 배포, 성능 측정은 아직 완료하지 않았습니다.

프로젝트명은 **Azure Ontology Lab: From Documents to Enterprise Knowledge**, 사용자 확정 저장소명은 `azure-ontology-lab`입니다. 원격 이름 변경은 현재 GitHub 인증의 관리 작업 권한 부족(HTTP 403)으로 차단되어, 실제 저장소명은 아직 `document-ontology-azure-poc`입니다. Microsoft 공식 제품이나 공식 가이드가 아닌 팀의 독립적인 실험입니다.

| 문서 | 내용 |
|---|---|
| [개발 계획](docs/development-plan.md) | 사용자 확정 범위, 검토 대기 사항, 개발 단계·의존 관계·완료 조건 |
| [방법론과 실행 계획](docs/methodology.md) | 개념, 문서 기반 온톨로지 생성, 데이터 선정, 실험, 평가, 운영 검증, 보고서 구성 |
| [다중 모델 비평과 반영 결과](docs/methodology-review.md) | GPT·Claude·Gemini·Grok 5개 모델의 독립 검토, 상호 반박, 보완 결정과 미검증 사항 |

확정된 구현 대상은 네이티브 RAG, Fabric 기반 Graph RAG, HorizonDB 기반 Graph RAG, Microsoft GraphRAG입니다. 대상에 포함됐다는 것이 현재 구독에서 배포 가능하거나 운영 적합성이 검증됐다는 뜻은 아닙니다.

## Development workflow

- Create changes on a feature branch and open a ready-for-review pull request.
- Use the existing repository-scoped Git credentials for fetch and push.
- Keep GitHub CLI credentials process-scoped for repository write operations; do not change shared or global authentication.
- Merge into `main` with a normal, non-force merge after required checks pass.