<p>
  <img src="./assets/header.svg" width="100%" alt="이경근 · Backend Developer — Cloud &amp; AI" />
</p>

요청이 들어와 저장되고 응답으로 돌아가는 흐름을 살피는 백엔드 개발자 이경근입니다.<br>
AWS·GitHub·LLM의 응답을 서비스에 연결하며, 권한 오류와 빈 결과를 구분하고 데이터 형식을 맞추는 일을 해왔습니다.

[Blog](https://velog.io/@lgg007/posts) · [Algorithm](https://github.com/whiskend/Algorithm)

## Projects

### [AI Workout Board](https://github.com/whiskend/ai-workout-board)

**개인 프로젝트 · 운동 기록과 이전 기록을 비교하는 AI 보조 서비스**<br>
`TypeScript` `NestJS` `PostgreSQL` `Python` `FastAPI`

- JWT 인증·작성자 권한 확인과 이전 기록 조회를 백엔드에서 처리했습니다.
- 운동명을 정규화해 같은 운동의 기록을 비교하고, LLM 분석 호출이 실패하면 규칙 기반 결과를 반환하도록 했습니다.

[기록 비교와 fallback](https://github.com/whiskend/ai-workout-board/pull/21) · [운동명 정규화와 분석 흐름](https://github.com/whiskend/ai-workout-board/pull/22)

### [SketchCatch](https://github.com/NearthYou/SketchCatch)

**5인 팀 프로젝트 · 클라우드 인프라 설계·배포 플랫폼**<br>
`TypeScript` `Node.js` `AWS` `Zod`

- AWS 조회·GitHub 저장소 분석을 담당했습니다. 권한 때문에 읽지 못한 자원을 빈 결과와 구분하고, 중복 자원을 정규화했습니다.
- 미리보기에는 보이지만 저장되지 않던 문제를 추적해, 미리보기 데이터와 저장 API 스키마의 불일치를 수정했습니다.

[저장소 분석](https://github.com/NearthYou/SketchCatch/pull/317) · [AWS 조회](https://github.com/NearthYou/SketchCatch/pull/169) · [저장 오류 수정](https://github.com/NearthYou/SketchCatch/pull/573)

### [Pintos](https://github.com/whiskend/pintos_302_G1)

**팀 프로젝트 · C로 구현하며 배운 운영체제**<br>
`C` `Virtual Memory` `Synchronization`

- 프로세스 종료 시 복사된 리스트 헤더를 순회하던 코드를 수정해, 실제 FD 리스트에서 자원을 정리하도록 했습니다.
- 가상 메모리의 page claim 실패 경로를 정리하고, mmap 진입부 검증과 페이지별 지연 로딩 정보 구현에 기여했습니다.

[FD 정리 수정](https://github.com/SISUinSea/Jungle-pintos_22-04_lab/commit/57649ebbdfa36f9fff63f305a55d5a364799c329) · [claim 실패 처리](https://github.com/whiskend/pintos_302_G1/pull/87) · [mmap 구현 기여](https://github.com/whiskend/pintos_302_G1/pull/98)

### [Mini GPT Lab](https://github.com/cloud-9-git/gpt-lab)

**팀 학습 프로젝트 · 한 화면에서 함께 구현하고 검토한 작은 GPT**<br>
`Python` `PyTorch` `Byte-level BPE` `Transformer`

- 토크나이저, GPT 모델, 학습·평가 흐름을 공동 구현·검토했습니다.
- 학습 수치와 실제 출력, 실험 조건을 함께 확인하며 사전 학습 모델과 무작위 초기화 모델의 비교 결과를 기록했습니다.

[토크나이저 공동 작업](https://github.com/cloud-9-git/gpt-lab/pull/1) · [모델 공동 작업](https://github.com/cloud-9-git/gpt-lab/pull/4)

## Working Notes

- 전체 요청 흐름을 먼저 그린 뒤, 중요한 부분을 깊게 살펴봅니다.
- 외부 응답은 서비스에서 쓸 데이터로 변환하고 검증합니다.
- 기능이 화면에 보이는 데서 끝내지 않고, 적용·저장까지 이어지는지 확인합니다.

배운 내용은 [블로그](https://velog.io/@lgg007/posts)에, 알고리즘 풀이는 [저장소](https://github.com/whiskend/Algorithm)에 남깁니다.
