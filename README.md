# 이경근

백엔드 개발자

[기술 블로그](https://velog.io/@lgg007/posts) · [알고리즘 풀이](https://github.com/whiskend/Algorithm)

## 프로젝트

### [SketchCatch](https://github.com/NearthYou/SketchCatch)

AWS 인프라를 다이어그램으로 설계하고 배포하는 서비스. 5인 팀에서 GitHub 저장소 분석과 기존 AWS 자원 조회 기능을 담당했습니다.

TypeScript · Node.js · AWS · Zod

- GitHub 저장소 분석을 구현하면서 파일 목록과 내용을 동일한 commit SHA 기준으로 조회하도록 했습니다. 분석 도중 코드가 변경되어 서로 다른 버전의 파일을 읽는 문제를 방지했습니다. [PR #317](https://github.com/NearthYou/SketchCatch/pull/317)
- AWS 조회 결과에서 자원이 없는 경우와 권한 부족으로 조회하지 못한 경우를 구분했습니다. 일부 조회가 실패해도 수집한 결과는 유지하고 실패 정보를 별도로 전달했습니다. [PR #169](https://github.com/NearthYou/SketchCatch/pull/169)
- 미리보기에서 생성한 메타데이터를 저장 API가 허용하지 않아 저장이 실패하는 문제를 수정했습니다. Zod 스키마를 보완하고 저장 API 회귀 테스트를 추가했습니다. [PR #573](https://github.com/NearthYou/SketchCatch/pull/573)

### [AI Workout Board](https://github.com/whiskend/ai-workout-board)

이전 운동 기록을 조회해 현재 기록과 비교하고 다음 목표를 제안하는 개인 프로젝트입니다.

TypeScript · NestJS · PostgreSQL · Python · FastAPI

- 작성자 본인의 기록만 분석하도록 권한을 확인하고 같은 사용자의 같은 운동에 대한 과거 기록을 조회했습니다. 응답에는 비교에 사용한 기록과 분석 근거를 포함했습니다. [PR #21](https://github.com/whiskend/ai-workout-board/pull/21)
- `bench`, `벤치` 등 운동명 표기를 정규화해 이전 기록 검색에 적용했습니다. [PR #22](https://github.com/whiskend/ai-workout-board/pull/22)
- OpenAI 호출이 실패하면 규칙 기반 분석으로 전환하고 응답에 분석 모드를 표시했습니다. [PR #21](https://github.com/whiskend/ai-workout-board/pull/21)

## 시스템·모델 구현

### [Pintos](https://github.com/whiskend/pintos_302_G1)

C 기반 교육용 운영체제 팀 프로젝트입니다.

- 프로세스 종료 시 원본 FD 목록을 순회하며 파일을 닫도록 수정했습니다. [커밋](https://github.com/SISUinSea/Jungle-pintos_22-04_lab/commit/57649ebbdfa36f9fff63f305a55d5a364799c329)
- 페이지 할당 실패 시 앞서 확보한 자원을 정리하도록 보완했습니다. mmap의 입력 검증과 페이지별 지연 로딩 정보 생성을 구현했습니다. [실패 처리](https://github.com/whiskend/pintos_302_G1/pull/87) · [mmap](https://github.com/whiskend/pintos_302_G1/pull/98)

### [Mini GPT Lab](https://github.com/cloud-9-git/gpt-lab)

Python·PyTorch로 BPE 토크나이저와 Transformer 기반 GPT 모델을 공동 구현한 학습 프로젝트입니다. 특정 모듈을 나누어 단독 구현한 것이 아니라 팀원들과 함께 코드를 작성하고 검토했습니다. [토크나이저](https://github.com/cloud-9-git/gpt-lab/pull/1) · [모델](https://github.com/cloud-9-git/gpt-lab/pull/4)

## 설계 문서

- [GitHub 저장소 분석 범위와 대안 검토](https://github.com/NearthYou/SketchCatch/blob/main/docs/adr/0004-gg-repository-analysis-evidence-boundary.md): 저장소 코드를 실행하는 방식과 정적 분석을 비교하고 보안·비용·재현성을 고려해 분석 범위를 정리했습니다.
