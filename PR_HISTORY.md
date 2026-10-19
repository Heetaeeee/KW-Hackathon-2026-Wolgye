# PR 기록 — 월계는 처음이라 (2026 광운대 KW해커톤 13조 NowonLikeUs)

원본 저장소 `2026-KW-HACKATHON/13_NowonLikeUs` 의 Pull Request 기록을 `gh pr list --json` 으로 받아 정리했습니다 (받은 날 2026-10-19). 시각은 한국 시간입니다.

## 요약

- 기간: 2026-09-25 ~ 2026-10-11
- PR 84개 — 머지 78 · 닫힘 6
- 흐름: `이름/작업` 브랜치 → `dev` PR → 팀원 리뷰 승인 + CI(lint · 타입 검사 · 테스트 · 빌드) 통과 → 머지 → `master` 릴리스

| 팀원 | 역할 | 올린 PR | 리뷰 승인 |
|---|---|---|---|
| 정우성(@wo0oo) | 프론트엔드 | 51 | 26 |
| 김권섭(@kwonseop) | AI | 18 | 24 |
| 우희태(@Heetaeeee) | 백엔드 · DB · 발표 | 12 | 19 |
| 박용민(@parkyongminn) | 조사 | 3 | 3 |

## 목록

| # | 제목 | 작성자 | 상태 | 머지 | 승인 |
|---|---|---|---|---|---|
| [#1](#pr-1) | Chore: 프로젝트 뼈대와 기획 문서 공개 | 정우성 | 머지 | 09-25 |  |
| [#2](#pr-2) | Chore: dev → master 배포 반영 (프로젝트 뼈대와 기획 문서) | 정우성 | 머지 | 09-25 |  |
| [#3](#pr-3) | Docs: 기본 브랜치를 dev 로 바꾼 것을 문서에 반영 | 정우성 | 머지 | 09-25 |  |
| [#4](#pr-4) | Merge: dev → master 배포 반영 (#2) | 정우성 | 머지 | 09-25 |  |
| [#5](#pr-5) | Docs: 김권섭 브랜치 로마자 표기 수정 | 정우성 | 머지 | 09-25 |  |
| [#6](#pr-6) | Feat: DB 마이그레이션, D-day 계산, 시드 스크립트 추가 | 우희태 | 머지 | 09-26 |  |
| [#7](#pr-7) | Feat: 공용 타입 계약 추가 | 정우성 | 머지 | 09-26 |  |
| [#8](#pr-8) | Feat: 상황 입력과 할 일 목록 화면 추가 | 정우성 | 머지 | 09-26 |  |
| [#9](#pr-9) | Feat: AI 근거 검증 로직 추가 | 김권섭 | 머지 | 09-26 | 정우성 |
| [#10](#pr-10) | Fix: UNKNOWN 판정 시 AI 답변 차단 | 김권섭 | 머지 | 09-27 | 정우성 |
| [#11](#pr-11) | Docs: 월계1동 생활정보 조사 결과 추가 | 박용민 | 머지 | 09-27 | 정우성 |
| [#12](#pr-12) | Feat: 프로필 매칭 로직과 할 일 조회 API 추가 | 우희태 | 머지 | 09-27 | 정우성 |
| [#13](#pr-13) | Kwonseop/search fallback | 김권섭 | 닫힘 |  |  |
| [#14](#pr-14) | Feat: 할 일 목록을 실제 API 로 연결 | 정우성 | 머지 | 10-01 | 김권섭 |
| [#15](#pr-15) | Feat: AI 장애 대비 키워드 폴백 검색 추가 | 김권섭 | 닫힘 |  |  |
| [#16](#pr-16) | Feat: AI 장애 대비 키워드 폴백 검색 추가 | 김권섭 | 머지 | 10-01 | 정우성 |
| [#17](#pr-17) | Feat: 할 일 상세 화면 추가 및 화면 디자인 재작업 | 정우성 | 머지 | 10-02 | 김권섭 |
| [#18](#pr-18) | Feat: 할 일 완료 체크와 진행률 추가 | 정우성 | 머지 | 10-02 | 김권섭 |
| [#19](#pr-19) | Chore: CI 워크플로 추가 | 정우성 | 머지 | 10-02 | 김권섭 |
| [#20](#pr-20) | Docs: 구현계획 진행 현황과 읽는 법 추가 | 정우성 | 머지 | 10-02 | 김권섭 |
| [#21](#pr-21) | Docs: 생활정보 추가 조사 결과 반영 | 박용민 | 머지 | 10-03 | 정우성 |
| [#22](#pr-22) | Feat: 조사 완료된 생활정보 시드 10건 추가 | 우희태 | 머지 | 10-06 | 정우성 |
| [#23](#pr-23) | Docs: 생활정보 직접 확인 결과 반영 | 박용민 | 닫힘 |  |  |
| [#24](#pr-24) | Fix: 조사와 문장부호로 인한 폴백 검색 누락 수정 | 김권섭 | 머지 | 10-03 | 정우성 |
| [#25](#pr-25) | Feat: Gemini 구조화 응답 호출 추가 | 김권섭 | 머지 | 10-03 | 정우성 |
| [#26](#pr-26) | Feat: 질문 API 연결 및 AI 안전장치 추가 | 김권섭 | 닫힘 |  |  |
| [#27](#pr-27) | Feat: 로그인·질문·답변·승격 공용 타입 초안 추가 | 정우성 | 머지 | 10-06 | 김권섭 |
| [#28](#pr-28) | Feat: 질문 화면과 신뢰도 배지 추가 | 정우성 | 머지 | 10-06 | 김권섭 |
| [#29](#pr-29) | Chore: 설치 시 Prisma 클라이언트 생성 스크립트 추가 | 정우성 | 머지 | 10-06 | 김권섭 |
| [#30](#pr-30) | Feat: 질문 API 연결 및 안전한 폴백 처리 추가 | 김권섭 | 머지 | 10-06 | 정우성 |
| [#31](#pr-31) | Fix: AI 생성 문장을 서버 고정 안내로 대체 | 김권섭 | 머지 | 10-06 | 정우성 |
| [#32](#pr-32) | Fix: Gemini 근거를 키워드 후보로 제한 | 김권섭 | 머지 | 10-06 | 정우성 |
| [#33](#pr-33) | Feat: 질문 시 상황 필터에 필요한 값 함께 전송 | 정우성 | 머지 | 10-06 | 김권섭 |
| [#34](#pr-34) | Feat: 질문 결과 정리와 다음 사람 돕기 안내 추가 | 정우성 | 머지 | 10-06 | 김권섭 |
| [#35](#pr-35) | Docs: 구현계획 진행 현황 갱신 (10/6 기준) | 정우성 | 머지 | 10-06 | 김권섭 |
| [#36](#pr-36) | Feat: 회원가입·로그인·로그아웃 API와 세션 가드 추가 | 우희태 | 머지 | 10-06 | 정우성 |
| [#37](#pr-37) | Feat: 질문 목록·주민 답변·맞아요 확인 API 추가 | 우희태 | 닫힘 |  |  |
| [#38](#pr-38) | Feat: 질문·답변·확인·승격 API (B-community) | 우희태 | 머지 | 10-06 | 정우성 |
| [#39](#pr-39) | Feat: 로그인·가입 화면 추가 | 정우성 | 머지 | 10-06 | 우희태 |
| [#40](#pr-40) | Fix: Gemini 응답에서 미사용 answer 제거 | 김권섭 | 머지 | 10-07 | 정우성 |
| [#41](#pr-41) | Feat: 질문 askerId 기록, 답변 authoredByMe, 질문자 닉네임 비공개 | 우희태 | 머지 | 10-07 | 정우성 |
| [#42](#pr-42) | Feat: 이웃의 질문 화면과 로그인 상태 표시 추가 | 정우성 | 머지 | 10-07 | 우희태 |
| [#43](#pr-43) | Feat: 운영자 승격 화면 추가 | 정우성 | 머지 | 10-07 | 우희태 |
| [#44](#pr-44) | Fix: 답변 저장은 배치 트랜잭션, 승격은 트랜잭션 시간 여유 | 우희태 | 머지 | 10-07 | 정우성 |
| [#45](#pr-45) | Style: 전화번호와 하단 링크 터치 영역을 44px로 | 정우성 | 머지 | 10-07 | 김권섭 |
| [#46](#pr-46) | Docs: 질문 로그인 · 승격 조건 · AI 역할을 구현에 맞게 정리 | 정우성 | 머지 | 10-07 | 김권섭 |
| [#47](#pr-47) | Chore: dev → master 배포 반영 (본선 — 질문 · 답변 · 승격 순환) | 정우성 | 머지 | 10-08 | 김권섭 |
| [#48](#pr-48) | Fix: 질문 검색 정확도와 AI 폴백 결과 개선 | 김권섭 | 머지 | 10-08 | 정우성 |
| [#49](#pr-49) | Feat: AI를 켜면 질문 화면에 외부 전송 안내 표시 | 정우성 | 머지 | 10-08 | 김권섭 |
| [#50](#pr-50) | Docs: 배포 직전 현황표 갱신 (#45 · #48 · #49) | 정우성 | 머지 | 10-08 | 김권섭 |
| [#51](#pr-51) | Feat: 서비스 소개 표지화면 추가 | 정우성 | 머지 | 10-08 | 우희태 |
| [#52](#pr-52) | Docs: 심사 · 외부 공개용으로 README 재작성 | 정우성 | 머지 | 10-08 | 우희태 |
| [#53](#pr-53) | Chore: dev → master 배포 반영 (표지 · README) | 정우성 | 머지 | 10-08 | 우희태 |
| [#54](#pr-54) | Docs: README에 오픈소스 · 출처 절 추가 | 정우성 | 머지 | 10-08 | 우희태 |
| [#55](#pr-55) | Feat: 서비스 로고 적용과 표지 디자인 개편 | 정우성 | 머지 | 10-08 | 박용민 |
| [#56](#pr-56) | Chore: dev → master 배포 반영 (로고 · 표지 개편 · README 출처) | 정우성 | 머지 | 10-08 | 박용민 |
| [#57](#pr-57) | Fix: 폴백 검색 정확도 개선 | 김권섭 | 머지 | 10-08 | 정우성 |
| [#58](#pr-58) | Fix: D-day 한국 날짜 기준 계산, 운영자 질문 삭제·답변 숨김 API, 지운 계정 401 | 우희태 | 머지 | 10-08 | 정우성 |
| [#59](#pr-59) | Feat: 이웃의 질문에 운영자 질문 지우기 · 답변 숨기기 버튼 | 정우성 | 머지 | 10-08 | 우희태 |
| [#60](#pr-60) | Chore: dev → master 배포 반영 (D-day · 운영자 정리 · 폴백 검색) | 정우성 | 머지 | 10-08 | 우희태 |
| [#61](#pr-61) | Feat: 상황 입력 · 할 일 상세 화면에 상단바 추가 | 정우성 | 머지 | 10-08 | 우희태 |
| [#62](#pr-62) | Chore: dev → master 배포 반영 (상황 입력 · 할 일 상세 상단바) | 정우성 | 머지 | 10-08 | 우희태 |
| [#63](#pr-63) | Fix: AI 실패 진단과 질문 API 요청 검증 강화 | 김권섭 | 머지 | 10-08 | 정우성 |
| [#64](#pr-64) | Fix: 폴백 검색 동의어와 쓰레기 질문 정확도 개선 | 김권섭 | 머지 | 10-08 | 정우성 |
| [#65](#pr-65) | Chore: dev → master 배포 반영 (검색 동의어 · AI 실패 로그) | 정우성 | 머지 | 10-08 | 김권섭 |
| [#66](#pr-66) | Docs: AI 초안 · 중복 판정을 다음 단계로 표시하고 테스트 건수 갱신 | 정우성 | 머지 | 10-09 | 김권섭 |
| [#67](#pr-67) | Feat: 원하는 답이 아니면 이웃에게 다시 묻기 | 김권섭 | 머지 | 10-09 | 정우성 |
| [#68](#pr-68) | Chore: dev → master 배포 반영 (이웃에게 다시 묻기 · 문서 정리) | 정우성 | 머지 | 10-09 | 박용민 |
| [#69](#pr-69) | Feat: 하단 탭으로 할 일 · 물어보기 · 이웃 질문 오가기 | 정우성 | 머지 | 10-10 | 김권섭 |
| [#70](#pr-70) | Feat: 로그인하면 내 질문 모아 보기 · 질문하기 로그인 안내 | 정우성 | 머지 | 10-10 | 김권섭 |
| [#71](#pr-71) | Feat: 카카오 로그인 추가 | 정우성 | 머지 | 10-10 | 김권섭 |
| [#72](#pr-72) | Feat: 주민 답변 기반 승격 AI 초안 추가 | 김권섭 | 머지 | 10-10 | 정우성 |
| [#73](#pr-73) | Feat: 동네 인증용 노원구 경계 데이터 추가 | 정우성 | 머지 | 10-10 | 우희태 |
| [#74](#pr-74) | Revert "Feat: 동네 인증용 노원구 경계 데이터 추가" | 우희태 | 닫힘 |  |  |
| [#75](#pr-75) | Feat: 노원 동네 인증 판정 로직과 저장 API 추가 | 우희태 | 머지 | 10-10 | 정우성 |
| [#76](#pr-76) | Feat: 노원 동네 인증 버튼과 답변 배지 추가 | 정우성 | 머지 | 10-10 | 우희태 |
| [#77](#pr-77) | Chore: dev → master 배포 반영 (카카오 로그인 · 동네 인증 · 하단 탭) | 정우성 | 머지 | 10-10 | 우희태 |
| [#78](#pr-78) | Docs: 전시 일정 · 새 기능 · 테스트 건수 반영 | 정우성 | 머지 | 10-11 | 우희태 |
| [#79](#pr-79) | Style: 화면 표면을 표지 기준으로 통일 · 평가 개선점 반영 | 정우성 | 머지 | 10-11 | 김권섭 |
| [#80](#pr-80) | Chore: dev → master 배포 반영 (화면 통일 · 문서 정리) | 정우성 | 머지 | 10-11 | 우희태 |
| [#81](#pr-81) | Fix: 상황 입력 반려동물 항목을 강아지로 좁히기 | 정우성 | 머지 | 10-11 | 우희태 |
| [#82](#pr-82) | Feat: 승격 화면에 같은 조건으로 이미 보이는 할 일 표시 | 정우성 | 머지 | 10-11 | 우희태 |
| [#83](#pr-83) | Feat: 승격 화면용 발행된 할 일 목록 API 추가 | 우희태 | 머지 | 10-11 | 정우성 |
| [#84](#pr-84) | Chore: dev → master 배포 반영 (강아지 조건 · 승격 겹침 패널 · API) | 정우성 | 머지 | 10-11 | 우희태 |

## 상세

<a id="pr-1"></a>

### #1 Chore: 프로젝트 뼈대와 기획 문서 공개

- 작성 정우성(@wo0oo) · `useong/midterm-loop` → `dev` · 머지 · 올림 2026-09-25 13:52 · 머지 2026-09-25 14:21
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/1

중간발표 전까지 프로젝트 뼈대와 저장소 세팅을 마치기 위한 PR. 개발은 아직 안 함.

##### 커밋 3개

| 커밋 | 내용 |
|---|---|
| `03d4d5e` | `.env`·`.env*.local` 을 git 추적에서 제외 (Neon 연결 문자열·Gemini 키 보호) |
| `3e0803a` | Next.js 스캐폴드 + Prisma 스키마 + Vitest 설정 |
| `be5eca6` | 기획 문서 공개 + 역할별 팀 브리프 |

##### 뼈대

- Next.js 16.3.6 (App Router, TypeScript), React 19
- Prisma **6.19.3 고정** 
- `prisma/schema.prisma` — `Task` · `Question` · `User` · `Answer` · `Confirmation` 5개 모델. 
- `lib/db.ts`, `vitest.config.ts`, `.env.local.example`

**마이그레이션은 아직 실행 X.** 실제 Neon 연결 문자열이 필요. `.env` 의 `DATABASE_URL` 을 채운 뒤 `npx prisma migrate dev --name init` 을 돌리면 이어짐.

##### 문서

- `docs/기획서.md` — 문제 정의, 차별점
- `docs/설계안.md` — 데이터 모델, API, 화면, AI 파이프라인, 오정보 방지 6층, 리스크
- `docs/승격시스템흐름.md` — 질문이 할 일로 승격되는 흐름
- `docs/구현계획.md` — task 단위 실행 계획
- `team/` — 역할 분담, 공용 타입 계약, 담당자별 브리프 4종


##### 확인 사항

- `npx prisma validate` / `npx prisma generate` 통과
- `npm test` — Vitest 설정 로드 정상 (테스트 파일 아직 없음)
- `.env`, `analysis/`, `*.pptx` 는 커밋에 포함 X

---

<a id="pr-2"></a>

### #2 Chore: dev → master 배포 반영 (프로젝트 뼈대와 기획 문서)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-09-25 14:21 · 머지 2026-09-25 14:27
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/2

`dev` 에 쌓인 저장소 부트스트랩 내용을 배포 브랜치 `master` 로 올립니다.

##### 들어가는 것

| 커밋 | 내용 |
|---|---|
| `03d4d5e` | `.env`·`.env*.local` 을 git 추적에서 제외 |
| `3e0803a` | Next.js 스캐폴드 + Prisma 스키마 + Vitest 설정 |
| `21621c8` | 기획 문서 공개 + 역할별 팀 브리프 |
| `b5bffc9` | 팀 역할 확정 반영, 발표 담당 이관 |

##### 구조

```
docs/     기획서 · 설계안 · 승격시스템흐름 · 구현계획
team/     역할별 작업 브리프 4종 (공용 타입 계약 포함)
prisma/   schema.prisma — Task · Question · User · Answer · Confirmation
lib/      db.ts
app/      Next.js 기본 스캐폴드
```

##### 팀

| 역할 | 담당 |
|---|---|
| 프론트엔드 · 저장소 관리 | 정우성 |
| 백엔드 · DB · 발표 | 우희태 |
| AI 파이프라인 | 김권섭 |
| 데이터 조사 | 박용민 |

##### 알아둘 것

- **마이그레이션은 아직 실행하지 않았습니다.** `.env` 의 `DATABASE_URL` 에 실제 Neon 연결 문자열을 넣고 `npx prisma migrate dev --name init` 을 돌려야 테이블이 생깁니다
- Prisma 는 **6.19.3 고정**입니다. `latest` 가 `8.0.0-rc` 로 잡히고 Prisma 7+ 는 `url = env(...)` 문법이 바뀌어 스키마를 다시 써야 합니다
- Next.js 는 **16.3.6** 입니다. 화면 작업 전에 `node_modules/next/dist/docs/` 를 확인해 주세요
- 기능 구현은 아직 없습니다. 이 PR 은 뼈대와 문서까지입니다

---

<a id="pr-3"></a>

### #3 Docs: 기본 브랜치를 dev 로 바꾼 것을 문서에 반영

- 작성 정우성(@wo0oo) · `useong/branch-policy` → `dev` · 머지 · 올림 2026-09-25 14:28 · 머지 2026-09-25 14:30
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/3

기본(default) 브랜치를 `master` → `dev` 로 변경한 것을 CONTRIBUTING.md 에 반영합니다.

##### 왜 바꿨나

GitHub 는 새 PR 의 base 를 기본 브랜치로 자동 지정합니다. 기본이 `master` 였을 때는 매번 base 를 `dev` 로 고쳐야 했고, 그래서 문서에 "base 가 master 가 아니라 dev 인지 확인" 이라는 경고를 달아두고 있었습니다. 기본을 `dev` 로 옮기면 그 실수가 구조적으로 사라집니다.

덤으로 저장소 첫 화면과 `git clone` 결과가 항상 최신 `dev` 가 됩니다. 문서가 중간발표 채점 대상(기획 문서의 재현 가능성)이라, 배포 머지를 놓쳐 옛 문서가 첫 화면에 걸리는 상황을 피할 수 있습니다.

##### 바뀐 곳 4군데

- 머리말 — `dev` 가 기본 브랜치임을 명시, `master` 는 평소 건드리지 않는 배포 전용
- 브랜치 구조 — 새 PR 의 base 가 자동으로 `dev` 로 잡힌다는 설명 추가
- 5번(PR 생성) — base 확인 경고 제거. 대신 `master` 로 잡히면 잘못된 것이라는 안내로 교체
- 7번(배포) — **배포 머지는 Squash 가 아니라 Merge commit** 이라는 규칙 명시. 실제로 PR #1·#2 를 그렇게 병합했습니다

`master` 는 Vercel 자동 배포 전용으로 그대로 둡니다.

---

<a id="pr-4"></a>

### #4 Merge: dev → master 배포 반영 (#2)

- 작성 정우성(@wo0oo) · `master` → `dev` · 머지 · 올림 2026-09-25 14:31 · 머지 2026-09-25 14:32
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/4

저장소 부트스트랩 — 프로젝트 뼈대와 기획 문서를 배포 브랜치에 반영한다.

---

<a id="pr-5"></a>

### #5 Docs: 김권섭 브랜치 로마자 표기 수정

- 작성 정우성(@wo0oo) · `useong/fix-branch-name` → `dev` · 머지 · 올림 2026-09-25 15:29 · 머지 2026-09-25 18:31
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/5

브랜치 이름 예시의 로마자 표기 오기 수정.

##### 변경
- `gwonseop` → `kwonseop` (3곳)
  - `CONTRIBUTING.md` 브랜치 구조 다이어그램
  - `CONTRIBUTING.md` 브랜치 이름 예시
  - `docs/설계안.md` 9.4 브랜치 구조

##### 이유
- 김 → `k`. 기존 표기가 오기
- 문서를 보고 브랜치를 따면 잘못된 이름이 생김

---

<a id="pr-6"></a>

### #6 Feat: DB 마이그레이션, D-day 계산, 시드 스크립트 추가

- 작성 우희태(@Heetaeeee) · `heetae/db-setup` → `dev` · 머지 · 올림 2026-09-25 18:23 · 머지 2026-09-26 13:55
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/6

- Prisma 초기 마이그레이션 (스키마 표 5개 생성)
- lib/dday.ts + 테스트 10개 통과
- 시드 3건(전입신고·확정일자·전월세신고) + sourceNote 비면 시딩 실패 확인
- seed-pending.md 조사 양식 (D 담당용)

---

<a id="pr-7"></a>

### #7 Feat: 공용 타입 계약 추가

- 작성 정우성(@wo0oo) · `useong/shared-types` → `dev` · 머지 · 올림 2026-09-26 13:56 · 머지 2026-09-26 13:57
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/7

화면·API·AI 공용 타입. `matching.ts` · `grounding.ts` 가 이걸 import 해야 해서 우희태·김권섭이 막혀 있었음.

##### 추가
- `lib/types.ts` — 타입 정의만, 런타임 코드 X

##### 주의
- `MatchedTask.category` 를 `string` → `TaskCategory` 로 좁힘 (`team/README.md` 도 같이 수정)
- Prisma enum 그대로 담으면 되므로 API 영향 X

##### 확인
- `npx tsc --noEmit` 통과

---

<a id="pr-8"></a>

### #8 Feat: 상황 입력과 할 일 목록 화면 추가

- 작성 정우성(@wo0oo) · `useong/setup-tasks-screens` → `dev` · 머지 · 올림 2026-09-26 14:10 · 머지 2026-09-26 14:47
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/8

9/28 시연 장면(상황을 바꾸면 목록이 갈린다)을 목 데이터로 먼저 구현.

##### 추가

| 경로 | 내용 |
|---|---|
| `app/setup` · `components/ProfileForm` | 상황 입력 |
| `app/tasks` · `components/TaskCard` | 할 일 목록 |
| `lib/profile.ts` | localStorage 저장 |
| `app/globals.css` | 본문 18px, 터치 타깃 48px |

##### 임시

- `lib/mock-tasks.ts` — `/api/tasks/match` 붙으면 통째로 삭제
- 내용은 `prisma/seed-data.ts` 시드 3건과 동일, 필터는 `lib/matching.ts` 를 세 줄로 흉내낸 것

##### 확인

- 전세 → 3건 / 기숙사비 → 1건 (브라우저 확인)
- 이사일 2026-09-01 → "기한 11일 지남" — 우희태 `lib/dday.ts` 결과
- `npx next build` 통과

##### 참고

- **화면 디자인은 추후 변경 예정.** 지금은 시연에 필요한 최소 형태

---

<a id="pr-9"></a>

### #9 Feat: AI 근거 검증 로직 추가

- 작성 김권섭(@kwonseop) · `kwonseop/gemini-grounding` → `dev` · 머지 · 올림 2026-09-26 15:23 · 머지 2026-09-26 15:45
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/9

##### 변경 내용
- AI가 반환한 근거 ID를 서버의 실제 ID 집합과 대조
- 존재하지 않는 근거와 중복 ID를 제거
- 허구 근거가 섞이거나 근거가 없을 때 신뢰도를 PARTIAL 또는 UNKNOWN으로 강등
- AI가 판단한 신뢰도를 서버가 임의로 상향하지 않음

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-09-26 15:45

#### 코멘트

- 정우성(@wo0oo) · 2026-09-26 15:44

  > 확인 완. 테스트 다 통과했고 타입도 문제 없음
  > 브리프랑 다르게 쓴 부분은 결과 같고 읽기 더 편해서 그걸로 쭉 가면 될듯
  > 
  > 근데 /api/ask 만들 때 confidence가 UNKNOWN이면 answer는 null로 내려주삼. 근거 없는 답이 화면에 뜨면 이거 만든 의미가 없어져서


---

<a id="pr-10"></a>

### #10 Fix: UNKNOWN 판정 시 AI 답변 차단

- 작성 김권섭(@kwonseop) · `kwonseop/unknown-answer-guard` → `dev` · 머지 · 올림 2026-09-26 18:50 · 머지 2026-09-27 12:00
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/10

##### 변경 내용

- UNKNOWN이면 answer가 null인 결과 타입과 groundAnswer() 추가
- 차단 시나리오 4건 및 GROUNDED/PARTIAL 답변 유지 테스트 2건 추가
- team/C-ai.md에 API 응답 및 Question.aiAnswer 저장 시 검증 결과를 사용하는 규칙 명시

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-09-27 12:00

#### 코멘트

- 정우성(@wo0oo) · 2026-09-27 11:57

  > 좋아요


---

<a id="pr-11"></a>

### #11 Docs: 월계1동 생활정보 조사 결과 추가

- 작성 박용민(@parkyongminn) · `yongmin/seed-waste` → `dev` · 머지 · 올림 2026-09-27 00:08 · 머지 2026-09-27 21:22
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/11

##### 작업 내용

월계1동 생활정보 조사 결과를 추가했습니다.

###### 확인 완료
- 일반 생활쓰레기 배출요일·시간
- 재활용 분리배출 요일·방법
- 월계1동 주민센터 주소·전화번호
- 대형폐기물 신고 절차
- 거주자우선주차 신청 절차
- 월세 세액공제
- 아파트 음식물쓰레기 처리방식
- 아파트 소형 폐가전 처리방식

###### 추가 확인 필요
- 음식물쓰레기 정확한 지정요일
- 월계1동 종량제봉투 실제 판매점
- 광운대 기숙사 전입신고 처리방식
- 월계동 동물등록 대행기관

확인하지 못한 값은 추정하지 않았습니다.

##### 공유사항

B는 확인 완료된 항목만 `prisma/seed-data.ts`에 반영해주세요.

A는 일반쓰레기 기준 월계1동 내부 세부 구역 구분이 공식 자료에서 확인되지 않은 점을 참고해주세요.

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-09-27 21:22

  > 굳


#### 코멘트

- 정우성(@wo0oo) · 2026-09-27 11:59

  > 조사 좋았음 근데 README.md 말고 별도 문서 만들어서커밋해줘
  > README.md는 건들면 안 돼
  > docs/월계1동_생활정보.md  이런식으로 따로 만들어서 ㄱㄱㄱ 파일만 옮기면 바로 승인함


---

<a id="pr-12"></a>

### #12 Feat: 프로필 매칭 로직과 할 일 조회 API 추가

- 작성 우희태(@Heetaeeee) · `heetae/match-api` → `dev` · 머지 · 올림 2026-09-27 18:19 · 머지 2026-09-27 18:45
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/12

- lib/matching.ts + 테스트 9개 통과 (전체 32개 통과)
- POST /api/tasks/match: 전세 3건 / 기숙사비 1건 / 이사 30일 전이면 기한 16일 지남 확인
- GET /api/tasks/[id]: 없는 id는 404
- lib/taskView.ts: 두 API가 같은 MatchedTask 모양을 내보내도록 변환 로직 통합

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-09-27 18:45

  > 확인 완 다 잘됨
  > 근데 본선때는 taskView.tst를 lib/server/로 옮기면 좋을듯 import 잘못하면 빨려들어가서


---

<a id="pr-13"></a>

### #13 Kwonseop/search fallback

- 작성 김권섭(@kwonseop) · `kwonseop/search-fallback` → `dev` · 닫힘 · 올림 2026-09-27 18:25
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/13

Feat: AI 호출 실패에 대비한 키워드 폴백 검색 추가

##### 구현 내용
- `title`, `why`, `howTo`에서 질문의 키워드로 관련 항목 검색
- 일치하는 서로 다른 키워드가 많은 순서로 정렬
- 동점이면 입력 순서를 유지하며 기본 최대 3개 반환
- 중복 키워드, 대소문자, 여러 공백 처리
- 빈 질문·빈 데이터·유효하지 않은 반환 개수는 빈 배열 반환
- 입력 배열과 원본 객체를 변경하지 않음

##### 검증
- 검색 테스트 22개 포함, 전체 테스트 39개 통과
- 변경 파일 ESLint 통과

##### 참고 사항
- 이번 PR은 검색 함수와 테스트만 포함. Gemini 실패 시 호출하는 `/api/ask` 연결은 후에 처리할 예정
- 검색 결과는 관련 항목 후보이며, 답변의 근거나 신뢰도를 확정하지 않음.
- 단순 부분 문자열 검색이므로 조사·동의어 처리는 지원하지 않음.

---

<a id="pr-14"></a>

### #14 Feat: 할 일 목록을 실제 API 로 연결

- 작성 정우성(@wo0oo) · `useong/wire-real-api` → `dev` · 머지 · 올림 2026-09-27 21:02 · 머지 2026-10-01 15:27
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/14

목데이터 없애고 API 연결

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-01 15:24

#### 코멘트

- 김권섭(@kwonseop) · 2026-10-01 15:22

  > API 연결 확인 했으


---

<a id="pr-15"></a>

### #15 Feat: AI 장애 대비 키워드 폴백 검색 추가

- 작성 김권섭(@kwonseop) · `kwonseop/search-fallback` → `dev` · 닫힘 · 올림 2026-09-29 17:19
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/15

##### 변경 내용

- 질문을 공백 기준 키워드로 나누고 중복 키워드를 제거
- 할 일의 `title`, `why`, `howTo`에서 관련 키워드 검색
- 일치한 서로 다른 키워드가 많은 항목부터 정렬
- 동점이면 기존 입력 순서를 유지하고 기본 최대 3개 반환
- 빈 질문·빈 데이터·유효하지 않은 `limit` 처리
- 입력 배열과 원본 객체를 변경하지 않도록 구현


##### 참고 사항

- 검색 결과는 관련 항목 후보이며 답변의 근거나 신뢰도를 확정하지 않음
- 부분 문자열 검색이므로 조사·동의어 처리는 지원하지 않음

---

<a id="pr-16"></a>

### #16 Feat: AI 장애 대비 키워드 폴백 검색 추가

- 작성 김권섭(@kwonseop) · `kwonseop/search-fallback` → `dev` · 머지 · 올림 2026-10-01 16:06 · 머지 2026-10-01 16:14
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/16

##### 변경 내용

- 질문을 공백 기준 키워드로 나누고 중복 키워드를 제거
- 할 일의 `title`, `why`, `howTo`에서 관련 키워드 검색
- 일치한 서로 다른 키워드가 많은 항목부터 정렬
- 동점이면 기존 입력 순서를 유지하고 기본 최대 3개 반환
- 빈 질문·빈 데이터·유효하지 않은 `limit` 처리
- 입력 배열과 원본 객체를 변경하지 않도록 구현

##### 참고 사항

- 검색 결과는 관련 항목 후보이며 답변의 근거나 신뢰도를 확정하지 않음
- 부분 문자열 검색이므로 조사·동의어 처리는 지원하지 않음
- Gemini 호출 실패 시 이 검색을 사용하는 `/api/ask` 연결은 후속 작업으로 진행
- 병합되지 않고 닫힌 기존 PR #13의 변경사항을 다시 제출

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-01 16:13

  > 조사 붙으면 처리가 안 돼서 질문 몇개가 빈 배열 나오는데 /api/ask 연결할 때 한번 더 보면 될듯


---

<a id="pr-17"></a>

### #17 Feat: 할 일 상세 화면 추가 및 화면 디자인 재작업

- 작성 정우성(@wo0oo) · `useong/task-detail` → `dev` · 머지 · 올림 2026-10-01 16:27 · 머지 2026-10-02 20:45
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/17

할 일 상세 화면을 추가하고 목록·입력 화면 디자인을 다시 짬. 화면 디자인은 추후에 변경될 수 있음.

상세 화면
- `/tasks/[id]` 추가 — 안 하면 어떻게 되나 · 어떻게 하나 · 어디서 · 온라인으로
- 금액·기한·장소·연락처는 DB 원문 그대로. AI 문장 없음
- 로딩 · 정상 · 404 · 실패 4상태
- 전화번호는 `tel:` 링크. 데이터가 비어 있으면 "어디서" 구획 숨김

디자인
- 공공 에디토리얼 스타일 — 굵은 구분선 · 카테고리 색띠 · D-day 히어로
- 가장 급한 항목 하나를 상단에 `D+16` 형태로 크게 표시
- 카테고리별 묶음 (행정 · 주거 · 쓰레기 · 생활)
- 색은 WCAG AAA(본문 7:1) 기준으로 계산해서 선택, 다크 모드 포함
- 카테고리는 색 + 글자 같이 표시 (색 단독 구분 X)
- `Noto Sans KR` 적용 (`next/font`, 자체 호스팅)
- 포커스 링 · `prefers-reduced-motion` 대응

정리
- `lib/useProfile.ts` — localStorage 읽기를 `useSyncExternalStore` 로 교체, lint 에러 2건 제거
- 상황 입력 안내 문구 수정 — "서버로 보내지 않습니다" → 할 일을 고를 때만 전송, 서버에 남기지 않음
- `lib/labels.ts` · `lib/taskGroups.ts` 로 목록·상세 공통 라벨과 그룹핑 분리

##### 확인 사항
- `vitest` 76건 통과 (신규 라벨 · 그룹핑 단위 테스트 포함)
- `tsc --noEmit` · `eslint` 통과 · `next build` 통과
- 실제 Neon DB로 `/` → `/tasks` → 상세 → 404 브라우저 확인
- 시드에 장소·전화가 없어 "어디서" 구획은 아직 안 뜸 — 조사·시딩 대기

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-02 20:42

  > 확인했습니당


---

<a id="pr-18"></a>

### #18 Feat: 할 일 완료 체크와 진행률 추가

- 작성 정우성(@wo0oo) · `useong/task-progress` → `dev` · 머지 · 올림 2026-10-01 16:35 · 머지 2026-10-02 20:53
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/18

할 일 완료 체크와 진행률 표시를 추가함. #17 위에 쌓인 PR.

완료 체크
- 상세 화면에 `완료했어요` 버튼 — 누르면 완료 상태 전환, 다시 누르면 취소
- 완료 목록은 localStorage 에만 저장, 서버 전송 X
- 저장 실패 시(시크릿 창 등) 경고 문구 표시
- 깨진 저장값·배열 아닌 값이 있어도 빈 목록으로 복구

진행률
- 목록 상단에 `3건 중 1건 완료` + 진행 바
- 끝낸 일은 하단 "끝낸 일" 구획으로 이동 (취소선 + `✓ 완료`)
- 지금 가장 급한 일(`D-n`)은 안 끝낸 것 중에서만 선택

확인 사항
- `vitest` 92건 통과 (신규 16건)
- `tsc --noEmit` · `eslint` · `next build` 통과
- 브라우저에서 확인 — 즉시 반영 · 새로고침 후 유지 · 진행 바 · 히어로 이동 · 깨진 저장값 복구

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-02 20:52

  > 할 일 완료 / 진행률 확인했어


---

<a id="pr-19"></a>

### #19 Chore: CI 워크플로 추가

- 작성 정우성(@wo0oo) · `useong/ci` → `dev` · 머지 · 올림 2026-10-01 16:40 · 머지 2026-10-02 20:53
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/19

PR·푸시마다 린트·타입 검사·테스트·빌드를 자동으로 돌리는 GitHub Actions 워크플로 추가.

트리거
- `dev` · `master` 로 가는 PR
- `dev` · `master` 푸시
- 같은 브랜치에 연달아 푸시하면 앞선 실행 취소

단계
- `npm ci` → `prisma generate` → `npm run lint` → `tsc --noEmit` → `npm test` → `npm run build`
- Node 24, npm 캐시 사용

설정
- 비밀값 X — 할 일 API 가 전부 요청 시점에 DB 를 읽는 동적 라우트라 빌드·테스트에 실제 DB 불필요
- `DATABASE_URL` 은 더미 값 (Prisma 클라이언트 생성용)
- `permissions: contents: read`, 타임아웃 10분

##### 확인 사항
- 같은 명령을 더미 `DATABASE_URL` 로 로컬에서 실행 — 전부 통과 (`vitest` 92건)
- `npm run lint` 저장소 전체 에러 0건
- 깨끗한 체크아웃에서의 동작은 이 PR 의 첫 Actions 실행으로 확인 필요

머지 후
- `master-protection` 에서 `check` 잡을 필수 상태 체크로 지정 가능 (설정 변경은 이 PR 에 포함 X)

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-02 20:51

  > 좋아용


---

<a id="pr-20"></a>

### #20 Docs: 구현계획 진행 현황과 읽는 법 추가

- 작성 정우성(@wo0oo) · `useong/docs-progress` → `dev` · 머지 · 올림 2026-10-01 16:55 · 머지 2026-10-02 00:12
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/20

구현계획 문서에 읽는 법과 진행 현황 표를 추가함. 문서의 코드가 완성된 결과물이 아니라 구현 전 계획이라는 점을 명시.

읽는 법
- 문서 안의 코드는 목표 형태이지 완성된 결과물이 아님을 안내
- 계획과 실제가 달라진 3곳을 표로 정리 (변환 로직 분리 · 반환값 분기 · 타입 위치)

진행 현황
- Task 1~11 상태 표 추가, 2026-10-01 `dev` 기준
- 시드는 스크립트만 완료, 내용물 3건 — 조사·입력 대기로 표기
- 근거 검증·검색 완료, 단 검색은 조사를 처리하지 않음
- 아직 머지되지 않은 PR 은 번호로 표시 (#17 · #18 · #19)
- 단위 테스트 54건 (`dev` 기준, 매칭 9 · 기한 10 · 근거 검증 13 · 검색 22)

수정
- `Next.js 15` → `16`, `Prisma 6.19.3` 고정 반영

확인 사항
- 테스트 건수는 `dev` 만 따로 떼어 `vitest` 를 실행해 확인
- 문서만 변경, 코드 변경 X
- 표에 적힌 PR 번호는 머지되면 낡으므로 머지 후 갱신 필요

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-02 00:07

  > 진행상황 읽는법 확인했습니당


---

<a id="pr-21"></a>

### #21 Docs: 생활정보 추가 조사 결과 반영

- 작성 박용민(@parkyongminn) · `yongmin/research-update` → `dev` · 머지 · 올림 2026-10-02 02:23 · 머지 2026-10-03 16:41
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/21

##### 작업 내용

월계1동 생활정보 추가 조사 결과를 반영했습니다.

- 종량제봉투 판매처 4곳 추가
- 월계동 동물등록 대행기관 4곳 추가
- 기존 조사정보 최신화
- 미확정 항목은 추정하지 않고 보류

리뷰 부탁드립니다.

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-03 16:41

  > 굳


#### 코멘트

- 정우성(@wo0oo) · 2026-10-02 20:12

  > 음식물쓰레기 주6일만 나와있고 정확한 요일명이 없음. 구역별로 다른지도 없고.
  > 확인 부탁

- 정우성(@wo0oo) · 2026-10-03 14:03

  > 문서에서 "토요일 및 공휴일 전일 배출 금지"인 부분도 있고, "공휴일 제외"인 부분도 있음.
  > 공휴일이 월요일이면 "전일 배출 금지"는 일요일 밤도 막고, "공휴일 제외"는 일요일을 허용함.
  > 원문 보고 어느쪽인지 맞춰줘 그 뒤에 승인할게

- 박용민(@parkyongminn) · 2026-10-03 15:03

  > 확인했습니다

- 정우성(@wo0oo) · 2026-10-03 15:41

  > 정정할거 있음
  > 내가 찾아보니까 주 6일(일-금, 공휴일 제외)에 공휴일 전일은 배출금지도 포함이네
  > 기존 정보는 삭제하지 말고
  > 음식물쓰레기 절(84-92줄)에도 "공휴일 전일 금지" 추가해서 맞춰주삼.
  > 규칙은 "일~금, 단 공휴일과 공휴일 전날 제외"
  > 추가되면 승인할게


---

<a id="pr-22"></a>

### #22 Feat: 조사 완료된 생활정보 시드 10건 추가

- 작성 우희태(@Heetaeeee) · `heetae/seed-research` → `dev` · 머지 · 올림 2026-10-02 14:47 · 머지 2026-10-06 15:59
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/22

- docs/월계1동_생활정보.md의 "확인 완료" 항목만 시드로 추가 (3건 → 13건)
- 쓰레기 규칙을 원룸·빌라 / 아파트 / 기숙사별로 분리
- 거주자 우선주차(차량), 월세 세액공제(월세) 추가
- 전입신고·확정일자·전월세 카드에 월계1동 주민센터 주소·전화 추가
- 미확인 항목(음식물 요일, 봉투 판매점, 빛솔재 전입신고, 동물등록 대행기관)은 제외
- 확인: 원룸·월세 8건, 기숙사·기숙사비 2건

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 15:58

  > 제목/본문 건수 실제(14건 추가, 총 17건)랑 다름, 본문의 "봉투 판매점 제외"도 지금이랑 안 맞음
  > 근데 사소해


#### 코멘트

- 정우성(@wo0oo) · 2026-10-02 20:11

  > 1. 거주자 우선주차 전화번호 02-2289-6727로 돼있는데 이거 거주자보험 번호임. 용민이 문서에 있는건 02-2289-6732.  02-2289-6727로 전화하면 보험 부서로 전화 걸릴듯
  > 2. 오피스텔은 대형폐기물 빼면 쓰레기 항목 하나도 안 뜨는데 의도한건지 궁금
  > 3. 기숙사랑 동물등록도 확인 됐으니 그거 반영하면 될듯
  > 4. studentOnly: true 지워주삼

- 우희태(@Heetaeeee) · 2026-10-05 11:16

  > 반영했습니다!
  > 1. 주차 전화번호 02-2289-6732로 수정 (공단 조직표 교차확인 내용 sourceNote에 기록)
  > 2. 오피스텔 전용 배출 규칙은 공식 확인이 안 돼서 의도적으로 뺐어요. 대신 종량제봉투 판매처를 오피스텔에도 노출
  > 3. 용민 10/2 확인분 추가: 음식물쓰레기, 종량제봉투 판매처, 빛솔재 거주증명서 전입신고, 반려견 동물등록 (13건 → 17건)
  > 4. 빛솔재 쓰레기 studentOnly 삭제
  > 확인: 원룸·월세 10건 / 기숙사·기숙사비 3건 / 오피스텔·월세 6건

- 정우성(@wo0oo) · 2026-10-05 12:55

  > 1. 생활쓰레기 카드 why에는 "공휴일 전날"이 있는데 howTo랑 sourceNote는 "일~금(공휴일 제외)"만 있음. 이거 맞춰주삼
  > 2. 기숙사 전입신고 카드에 기한이 없는데 빛솔재 카드를 dueOffsetDatys: 14로 하고 일반 전입신고 카드에서 DORM을 빼는 게 나아 보임. 어떤지는 너가 판단해서 반영해줘
  > 3. 기숙사 카드 "평일 09:00~17:30"에서 "평일"은 용민이가 조사한 내용에 없음. 그리고 빛솔재 홈페이지도 확인해봤는데 요일 얘기는 안 나와있음. 빼거나 용민이한테 확인 받아야할듯

- @vercel · 2026-10-06 15:27

  > [vc]: #mh5MlqjCGF05O3LbhK1svJudFzYXmY8diT/7Tke8dzw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwicm9vdERpcmVjdG9yeSI6bnVsbCwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8ybks4WlNQVjdUaUxjeWR0Z2VaZXJEM0dNaFFUIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtc2VlZC1yZXNlYXJjaC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLXNlZWQtcmVzZWFyY2gtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifX1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/2nK8ZSPV7TiLcydtgeZerD3GMhQT) | [Preview](https://nowonlikeus-git-heetae-seed-research-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T06:27:39.003Z">Oct 6, 2026 6:27am UTC</relative-time> |

- 우희태(@Heetaeeee) · 2026-10-06 15:30

  > 반영했습니다!
  > 1. 생활쓰레기 howTo·sourceNote를 용민 문서 최종 규칙(일~금, 토요일·공휴일 전날 배출 금지)으로 맞춤. 같은 페이지 상단의 "공휴일 제외"보다 구체적인 수거업체 표 기준이라는 것도 sourceNote에 기록
  > 2. 제안대로 빛솔재 전입신고 카드에 dueOffsetDays: 14 넣고, 일반 전입신고 카드에서 DORM 제외 (기숙사 → 2건)
  > 3. 행정실 운영시간에서 "평일" 삭제 (용민 문서에도 09:00~17:30만 있음)


---

<a id="pr-23"></a>

### #23 Docs: 생활정보 직접 확인 결과 반영

- 작성 박용민(@parkyongminn) · `parkyongminn-patch-1` → `dev` · 닫힘 · 올림 2026-10-02 18:36
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/23

##### 작업 내용
월계1동 생활정보 조사 결과를 최신화했습니다.

- 음식물쓰레기 배출 원칙 노원구청 자원순환과 전화 확인 반영
- 빛솔재 전입신고 처리방식 행정실 전화 확인 반영
- 종량제봉투 판매처 4곳 반영
- 동물등록 대행기관 4곳 반영
- 공식 출처 URL 및 sourceNote 보완
- 미확정 값은 추정하지 않음

리뷰 부탁드립니다.

---

<a id="pr-24"></a>

### #24 Fix: 조사와 문장부호로 인한 폴백 검색 누락 수정

- 작성 김권섭(@kwonseop) · `kwonseop/search-fallback` → `dev` · 머지 · 올림 2026-10-02 23:42 · 머지 2026-10-03 14:02
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/24

##### 변경 내용
- `전입신고`는 검색되지만 `전입신고는?`처럼 조사·문장부호가 붙으면 빈 배열이 반환되는 문제를 수정
- 질문의 단어 앞뒤 문장부호 제거
- 흔한 조사 한 개를 제거한 검색어도 함께 비교
- 원래 단어의 일치 유지
- 조사 변형을 반복해도 동일 키워드 점수 중복 방지
- 조사 제거 후 한 글자만 남는 경우 검색 범위 확대 방지
- 회귀 테스트 11개 추가

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-03 14:02

  > 담부턴 커밋메시지 Docs: ... 로 해주삼 일단 머지할게


---

<a id="pr-25"></a>

### #25 Feat: Gemini 구조화 응답 호출 추가

- 작성 김권섭(@kwonseop) · `kwonseop/gemini-client` → `dev` · 머지 · 올림 2026-10-02 23:51 · 머지 2026-10-03 14:03
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/25

##### 변경 내용

- SDK 없이 Gemini REST API를 호출하는 `askGemini` 구현
- `answer`, `sourceIds`, `confidence` 구조화 응답 요청 및 반환 형식 검증
- 키 누락·HTTP 오류·네트워크 오류·응답 파싱 실패 시 `null` 반환
- 15초 시간 제한과 요청 중단 처리
- 기본 모델을 `gemini-3.1-flash-lite`로 설정하고 환경 변수 예시·문서 반영
- Gemini client 테스트 29개 추가

##### 참고 사항

- 이번 PR은 Gemini 호출 함수까지이며 `/api/ask` 연결은 미포함
- 반환값은 미검증 AI 응답이므로 API 응답·저장 전 반드시 `groundAnswer`를 거쳐야 함
- 호출 실패 시 반환되는 `null`을 받아 키워드 폴백으로 연결하는 작업은 `/api/ask`에서 진행
- 검색 조사 처리 수정은 별도 PR로 관리
- 실제 API 키는 커밋 X

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-03 14:03

  > 일단 승인할게 근데 /api/ask 붙일때
  > 
  > 1. 숫자는 AI가 만들지 않는다는 규칙은 프롬프트로만 막혀있음. 이게 핵심인데 코드가 검사를 안 해서 응답에 숫자가 있으면 걸러내는 로직 필요할듯 
  > 
  > 2. 질문이랑 profileLine이 제미나이 통해서 구글로 나가는데 상황 입력 화면엔 "서버에 남기지 않습니다"가 있음. 무료 티어 약관에서 입력 데이터를 어떻게 쓰는지 확인해주면 좋을듯. 그리고 profileLine에 뭘 넣을지 (주거형태/계약형태만 넣을지, 이사일은 뺄지) 정해주삼. 그거 맞춰서 프론트 안내 문구 만들게


---

<a id="pr-26"></a>

### #26 Feat: 질문 API 연결 및 AI 안전장치 추가

- 작성 김권섭(@kwonseop) · `kwonseop/ask-api` → `dev` · 닫힘 · 올림 2026-10-03 21:59
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/26

##### 변경 내용

- `POST /api/ask` 구현
  - 질문 및 상황 정보 검증
  - 공개된 항목 조회 → Gemini 또는 키워드 검색 → 근거 검증
  - 검증 결과 저장 및 원문 카드 반환
- Google 전송을 기본 차단하는 `GEMINI_ALLOW_USER_INPUT` 설정 추가
  - 미설정 또는 `false`이면 API 키가 있어도 키워드 검색 사용
- 숫자·흔한 한글 수량이 포함된 AI 답변은 폐기하고 폴백
- `UNKNOWN` 답변은 응답·저장 모두 `null` 처리
- AI에 전달하는 상황 정보를 주거형태·계약형태로 제한
  - 이사일은 카드 기한 계산에만 사용하며 Google 전송·DB 저장 제외
- 상황 입력 안내 문구와 데이터 처리 문서 수정

##### 참고 사항

- API 요청·응답 타입 구조와 DB 스키마 변경 없음
- 자체 DB에는 질문, 주거형태·계약형태, 검증된 답변·근거·신뢰도를 저장
- 질문 화면 연결, 제출 전 고지, 인증·남용 방지는 후속 협업 필요
- 무료 티어에서는 외부 전송 차단 유지. AI 활성화 전 유료 프로젝트와 고지·운영 정책 확인 필요
- 한글 수량 검사는 휴리스틱이므로 모든 자연어 수치 표현의 차단을 보장하지 않음

##### 전달사항
profileLine에는 **주거형태·계약형태만** 넣는 걸로 구현
예: `주거형태: 원룸, 계약형태: 월세`

이사일은 카드 기한 계산에만 쓰고 Google로 보내거나 DB에 저장하지 않음
구역·차량·반려동물·학생 여부도 AI에 보내지 않음

현재는 Google 전송을 차단해 둬서 키워드 검색만 동작함
나중에 AI를 활성화하면 질문 본문 + 주거형태·계약형태가 Google로 전달되게 됨

다만 AI 사용 여부와 상관없이 질문 본문과 주거형태·계약형태는 우리 DB에 저장돼서
“질문 내용과 주거형태·계약형태는 답변 및 후속 확인을 위해 서버에 저장됩니다. 이름·연락처·상세 주소 등 개인정보는 입력하지 마세요.”
라는 식으로 안내하면 될 것 같음

Google 전송 안내는 AI 활성화할 때 추가하면 됨

#### 코멘트

- 정우성(@wo0oo) · 2026-10-05 13:04

  > <img width="695" height="549" alt="image" src="https://github.com/user-attachments/assets/8edfdcd9-b9a8-41c1-9e46-7c5a10e90555" />
  > 
  > "이 주민센터에서~~"에서 "이 주"를 숫자로 인식하고 나머지 오탐들도 "이" 뒤에 단위가 붙으면 숫자로 인식하는듯. 보완 부탁


---

<a id="pr-27"></a>

### #27 Feat: 로그인·질문·답변·승격 공용 타입 초안 추가

- 작성 정우성(@wo0oo) · `useong/qa-types` → `dev` · 머지 · 올림 2026-10-05 13:14 · 머지 2026-10-06 13:18
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/27

본선 범위(로그인·질문·답변·승격) API 의 요청·응답 타입 초안 추가. 담당자 검토 전이라 확정 아님 — 희태·권섭 확인 필요.

추가한 타입
- 인증: SessionUser · SignupRequest · LoginRequest · AuthResponse · MeResponse
- 질문·답변: QuestionItem · AnswerItem · QuestionListResponse · CreateAnswerRequest/Response · ConfirmAnswerResponse
- 승격: TaskDraft · PromotionQueueResponse · PromoteDraftRequest/Response · PromoteRequest/Response
- 공통: ApiErrorResponse · UserRole · QuestionStatus

설계 판단
- 이메일·비밀번호 해시는 어떤 응답에도 포함 X, 화면에는 닉네임만
- 비로그인 상태의 GET /api/auth/me 는 401 이 아니라 200 + { user: null }
- TaskDraft 는 TaskConditions 확장 — matching.ts 와 같은 노출 조건 그대로 사용
- PromoteDraftResponse.draft 는 null 가능 — AI 실패 시 운영자가 빈 양식에 직접 작성
- PromoteRequest.sourceNote 필수, verifiedAt 은 서버가 발행 시각으로 채움
- PromoteResponse 는 taskId 만 — daysLeft 는 특정 사용자 이사일 기준이라 발행 시점에 계산 불가

검토 요청 (설계안 2.5 API 목록에 없던 것)
- GET /api/auth/me — 화면의 로그인 상태 확인용
- GET /api/admin/promotions — 승격 큐 조회
- POST /api/admin/promote/draft — AI 초안 요청

확인 사항
- enum 6종 값이 prisma/schema.prisma 와 일치하는지 스크립트로 대조
- tsc --noEmit · eslint · vitest 132건 통과
- 타입 정의만 추가, 런타임 코드 X
- 열린 PR #22 · #26 과 충돌 없음

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 13:06
- **승인** — 김권섭(@kwonseop) · 2026-10-06 13:06

#### 코멘트

- 김권섭(@kwonseop) · 2026-10-06 00:37

  > 권섭 확인
  > 
  > 현재 C-ai 담당 코드와 충돌하는 부분은 따로 없음
  > 
  > - `UserRole`, `QuestionStatus` 값은 현재 Prisma enum과 일치
  > - `QuestionItem.aiAnswer`와 `confidence` 구조는 현재 서버 고정 안내 및 `UNKNOWN → null` 처리와 호환
  > - `ApiErrorResponse`도 현재 질문 API의 `{ error: string }` 응답과 일치
  > - `GET /api/auth/me`, `GET /api/admin/promotions`, `POST /api/admin/promote/draft` 타입 추가는 C-ai 범위와 충돌하지 않아 초안으로 사용해도 오케


---

<a id="pr-28"></a>

### #28 Feat: 질문 화면과 신뢰도 배지 추가

- 작성 정우성(@wo0oo) · `useong/ask-screen` → `dev` · 머지 · 올림 2026-10-05 13:37 · 머지 2026-10-06 13:18
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/28

질문하기 화면(/ask)과 AI 답변 신뢰도 배지 추가. #26(/api/ask) 머지 후 실제 동작.

화면
- 질문 입력, 1000자 제한, 글자 수 표시
- 제출 버튼 바로 위에 저장 고지 (질문 내용·주거형태·계약형태 서버 저장, 개인정보 입력 금지)
- 결과 표시 — GROUNDED · PARTIAL · UNKNOWN · 폴백 · 서버 오류
- 배지 문구는 설계안 3.1, 폴백 문구는 설계안 3.5 그대로
- 근거 카드는 기존 할 일 카드 재사용 (DB 원문)
- 목록 화면 하단에 질문하기 링크

안전장치
- UNKNOWN 인데 문장이 실려 와도 화면에서 다시 버림
- 질문에 주거형태·계약형태·이사일만 전송, 구역·차량·반려동물·학생 여부 전송 X

접근성
- 배지는 기호 + 글자 (색 단독 구분 X), PARTIAL 노랑도 AAA 대비
- 결과가 나오면 결과 제목으로 초점 이동
- 빈 질문은 입력칸 바로 아래 오류

변경
- lib/types.ts: AskRequest.profile 을 AskProfile(주거형태·계약형태·이사일)로 좁힘 — #26 라우트는 이 타입 미사용이라 영향 없음 (권섭 확인 요청)
- 목록 화면의 제호를 components/Masthead.tsx 로 분리

확인 사항
- vitest 141건 통과 (신규 9건)
- tsc --noEmit · eslint · next build 통과
- 열린 PR #22 · #26 · #27 과 충돌 없음
- 브라우저에서 응답을 가짜로 넣어 상태별 화면 확인. 실제 /api/ask 연결은 미확인 (공용 DB 에 테스트 질문이 저장돼서 보류)

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 13:06

#### 코멘트

- 김권섭(@kwonseop) · 2026-10-06 00:45

  > 권섭 확인
  > 
  > `AskRequest.profile`을 `AskProfile`로 좁히는 변경은 현재 `/api/ask` 구현과 일치
  > 서버는 실제로 `housingType`, `contractType`, `moveInDate`만 사용하며 질문 화면에서도 동일한 세 필드만 전송하므로 타입 및 런타임 모두 문제 X
  > 현재 PR #30~#32의 질문 API와 질문 화면을 합친 상태에서 테스트, 타입 검사, 린트, 프로덕션 빌드까지 통과
  > 
  > 다만 의존 PR 표시는 현재 분할 PR #30~#32를 기준으로 갱신 해봐야 될 듯


---

<a id="pr-29"></a>

### #29 Chore: 설치 시 Prisma 클라이언트 생성 스크립트 추가

- 작성 정우성(@wo0oo) · `useong/vercel-prep` → `dev` · 머지 · 올림 2026-10-05 18:37 · 머지 2026-10-06 13:19
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/29

Vercel 배포를 위해 설치 시 Prisma 클라이언트를 생성하는 postinstall 스크립트 추가.

변경
- package.json: "postinstall": "prisma generate"

이유
- 새 npm 은 의존성의 설치 스크립트(@prisma/client · @prisma/engines 등)를 승인 없이 실행하지 않음
- 이 줄이 없으면 Vercel 빌드에서 Prisma 클라이언트가 안 만들어질 수 있음
- 프로젝트 자체의 postinstall 은 막히지 않아서 이 줄로 해결

확인 사항
- 빈 폴더에서 npm ci → next build 로 Vercel 과 같은 순서 확인, 클라이언트 생성·빌드 통과
- CI 의 prisma generate 단계와 중복되지만 동작에 영향 X

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 13:06

---

<a id="pr-30"></a>

### #30 Feat: 질문 API 연결 및 안전한 폴백 처리 추가

- 작성 김권섭(@kwonseop) · `kwonseop/ask-api-core` → `dev` · 머지 · 올림 2026-10-05 22:37 · 머지 2026-10-06 13:50
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/30

##### 작업 내용

- `POST /api/ask` 질문 API를 추가
- 질문 및 프로필 입력값 검증을 추가
- 외부 AI 전송은 `GEMINI_ALLOW_USER_INPUT=true`일 때만 허용하도록 구성
- 기본 설정에서는 사용자 질문을 외부로 전송하지 않고 키워드 검색을 사용
- Gemini 호출 실패, 잘못된 근거 ID, 수치가 포함된 AI 응답은 안전하게 차단하고 폴백
- 검증된 근거만 응답과 질문 기록에 저장하도록 처리
- 질문 제출 시 저장되는 정보와 외부 전송 조건을 문서화
- API, Gemini 예외 처리 및 근거 검증 테스트를 추가

##### 참고 사항

- 외부 AI 입력 전송은 기본적으로 비활성화
- AI 생성 문장 고정 안내 전환과 Gemini 후보 범위 제한은 후속 PR로 분리
- 후속 안전장치 PR이 반영되기 전까지는 `GEMINI_ALLOW_USER_INPUT=false` 유지를 권장

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 13:49

#### 코멘트

- @vercel · 2026-10-05 22:37

  > [vc]: #Ik3QxMJlu71ZJ7ERgsjufdkk9tNoOZxHT11PMdB9Lzk=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwicm9vdERpcmVjdG9yeSI6bnVsbCwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy83eVpFZ25aS21oNUN3WXJFMXI1M2V2OXU4eDJRIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMudmVyY2VsLmFwcCJ9fV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/7yZEgnZKmh5CwYrE1r53ev9u8x2Q) | [Preview](https://nowonlikeus.vercel.app) | <relative-time datetime="2026-10-06T04:16:47.446Z">Oct 6, 2026 4:16am UTC</relative-time> |


---

<a id="pr-31"></a>

### #31 Fix: AI 생성 문장을 서버 고정 안내로 대체

- 작성 김권섭(@kwonseop) · `kwonseop/ask-answer-safety` → `dev` · 머지 · 올림 2026-10-05 22:56 · 머지 2026-10-06 13:53
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/31

##### 작업 내용

- Gemini가 생성한 답변 문장을 사용자 응답과 DB에 직접 사용하지 않도록 변경
- 검증된 근거가 있으면 서버가 관리하는 고정 안내 문구만 반환하도록 수정
- AI가 제시한 근거 ID와 신뢰도만 검증에 사용
- 근거가 없거나 신뢰도가 `UNKNOWN`이면 `answer: null`과 빈 근거 목록을 유지
- 숫자 탐지 정규식에 의존하던 차단 방식을 제거
- `이번`, `이사일` 등의 일반어가 숫자로 잘못 인식되는 문제를 제거
- 금액·기한·날짜·주소·전화번호 등의 정보는 검증된 DB 원문 카드에서 그대로 제공
- 변경된 안전 정책을 API 문서와 `team/C-ai.md`에 반영
- AI 원문 미노출, 고정 안내 반환 및 일반어 오탐 방지 테스트를 추가

##### 변경 효과

기존 방식은 AI 문장에서 숫자를 찾아 차단했기 때문에 자연어 수치를 놓치거나 일반 단어를 숫자로 잘못 판단할 수 있었음.
하지만 변경 후에는 AI 문장을 아예 노출하거나 저장하지 않으므로 수치 탐지의 누락과 오탐에 의존하지 않게 됨. 사용자는 검증된 원문 카드에서 실제 수치와 세부 정보를 확인하게 됨.

##### PR 관계

이 PR은 `kwonseop/ask-api-core` 위에 쌓인 두 번째 PR
Gemini가 선택할 수 있는 후보를 질문 관련 항목으로 제한하는 작업은 후속 `kwonseop/ask-candidate-scope` PR

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 13:50

#### 코멘트

- @vercel · 2026-10-05 22:56

  > [vc]: #1iNZubSkf1IAFmZuGaTaQgB86m6GTvefvy1rDs8FA38=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwicm9vdERpcmVjdG9yeSI6bnVsbCwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9EdGZDR1pycmg3bTFlU2MzU2IxMkVuajE3c29QIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stYW5zd2VyLXNhZmV0eS13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQta3dvbnNlb3AtYXNrLWFuc3dlci1zYWZldHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifX1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/DtfCGZrrh7m1eSc3Sb12Enj17soP) | [Preview](https://nowonlikeus-git-kwonseop-ask-answer-safety-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-05T13:57:19.312Z">Oct 5, 2026 1:57pm UTC</relative-time> |


---

<a id="pr-32"></a>

### #32 Fix: Gemini 근거를 키워드 후보로 제한

- 작성 김권섭(@kwonseop) · `kwonseop/ask-candidate-scope` → `dev` · 머지 · 올림 2026-10-06 00:14 · 머지 2026-10-06 22:53
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/32

##### 작업 내용

- Gemini 호출 전에 `keywordSearch`로 질문과 관련된 Task 후보를 계산하도록 변경
- 검색 순위가 높은 후보를 최대 3개까지만 Gemini 지식으로 전달
- Gemini가 반환한 근거 ID도 동일한 후보 집합 안에서만 인정
- DB에 존재하더라도 질문 후보에 포함되지 않은 Task ID는 근거로 사용할 수 없음
- 검증된 후보에 해당하는 원문 카드만 API 응답에 포함
- 후보가 없으면 Gemini를 호출하지 않고 빈 키워드 폴백 결과를 반환
- 후보 제한 정책을 API 문서와 `team/C-ai.md`에 반영

##### 변경 효과

기존에는 공개 Task 전체가 Gemini의 선택 범위였기 때문에, DB에 실제로 존재하지만 질문과 무관한 Task가 근거로 선택될 수 있는 문제가 존재
변경 후에는 서버의 키워드 검색을 통과한 최대 3개 후보만 전송·검증·응답에 사용됨
따라서 외부 전송 범위와 잘못된 근거 선택 가능성 감소

###### 병합 순서:
1. `kwonseop/ask-api-core`
2. `kwonseop/ask-answer-safety`
3. `kwonseop/ask-candidate-scope`

####### 추가 수정
피드백 반영

- 프로필이 전달되면 공개 할 일을 `matchesProfile`로 먼저 필터링하도록 수정
- `hasCar`, `hasPet`, `isStudent`가 누락된 이전 요청은 `false`로 처리
- 세 값은 할 일 필터링에만 사용하며 DB에 저장하거나 Gemini로 전송하지 않도록 수정
- Gemini에는 키워드 상위 3개가 아니라 프로필에 맞는 전체 할 일을 전달
- Gemini가 비활성화 됐거나 호출에 실패하면 프로필에 맞는 할 일 안에서만 기존 키워드 검색을 사용
- 프로필에 맞지 않는 Task ID는 Gemini가 반환해도 근거로 인정하지 않도록 수정

아래 상황을 테스트 -> 통과

- 원룸 사용자에게 기숙사 전용 카드가 노출되지 않음
- 차량·반려동물·학생 여부의 누락 및 `true` 조건 처리
- “쓰레기봉투 어디서 사요?”처럼 DB 문구와 다른 질문도 Gemini가 전체 후보에서 찾을 수 있음
- AI 미사용 시에도 프로필 필터 이후 키워드 검색
- 프로필에 맞는 후보가 없으면 Gemini를 호출하지 않음

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 20:17

  > 승인. 1·2번 반영 확인 (상황 필터 먼저, 후보 전체 전달, 원룸에 기숙사 카드 X 테스트)
  > - 이 PR 커밋들도 작성자 이메일 kapafe.kw.ac.kr (@ 빠짐) → #40 이랑 같이 고쳐줘


#### 코멘트

- @vercel · 2026-10-06 00:16

  > [vc]: #KPOZV3tHvevXsnLGz9EeuKyztVLrJAcN7n27LIvhm8Y=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwicm9vdERpcmVjdG9yeSI6bnVsbCwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zQXBGZTRrd2tBc21SRTk3VEZ3WUNZdjdSYzR3IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stY2FuZGlkYXRlLXNjb3BlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stY2FuZGlkYXRlLXNjb3BlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn19XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3ApFe4kwkAsmRE97TFwYCYv7Rc4w) | [Preview](https://nowonlikeus-git-kwonseop-ask-candidate-scope-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T11:38:11.329Z">Oct 6, 2026 11:38am UTC</relative-time> |

- 정우성(@wo0oo) · 2026-10-06 13:45

  > 1. 질문 결과가 내 상황을 안 거름.
  > 원룸 체크하고 "분리수거 언제 해야돼?" 하고 물으면 기숙사 카드가 나옴. 원룸 카드는 안 나옴.
  > - 프로필 오면 lib/matching.ts에서 matchesProfile로 먼저 거르고 찾게 해주삼.
  > - 내가 질문할때 차량/반려동물/학생 여부고 같이 보내도록 PR 올림. 이거 3개는 거르는 데 만 쓰고 저장하거나 외부 전송은 ㄴㄴㄴ
  > - matchesProfile이 Profile을 받아서 { ...profile, zone: '' } 처럼 넘기면 됨. 3개가 안 오면 false로 두면 조건없음이랑 같게 동작함.
  > 
  > 2. 후보를 "내 상황에 맞는 할 일 전체"로 넓히는 게 나을듯. 키워드 상위 3개로 묶으면 키워드 안 맞을 때 AI가 보질못함. "쓰레기봉투 어디서 사요?" 질문하면 후보가 0개 나오고 종량제봉투를 못 찾음. 1번으로 거른 전체를 AI한테 주면 말 달라도 찾을 수 있고 할일 데이터는 공개 정보라 구글에 가도 문제 없음. #31 로 AI 문장도 안 나가서 숫자 위험 없고 AI 꺼졌을 땐 지금처럼 거른 거 안에서 키워드 검색으로 ㄱㄱ
  > 
  > 3. AI한테 안 쓸 문장을 아직 요구함.
  > #31 부터 answer는 버리는데 lib/gemini.ts가 아직 answer를 required로 받고, 비어있으면 응답을 버림.
  > responseSchema/required/지시문에서 answer 빼고 GeminiAnswer를 { sourceIds, confidence }로, groundAnswer 입력에서도 빼면 됨. 
  > 
  > 1, 2번은 #32 에 같이 넣고 3번은 PR 따로 해도 될듯


---

<a id="pr-33"></a>

### #33 Feat: 질문 시 상황 필터에 필요한 값 함께 전송

- 작성 정우성(@wo0oo) · `useong/ask-profile-filter` → `dev` · 머지 · 올림 2026-10-06 13:46 · 머지 2026-10-06 22:52
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/33

질문할 때 차량·반려동물·학생 여부도 함께 전송. 서버가 질문 결과를 내 상황에 맞는 할 일로만 거르기 위함.

배경
- 지금 /api/ask(#30)는 공개된 할 일 전체에서 찾아서, 원룸 사용자에게 기숙사 전용 카드가 나감 ("분리수거 언제 해요?" → 빛솔재 카드)
- 화면이 받는 카드에는 노출 조건이 없어서 화면에서는 거를 수 없음 → 서버가 거르려면 이 값들이 필요

변경
- lib/types.ts: AskProfile 에 hasCar · hasPet · isStudent 추가, 값별 용도(거르기·저장·외부 전송) 주석
- lib/askView.ts: 질문 시 세 값 함께 전송, 구역은 계속 전송 X
- 세 값은 거르기에만 사용, 저장·외부 전송 X (서버 반영은 권섭 #32)

확인 사항
- vitest 142건 통과 — "보낸 값만으로 목록 화면과 같은 필터 판정" 테스트 추가, 필드를 빼면 실패하는 것 확인
- tsc --noEmit · eslint 통과
- 권섭 #30 · #31 · #32 와 충돌 없음
- 서버가 아직 세 값을 쓰지 않아도 동작에 영향 X (받기만 하고 무시)

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 22:01

#### 코멘트

- @vercel · 2026-10-06 13:46

  > [vc]: #yoKPGoTYAvi/8nAqhG6Vvd6EqBX1Dd3DKcyA0LbNGFU=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9GVGpZc2hBaGJrWmtpamVVUm85SEJqYUZwVnhtIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYXNrLXByb2ZpbGUtZmlsdGVyLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYXNrLXByb2ZpbGUtZmlsdGVyLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/FTjYshAhbkZkijeURo9HBjaFpVxm) | [Preview](https://nowonlikeus-git-useong-ask-profile-filter-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T04:46:49.752Z">Oct 6, 2026 4:46am UTC</relative-time> |

- 김권섭(@kwonseop) · 2026-10-06 22:01

  > ㅇㅋㅇㅋ 확인했어


---

<a id="pr-34"></a>

### #34 Feat: 질문 결과 정리와 다음 사람 돕기 안내 추가

- 작성 정우성(@wo0oo) · `useong/ask-result-polish` → `dev` · 머지 · 올림 2026-10-06 14:04 · 머지 2026-10-06 22:52
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/34

질문 결과 화면을 #31 이후 응답에 맞게 정리하고, 할 일을 모두 끝낸 사람에게 다음 사람을 돕도록 안내하는 화면 추가.

질문 결과 정리
- #31 부터 서버는 근거가 확인되면 늘 같은 고정 문장을 줌 → 그대로 띄우면 GROUNDED · PARTIAL 이 같은 말이 됨
- 신뢰도별 한 줄 설명은 화면이 정하고, 서버 문장은 반복 표시 X
- 결과 제목 "답변" → "결과" (AI 가 답을 쓰지 않으므로)
- 원문 카드 제목에 건수 표시, 목록 화면 묶음 제목과 같은 모양

다음 사람 돕기 안내 (멘토링 피드백 — 일회성 앱 지적 대응)
- 할 일을 모두 끝내면 "모두 끝냈어요. 이제 다음 사람 차례예요" + 질문으로 남기기 버튼
- 연결 대상은 /ask — 주민 답변 화면(/questions)이 생기면 버튼 추가 예정

확인 사항
- vitest 173건 · tsc · eslint · next build 통과
- 브라우저에서 결과 4상태와 전부 완료 상태 확인. 질문은 가짜 응답으로 확인 (실제 /api/ask 는 공용 DB 에 저장돼서 호출 X)
- 열린 PR #32 · #33 과 충돌 없음

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 22:01

#### 코멘트

- @vercel · 2026-10-06 14:04

  > [vc]: #9GM5t76LwzTVjHA7BPgd3Kr3r+HuppGNzd8YTgRbF/Y=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8yeXNDZ0VTSmM0aVU1aGhpcTdjN3pWUGVoOFRLIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYXNrLXJlc3VsdC1wb2xpc2gtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1hc2stcmVzdWx0LXBvbGlzaC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/2ysCgESJc4iU5hhiq7c7zVPeh8TK) | [Preview](https://nowonlikeus-git-useong-ask-result-polish-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T05:04:57.171Z">Oct 6, 2026 5:04am UTC</relative-time> |


---

<a id="pr-35"></a>

### #35 Docs: 구현계획 진행 현황 갱신 (10/6 기준)

- 작성 정우성(@wo0oo) · `useong/docs-status-1006` → `dev` · 머지 · 올림 2026-10-06 14:04 · 머지 2026-10-06 22:52
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/35

구현계획 진행 현황을 10/6 기준으로 갱신.

진행 현황
- Task 4 시드: 17건 PR #22 대기 (DB 에는 먼저 시딩됨)
- Task 7 상세·완료 체크, Task 10 질문 화면 완료로 변경
- Task 9 /api/ask 머지 — 상황 필터·후보 범위는 PR #32 · #33 대기
- Task 11 README · CI · Vercel 연결 완료, master 릴리스 전
- 단위 테스트 54건 → 173건 (dev 에서 직접 실행해 집계)
- 이 표가 9/28 범위(Task 1~11) 기준이고 본선 범위는 따로 진행한다는 점 명시

계획과 실제가 다른 곳 (표에 추가)
- AI 안내 문장 → 서버 고정 안내 (김권섭)
- 기본 모델 gemini-2.5-flash → gemini-3.1-flash-lite (김권섭)

확인 사항
- 문서만 변경
- PR 번호가 들어간 칸은 머지되면 다시 갱신 필요

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-06 22:13

#### 코멘트

- @vercel · 2026-10-06 14:04

  > [vc]: #hLVaoHP8a6gmpk3m9s7xKhg4jwyWGKpOzC+84X5eGGE=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9IdExCZDNWTDRIa2ZDSDRXZmlacGg2UUVrV0p3IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy1zdGF0dXMtMTAwNi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLWRvY3Mtc3RhdHVzLTEwMDYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/HtLBd3VL4HkfCH4WfiZph6QEkWJw) | [Preview](https://nowonlikeus-git-useong-docs-status-1006-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T05:05:23.155Z">Oct 6, 2026 5:05am UTC</relative-time> |

- 김권섭(@kwonseop) · 2026-10-06 22:02

  > PR #22는 이미 병합됨
  > 인증·승격 API와 로그인 화면 PR #36, #38, #39도 이미 병합
  > 현재 dev 테스트 297개
  > 요정도 최신화 하면 될 듯?


---

<a id="pr-36"></a>

### #36 Feat: 회원가입·로그인·로그아웃 API와 세션 가드 추가

- 작성 우희태(@Heetaeeee) · `heetae/auth` → `dev` · 머지 · 올림 2026-10-06 15:20 · 머지 2026-10-06 15:31
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/36

B-auth.md 기준 구현
- lib: authValidation · password · session · auth(가드 getSessionUser · requireUser · requireAdmin)
- API: POST signup · login · logout, GET me
- prisma/seed-admin.ts + npm run seed:admin
- 테스트 3개 파일 47건 통과 (전체 220건 통과)
- 9장 수동 확인 15항목 전부 통과
- Vercel 에 SESSION_SECRET 등록 필요

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 15:30

  > 굳 머지할게


#### 코멘트

- @vercel · 2026-10-06 15:20

  > [vc]: #JrdQeCVO/q55vReiLvC75v2ufWv9w/RJ2xJqIG/9sB4=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy80ZXVvM1ZMdFJrQUJYOGN5N1B1UXVZVmhRN1N0IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtYXV0aC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLWF1dGgtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/4euo3VLtRkABX8cy7PuQuYVhQ7St) | [Preview](https://nowonlikeus-git-heetae-auth-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T06:20:36.695Z">Oct 6, 2026 6:20am UTC</relative-time> |


---

<a id="pr-37"></a>

### #37 Feat: 질문 목록·주민 답변·맞아요 확인 API 추가

- 작성 우희태(@Heetaeeee) · `heetae/qa-api` → `dev` · 닫힘 · 올림 2026-10-06 15:44
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/37

lib/types.ts 의 질문·답변 계약 기준 구현
- GET /api/questions (?status=OPEN|ANSWERED|PROMOTED), 숨김 답변 제외, 맞아요 많은 답변 순
- POST /api/questions/[id]/answers (로그인), 첫 답변 시 OPEN → ANSWERED, 승격된 질문은 409
- POST /api/answers/[id]/confirm (로그인), 중복 클릭은 그대로 반환, 자기 답변은 403
- 확인 요청은 Content-Type: application/json 필요 (본문은 비어도 됨)
- lib/questionView.ts 순수 로직 + 테스트 18건
- 수동 확인 20항목 전부 통과 (테스트 데이터는 확인 후 삭제)

#### 코멘트

- @vercel · 2026-10-06 15:44

  > [vc]: #Z1osxjPz43daRTBZje/O8qL/WciLjyGd39OeBmEYvgw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy81UDZCNXBxVGtSRlpqc21mUFRSZ3pnbURDN0p1IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtcWEtYXBpLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtcWEtYXBpLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/5P6B5pqTkRFZjsmfPTRgzgmDC7Ju) | [Preview](https://nowonlikeus-git-heetae-qa-api-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T06:44:39.396Z">Oct 6, 2026 6:44am UTC</relative-time> |


---

<a id="pr-38"></a>

### #38 Feat: 질문·답변·확인·승격 API (B-community)

- 작성 우희태(@Heetaeeee) · `heetae/promotion` → `dev` · 머지 · 올림 2026-10-06 15:52 · 머지 2026-10-06 19:19
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/38

승격 큐 · 승격 API (ADMIN)
- GET /api/admin/promotions: ANSWERED 질문을 맞아요 합계 순(같으면 오래된 순)
- POST /api/admin/promote: 할 일 발행 + 질문 PROMOTED 를 한 트랜잭션으로, 동시 승격은 409
- 출처(sourceNote) 필수, 기한 0~365 또는 null, 링크 http(s)만, 노출 조건은 정해진 값만
- lib/promotion.ts 순수 로직 + 테스트 20건 (전체 258건 통과)
- 수동 확인 16항목 통과: 승격 직후 조건 맞는 사람의 /api/tasks/match 에 새 할 일 노출, 안 맞는 사람에겐 안 보임
- ⚠️ 질문·답변 API PR(heetae/qa-api) 위에 쌓은 브랜치라 그 PR 먼저 머지 필요
- 승격 초안 /api/admin/promote/draft 는 AI 담당(권섭)

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-06 19:19

  > 승인


#### 코멘트

- @vercel · 2026-10-06 15:52

  > [vc]: #M7RHzARvtVtInvMrrr0W6fFTjYqTJAF7EWqWHIFmJuw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtcHJvbW90aW9uLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvNjJ4bjU5UXlnaHA4Rml0Z3JBRHE3TXNKdWNjQiIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLXByb21vdGlvbi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/62xn59Qyghp8FitgrADq7MsJuccB) | [Preview](https://nowonlikeus-git-heetae-promotion-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T10:14:57.446Z">Oct 6, 2026 10:14am UTC</relative-time> |

- 우희태(@Heetaeeee) · 2026-10-06 16:10

  > B-community.md 기준으로 맞췄습니다.
  > - lib/answerValidation.ts 분리 (validateAnswer · ANSWER_MAX)
  > - lib/promotion.ts: sortQueue · totalConfirmations(answers) · validatePromoteRequest
  > - 질문 목록: GROUNDED 제외, 답변 오래된 순, take 50, _count 로 확인 수
  > - 확인: Content-Type 검사 제외(본문 없음), 403 문구 수정
  > - 승격: 트랜잭션 안에서 조건부 갱신 먼저, 0건이면 404/409 구분
  > - 지침서 테스트 36건 통과 (전체 263건)
  > - 7장 수동 확인 25항목 통과, 테스트 데이터 정리 완료
  > - 질문·답변 PR(heetae/qa-api)의 내용도 이 PR에 포함돼서, 그 PR은 닫아도 됩니다

- 정우성(@wo0oo) · 2026-10-06 16:27

  > 답변이 전부 숨김인 질문도 큐에 들어가고 승격도 됨
  > → promotions 조회 where 와 promote 의 updateMany where 에 answers: { some: { isHidden: false } } 추가
  > 보이는 답변 없으면 기존 409 문구 그대로 나감

- 우희태(@Heetaeeee) · 2026-10-06 19:15

  > 반영 완료
  > promotions 조회 where 와 promote 의 updateMany where 에 answers: { some: { isHidden: false } } 추가
  > 보이는 답변이 없으면 갱신 0건 → 기존 409 "답변이 없는 질문은 승격할 수 없습니다." 그대로
  > 수동 확인: 답변이 전부 숨김인 질문이 큐에 없고, 승격 시 409, 할 일 생성 안 됨 (테스트 데이터 삭제)

- 정우성(@wo0oo) · 2026-10-06 19:17

  > 승인. 숨김 답변 조건 반영 확인
  > - (사소) 추가한 주석 2줄 들여쓰기 어긋남, 다음 수정 때 같이


---

<a id="pr-39"></a>

### #39 Feat: 로그인·가입 화면 추가

- 작성 정우성(@wo0oo) · `useong/login-screen` → `dev` · 머지 · 올림 2026-10-06 15:53 · 머지 2026-10-06 20:14
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/39

답변 · 운영자 화면 전에 필요한 로그인 · 가입 화면 추가. API 는 희태 #36 기준.

화면
- /login · /signup — 질문 화면과 같은 제호 · 뒤로 가기 구성
- 칸 검사는 서버까지 가기 전에 이유를 칸 아래 표시하는 용도, 최종 판정은 서버 error 문장 그대로 노출
- 서버 거절 시 오류 문장으로 초점 이동 (스크린리더 대응), 칸 오류는 첫 오류 칸으로 초점
- 성공 시 ?next= 로 replace 이동 — 뒤로 가기로 로그인 화면 복귀 X
- 비밀번호 보기 체크박스, 브라우저 비밀번호 저장용 autocomplete 지정
- 닉네임 칸에 "실명은 피해 주세요" 안내 — 답변에 닉네임이 공개되므로

판정 로직 (lib/authView.ts)
- safeNext: ?next= 를 사이트 안 경로로만 제한 — https:// · // · /\ · 제어 문자 우회 차단 (오픈 리다이렉트 방지), /login · /signup 으로는 복귀 X
- 한도는 #36 lib/authValidation.ts 상수 그대로 사용, 글자 수 세는 방식(이모지 1자)도 서버와 동일
- 로그인은 비밀번호 길이 검사 X — 가입 규칙이 바뀌어도 옛 계정 로그인 가능

범위 밖
- 로그인 상태 표시 · 로그아웃 버튼 — /questions 작업 때 제호에 추가
- 로그인이 필요한 화면의 진입 차단 — 답변 · 운영자 화면에서 처리

확인 사항
- vitest 254건 · tsc · eslint · next build 통과
- safeNext · 가입 칸 검사에 일부러 버그를 넣은 변이 6종 모두 테스트가 잡아냄
- 실제 API(#36)로 가입 → 이동, 대소문자만 다른 이메일 재가입 409, 틀린 비밀번호 · 없는 이메일 같은 문구, 로그아웃 확인
- 확인용 계정은 공용 DB 에서 삭제 완료

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-06 20:12

#### 코멘트

- @vercel · 2026-10-06 15:53

  > [vc]: #sFptuprg6vD5mh94F99KAz9PN3Wu8voIzZtwZkHW4MI=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9FdFlUbmV4eGFlQk1oZGljajgyeE5jZHdKZUtWIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbG9naW4tc2NyZWVuLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbG9naW4tc2NyZWVuLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/EtYTnexxaeBMhdicj82xNcdwJeKV) | [Preview](https://nowonlikeus-git-useong-login-screen-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-06T06:54:14.369Z">Oct 6, 2026 6:54am UTC</relative-time> |


---

<a id="pr-40"></a>

### #40 Fix: Gemini 응답에서 미사용 answer 제거

- 작성 김권섭(@kwonseop) · `kwonseop/gemini-source-only` → `dev` · 머지 · 올림 2026-10-06 18:39 · 머지 2026-10-07 22:08
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/40

##### 변경 내용

- `GeminiAnswer`에서 사용하지 않는 `answer` 필드를 제거
- Gemini 응답 스키마의 `properties`와 `required`에서 `answer`를 제거
- Gemini 지시문에서 안내 문장 생성 요구를 제거
- Gemini가 `{ sourceIds, confidence }`만 반환하도록 파서를 수정
- `groundAnswer` 입력에서도 `answer`를 제거
- 검증된 근거가 있을 때 API가 반환하는 안내 문장은 기존처럼 서버 고정 문구를 사용하도록 수정
- 관련 테스트와 문서를 현재 동작에 맞게 수정

##### 변경 이유

서버는 PR #31부터 Gemini가 생성한 안내 문장을 사용하지 않고 고정 안내만 반환하고 있는 상태. 하지만 Gemini 응답 스키마에서는 여전히 `answer`를 필수로 요구해, `answer`가 없으면 유효한 근거 선택 결과도 버리고 있었기 때문

이번 변경으로 Gemini는 관련 카드의 ID와 신뢰도만 선택하며, 사용자에게 보여주는 문장은 서버에서만 생성하게 됨

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-07 22:08

  > 승인. 접두어 보정 확인 — 실제 Gemini로 전입신고 · 쓰레기봉투 · 분리수거 모두 GROUNDED + 맞는 카드, 없는 질문은 UNKNOWN


#### 코멘트

- @vercel · 2026-10-06 18:39

  > [vc]: #Vw9I/w5BTfomcRV/kEGdeoFg88+nkG2oQyYDnhOZePY=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1nZW1pbmktc291cmNlLW9ubHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9DY3M0MXFGbWNnZEhka3pwa3NIVjZldnR4UUxZIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1nZW1pbmktc291cmNlLW9ubHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/Ccs41qFmcgdHdkzpksHV6evtxQLY) | [Preview](https://nowonlikeus-git-kwonseop-gemini-source-only-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T11:03:20.621Z">Oct 7, 2026 11:03am UTC</relative-time> |

- 정우성(@wo0oo) · 2026-10-06 20:13

  > - 커밋 작성자 이메일이 kapafe.kw.ac.kr (@ 빠짐) → GitHub 계정이랑 연결 안 됨. git config user.email 고치고 amend 해서 다시 올려줘

- 정우성(@wo0oo) · 2026-10-07 15:50

  > @kwonseop
  > AI 켜면 모든 질문이 UNKNOWN 으로 떨어지고 카드 0개 나옴 (리허설 전에 고쳐야 함)
  > - 지식은 task:{id} 로 보내는데 Gemini 가 sourceIds 에 task: 를 떼고 id 만 돌려줌
  > - 서버 knownIds 는 task:{id} 라 전부 '없는 id' → groundAnswer 가 UNKNOWN 으로 강등
  > - 실측 (gemini-3.1-flash-lite, 원룸 · 월세 후보 10개, DB 저장 없이 askGemini + groundAnswer 직접 호출)
  >   - 전입신고 언제까지 해요? → AI GROUNDED, raw=cmuwaqa4z… (전입신고 카드 맞음) → 검증 후 UNKNOWN []
  >   - 쓰레기봉투 어디서 사요? → AI GROUNDED, raw=cmuwaqbli… → UNKNOWN []
  >   - 분리수거 언제 해요? → AI GROUNDED, raw=cmuwaqb5o… → UNKNOWN []
  >   - 빛솔재에서 고양이 키워도 돼요? → AI UNKNOWN (정상)
  > - 지금은 AI 켜면 키워드 검색(AI 꺼짐)보다 결과가 나쁨
  > 
  > 고치는 법 (둘 중 하나)
  > - 비교 전에 id 맞추기: 접두어 없으면 task: 붙여서 knownIds 와 비교
  > - 지식 줄에서 task: 빼고 id 만 보내고 knownIds 도 id 만
  > 테스트에 'task: 없는 id 를 돌려줘도 인정' 케이스 하나 넣어주면 좋겠음

- 김권섭(@kwonseop) · 2026-10-07 20:09

  > #40 피드백 수정 완료
  > - Gemini가 task:를 뺀 ID를 반환해도, 실제 knownIds에 존재할 때만 task:{id}로 정규화
  > - 존재하지 않는 ID는 기존처럼 폐기
  > - 응답 카드 선택과 DB 저장 모두 정규화된 ID 사용
  > - 회귀 테스트 추가: 기존 코드에서 UNKNOWN + 카드 0개 실패를 확인한 뒤 수정 후 통과


---

<a id="pr-41"></a>

### #41 Feat: 질문 askerId 기록, 답변 authoredByMe, 질문자 닉네임 비공개

- 작성 우희태(@Heetaeeee) · `heetae/ask-asker` → `dev` · 머지 · 올림 2026-10-06 19:09 · 머지 2026-10-07 14:17
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/41

/api/ask 에 질문자 기록 (권섭 확인)
- 로그인 상태면 Question.askerId = user.id, 비로그인은 null
- 세션을 읽지 못해도(비밀키 설정 오류 등) 질문은 막지 않고 null 로 저장
- askerId 는 자체 DB 에만 저장, Gemini 요청에는 포함되지 않음
- tests/ask.test.ts: 저장 데이터 기대값에 askerId 추가, 로그인 · 세션 오류 · 외부 전송 미포함 테스트 3건 추가 (25 → 28)

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-07 14:17

  > 승인. authoredByMe · 질문자 닉네임 비공개 · 지운 계정 쿠키 처리 확인


#### 코멘트

- @vercel · 2026-10-06 19:09

  > [vc]: #aBplGGEVZt5iXL8X/A2u5KEtHehldQBOfjTSihd97E4=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy84U1ZVOTNuVHlOWFRYM3hDbVdHSHJueDFNZldxIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtYXNrLWFza2VyLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtYXNrLWFza2VyLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/8SVU93nTyNXTX3xCmWGHrnx1MfWq) | [Preview](https://nowonlikeus-git-heetae-ask-asker-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T03:33:53.777Z">Oct 7, 2026 3:33am UTC</relative-time> |

- 정우성(@wo0oo) · 2026-10-06 20:12

  > 변경 요청 2건
  > 
  > 1. 지운 계정 쿠키가 남아 있으면 /ask 가 503 남. askerId FK 위반 → catch 로 빠짐. 로그인 없이 쓰는 기능이 막힘
  > → 저장 전에 user 존재 확인, 없으면 askerId null
  > 
  > 2. /api/questions 응답에서 askerNickname 은 null 로 내려줘
  > - 원칙이 "받는 사람은 로그인 없이" → 질문은 원래 익명
  > - 이 PR 부터는 답변하려고 로그인해 둔 사람이 질문하면 닉네임이 붙음. 같은 질문인데 로그인 여부에 따라 공개 범위가 몰래 달라짐
  > - 화면은 askerNickname 안 씀. 운영자 확인용이면 승격 큐(ADMIN)에만 남기기

- 우희태(@Heetaeeee) · 2026-10-06 20:22

  > 반영 완료
  > 1. askerId 저장 전에 계정이 DB 에 있는지 확인, 없으면 null (지운 계정 쿠키가 남아도 질문 200). 테스트 1건 추가 (28 → 29)
  > 2. /api/questions 는 승격 PR(heetae/promotion)에 있어서 거기서 수정했습니다. 공개 목록은 askerNickname 항상 null, 운영자 승격 큐(GET /api/admin/promotions)에서만 닉네임 표시. 테스트 2건으로 교체

- 우희태(@Heetaeeee) · 2026-10-07 12:35

  > 반영했습니다!
  > - AnswerItem 에 authoredByMe 추가 (비로그인 false)
  > - answerSelect 에서 authorId 를 꺼내 toAnswerItem(row, viewerId) 에서 비교만 하고, authorId 는 응답에 싣지 않음
  > - toQuestionItem(row, { viewerId, showAsker }) 로 보는 사람을 답변까지 전달
  > - 답변 작성 응답은 항상 true
  > - 테스트: 내 답변 true / 남의 답변 false(닉네임 같아도) / 비로그인 false / 응답에 작성자 id 없음
  > - #43 확인 요청: 검증 문구 조사를 받침에 맞게 수정 ("출처를 입력해 주세요.", "제목을 ...", "주소는 200자 ...")
  > - 최신 dev 반영, 로컬에서 lint · tsc · test(315) 통과


---

<a id="pr-42"></a>

### #42 Feat: 이웃의 질문 화면과 로그인 상태 표시 추가

- 작성 정우성(@wo0oo) · `useong/questions-screen` → `dev` · 머지 · 올림 2026-10-06 20:06 · 머지 2026-10-07 22:05
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/42

확인된 정보로 답하지 못한 질문에 주민이 답하고 "맞아요"로 확인하는 화면 추가. API 는 희태 #38 · #41 기준.

이웃의 질문 (/questions)
- 탭 3개: 답을 기다려요 · 답이 달렸어요 · 할 일이 됐어요 — 탭이 링크라 주소로 바로 열림, 뒤로 가기 탭 단위
- 질문마다 질문한 사람 상황 표시 ("원룸 · 월세 사는 분의 질문")
- 주민 답변은 "운영자 확인 전" 표시, 할 일 카드와 다른 모양 — 확인된 정보로 오인 방지
- AI 신뢰도 배지는 안 붙임 — "아직 아무도 확인하지 않았습니다"가 바로 아래 주민 답변과 어긋남
- 맞아요: 로그인 시에만, 누른 상태는 ✓ 기호 + 색, 개수는 서버가 다시 센 값 사용
- 내가 쓴 답변은 맞아요 버튼 대신 "내 답변" 표시 + 개수만 (#41 authoredByMe). 닉네임은 겹칠 수 있어 비교 X — 동명이인 계정으로 확인
- 답변 쓰기: 펼침식, 500자(ANSWER_MAX), 공개 · 개인정보 안내, 저장 후 목록에 바로 반영
- 비로그인은 "로그인하고 답하기" → 로그인 후 해당 질문 위치로 복귀
- 할 일이 된 질문은 답변 · 맞아요 X (서버도 409)

로그인 상태
- 모든 화면 제호 오른쪽에 "닉네임 님 · 로그아웃" 또는 "로그인", 로그인 · 가입 화면은 제외
- 확인 전에는 자리만 잡아 둠 — 로그인한 사람에게 "로그인"이 깜빡이지 않게
- 로그인 직후 상태를 새로 읽고 이동

연결 · 안내
- 할 일 목록 하단에 "이웃의 질문에 답하기" 링크
- 질문 결과: 확인되지 않은 질문이면 "이웃의 질문에 올라갔다" 안내 + 그 질문으로 바로 가는 링크 — 모르면 답이 달려도 다시 안 옴
- 할 일 다 끝낸 화면: "이웃의 질문에 답하기"(주) · "질문으로 남기기"(보조)
- 링크로 찾아온 질문(#q-…)은 목록 불러온 뒤 스크롤 · 초점 이동 · 왼쪽 띠 표시 — 목록을 화면이 나중에 불러와서 브라우저 기본 이동이 안 먹음. 로그인 후 복귀도 같은 효과
- 질문 화면 안내 문구: 답하지 못한 질문이 '이웃의 질문'에 공개된다는 사실 추가 (B-community 지침서 9장)

확인 사항
- vitest 352건 · tsc · eslint · next build 통과
- 탭 · 답변 반영 · 맞아요 반영 · 시각 표시(한국 시간) · 답변 칸 · 맞아요 버튼 판정 테스트 37건
- 테스트 계정 · 질문으로 실제 API 확인: 로그인 후 복귀, 맞아요 0 → 1, 빈 답변 안내, 답변 저장, 내 답변 버튼 없음(동명이인 구분), 할 일이 된 질문 버튼 없음
- AI 꺼진 상태로 실제 질문 → 안내 링크 → 해당 질문 이동, 질문 10개 중 맨 아래 질문 스크롤 · 표시 확인
- 테스트 데이터 공용 DB 에서 전부 삭제

참고
- 로컬에서 답변 저장이 3~6초 걸려 트랜잭션 5초 제한에 걸리면 500 — 희태 확인 요청 (코멘트 참고)
- 삭제된 계정의 쿠키가 남은 상태로 답변 · 맞아요 시 500 — 답변 · 확인 API 의 requireUser 는 계정 존재를 확인 안 함 (/ask 는 #41 에서 처리됨)

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-07 15:21

  > API 계약대로 호출하는 것 확인했습니다 (목록 status 탭, 답변 JSON, 맞아요 본문 없음, authoredByMe 로 내 답변 판단). 최신 dev 합쳐서 lint · tsc · test · build 통과 확인. 승인합니다!


#### 코멘트

- @vercel · 2026-10-06 20:06

  > [vc]: #DgHEBcloNHW7aGIyo1bY6u8bGVXDdg76OMO8KR6iLto=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy85UW9ydGVYYnpFQ0RnNHN0ZEVKaVFVVXVxUVR5IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcXVlc3Rpb25zLXNjcmVlbi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLXF1ZXN0aW9ucy1zY3JlZW4td28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/9QorteXbzECDg4stdEJiQUUuqQTy) | [Preview](https://nowonlikeus-git-useong-questions-screen-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T05:27:58.832Z">Oct 7, 2026 5:27am UTC</relative-time> |

- 김권섭(@kwonseop) · 2026-10-06 22:04

  > - GitHub에서 현재 PR 상태가 dirty로 표시됩니다. PR #39 브랜치와 이전 dev를 서로 병합하면서 교차 병합 기록이 생긴 영향으로 보입니다. 최신 dev 위에 질문 화면 커밋을 리베이스해 PR 이력을 정리해 주세요.
  > 
  > - 로그인 사용자는 본인이 작성한 답변에도 “맞아요” 버튼이 표시됩니다. 누르면 서버가 403을 반환하므로, 화면에서 처음부터 숨기거나 비활성화하는 편이 맞습니다. 닉네임은 중복될 수 있으므로 닉네임 비교 대신 API의 AnswerItem에 authoredByMe 같은 값을 추가해 판별하는 방식이 안전합니다.
  > 
  > 이렇다는데 한 번 확인해보면 좋을 것 같아

- 정우성(@wo0oo) · 2026-10-06 23:04

  > @Heetaeeee
  > #42 리뷰에서 권섭이 짚은 거: 로그인하면 내 답변에도 "맞아요" 버튼이 보임 (누르면 403)
  > 닉네임은 중복될 수 있어서 화면에서 비교 X → API 에서 내려줘야 함
  > 
  > AnswerItem 에 authoredByMe: boolean 추가 부탁
  > - lib/types.ts AnswerItem 에 필드 추가 (비로그인이면 false)
  > - questionView.ts: answerSelect 에 authorId 꺼내고, toAnswerItem 에서 viewerId 랑 비교
  >   → authorId 자체는 응답에 내보내지 X (다른 사람 id 노출 방지, confirmedByMe 랑 같은 방식)
  > - 답변 작성 응답(CreateAnswerResponse)은 항상 true
  > - 테스트: 내 답변 true / 남의 답변 false / 비로그인 false
  > 
  > #41 이랑 같은 파일이라 #41 에 같이 넣거나 작은 PR 따로 올려도 됨
  > 들어오면 화면에서 내 답변은 버튼 대신 개수만 보이게 바꿀게

- 우희태(@Heetaeeee) · 2026-10-07 12:35

  > authoredByMe #41 에 반영했어요! questionBoard.test.ts 의 AnswerItem 에 authoredByMe: false 추가 필요합니다

- 정우성(@wo0oo) · 2026-10-07 14:26

  > @Heetaeeee
  > 답변 저장이 로컬에서 3~6초 걸려서 Prisma interactive 트랜잭션 기본 제한(5초) 넘으면 500 남
  > - 서버 데워진 뒤에도 3번 중 1번 실패: 201 3.0s / 201 4.2s / 500 6.1s
  > - 에러: Transaction not found. Transaction ID is invalid, refers to an old closed transaction
  > - 로컬 .env 는 Neon 직접 연결이라 한국 → us-east-2 왕복이 쌓임. 운영(Vercel)은 덜할 수도 있는데 아직 확인 못 함
  > - 승격 발행(/api/admin/promote)도 같은 방식이라 시연 중에 실패할 수 있음
  > 
  > 부탁
  > - $transaction(fn, { timeout: 15000, maxWait: 10000 }) 로 여유 주기 (answers · promote 둘 다)
  > - 답변 저장은 분기 없으니 $transaction([create, updateMany]) 배치로 바꾸면 더 빠름


---

<a id="pr-43"></a>

### #43 Feat: 운영자 승격 화면 추가

- 작성 정우성(@wo0oo) · `useong/admin-promotions` → `dev` · 머지 · 올림 2026-10-06 23:12 · 머지 2026-10-07 22:06
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/43

주민 답변이 달린 질문을 운영자가 확인해 다음 사람의 할 일로 발행하는 화면 추가. API 는 희태 #38 기준.

/admin/promotions
- 로그인 안 했으면 운영자 로그인 링크, 일반 회원이면 안내만 — 실제 권한은 서버(requireAdmin, 역할 DB 재조회)가 판정
- 승격 큐: 맞아요 많은 순, 질문 · 질문자 상황 · 주민 답변 표시
- "확인 수는 순서일 뿐 승격 조건 X" 안내 (승격시스템흐름 7절)

편집기
- 질문 · 주민 답변을 양식 위에 고정 — 쓰는 동안 계속 대조
- AI 초안(/api/admin/promote/draft, 권섭) 먼저 요청, 20초 안에 못 받거나 실패하면 빈 양식 — 승격이 AI 에 막히지 않게
- AI 초안이면 노란 안내, AI 가 채운 기한 칸에 "법정 기한 확인" 경고
- 노출 조건 요약 ("보이는 사람: 기숙사, 반려동물 있음, 학생"), 조건 없으면 "모든 사람" 따로 표시
- 출처는 AI 초안이 있어도 빈칸 — 운영자가 무엇으로 확인했는지 직접 작성
- "공식 자료나 기관에 직접 확인했습니다" 체크 없으면 발행 X (확인되지 않은 데이터는 넣지 않는다)
- 기한 칸에 "14일"처럼 글자가 섞이면 숫자로 추측하지 않고 거절
- 최종 검증은 서버와 같은 validatePromoteRequest 사용 — 규칙 한 곳
- 발행 후 "발행된 할 일 보기" 안내, 다른 운영자가 먼저 발행했으면(409) 큐 새로 보기로 안내

확인 사항
- vitest 373건 · tsc · eslint · next build 통과
- 양식 변환 · 검증 · 노출 조건 요약 테스트 21건
- 테스트 운영자 · 질문으로 실제 API 확인: 로그인 후 복귀, 답변 있는 질문만 큐에 표시, 검증 순서, 발행 → 상세 200, 같은 질문 재발행 409
- 발행된 할 일은 조건 맞는 프로필에만 노출 (기숙사 · 학생 · 반려동물 O / 반려동물 X · 원룸 X)
- 테스트 데이터(할 일 · 질문 · 답변 · 계정) 공용 DB 에서 바로 삭제, 시드 17건 그대로

참고
- #42(이웃의 질문) 위에 쌓은 브랜치 → #42 먼저 머지 필요
- AI 초안 API 는 아직 없어 지금은 항상 빈 양식으로 동작
- 발행도 답변 저장과 같은 트랜잭션 방식이라 로컬에서 5초 제한에 걸릴 수 있음 (#42 코멘트, 희태 확인 요청)

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-07 15:21

  > 승격 큐 · 발행 API 호출 확인했습니다. 화면도 서버와 같은 validatePromoteRequest 를 쓰고, 409/404 는 큐 새로 보기로 처리, 초안 API 가 없어도 빈 양식으로 진행되는 것 확인. #42 먼저 머지 후 머지하면 됩니다. 승인합니다!


#### 코멘트

- @vercel · 2026-10-06 23:12

  > [vc]: #bSyhL6SgK1xR4Nmgdr29E82UJEmBXsi4jvwC8w/7LXw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYWRtaW4tcHJvbW90aW9ucy13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJpbnNwZWN0b3JVcmwiOiJodHRwczovL3ZlcmNlbC5jb20vd28wb29zLXByb2plY3RzL25vd29ubGlrZXVzLzVSOW84bmd0YjV0c2Z5b1hDMnlRRVRtcHBGb3QiLCJwcmV2aWV3VXJsIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1hZG1pbi1wcm9tb3Rpb25zLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/5R9o8ngtb5tsfyoXC2yQETmppFot) | [Preview](https://nowonlikeus-git-useong-admin-promotions-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T05:35:43.972Z">Oct 7, 2026 5:35am UTC</relative-time> |

- 우희태(@Heetaeeee) · 2026-10-07 12:35

  > "출처을(를)" 조사 #41 에서 "출처를 입력해 주세요." 처럼 고쳤어요


---

<a id="pr-44"></a>

### #44 Fix: 답변 저장은 배치 트랜잭션, 승격은 트랜잭션 시간 여유

- 작성 우희태(@Heetaeeee) · `heetae/tx-timeout` → `dev` · 머지 · 올림 2026-10-07 14:36 · 머지 2026-10-07 14:38
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/44

트랜잭션 시간 초과 500 수정 (우성 리뷰)
- 답변 저장: 인터랙티브 → 배치 트랜잭션 $transaction([create, updateMany]) — 분기가 없어 한 번에 전송, 왕복 감소
- 승격 발행: 중간 분기(404/409 판단)가 있어 인터랙티브 유지, { maxWait: 10000, timeout: 15000 } 추가
- 로컬 lint · tsc · test(315) 통과

로컬 측정 (Neon 직접 연결, 한국 → us-east-2)
- 답변 저장 5회: 전부 201, 4.3s / 2.5s / 2.5s / 2.7s / 2.5s (평균 2.9s, 첫 회는 라우트 컴파일 포함)
- 승격 발행 1회: 201, 2.2s
- 수정 전: 3.0s / 4.2s / 6.1s(500), 3번 중 1번 실패
- 테스트 데이터는 측정 후 삭제

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-07 14:38

  > 승인. 답변 배치 트랜잭션 · 승격 시간 여유 확인


#### 코멘트

- @vercel · 2026-10-07 14:36

  > [vc]: #SPBhrQHApnvswCscRlOieg+XNsHs5gtzJX7cmUGMxxw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy80QVJMN0w3alhKUWZMYmhWdjM2RWlaS29pNW5XIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtdHgtdGltZW91dC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLXR4LXRpbWVvdXQtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/4ARL7L7jXJQfLbhVv36EiZKoi5nW) | [Preview](https://nowonlikeus-git-heetae-tx-timeout-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T05:36:38.239Z">Oct 7, 2026 5:36am UTC</relative-time> |


---

<a id="pr-45"></a>

### #45 Style: 전화번호와 하단 링크 터치 영역을 44px로

- 작성 정우성(@wo0oo) · `useong/touch-targets` → `dev` · 머지 · 올림 2026-10-07 15:54 · 머지 2026-10-07 22:18
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/45

360px 화면 점검에서 찾은 작은 터치 영역 수정. CSS 만 변경.

- 할 일 상세 전화번호 링크 26px → 44px — 전화 걸기는 상세 화면의 핵심 동작
- 할 일 목록 하단 링크(질문하기 · 상황 다시 입력하기 등) 26px → 44px
- 글자 크기 · 모양은 그대로, 눌리는 높이만 늘림

확인 사항
- 실제 화면에서 높이 측정 (전화 링크 tel: 동작 그대로)
- 360px 점검: 8개 화면 가로 넘침 없음, 이름 없는 버튼 · 이름표 없는 입력칸 없음, 다크 모드 색은 전부 변수
- vitest 315건 · tsc · eslint · next build 통과

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-07 22:11

#### 코멘트

- @vercel · 2026-10-07 15:54

  > [vc]: #hstex9m5PlTTNJmFLVZvmXAuL44BmTEz+nZnT2ZHSNs=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HWThncmh0Y0R1WEdoaFVrVDR1enY0NTl0YWdMIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctdG91Y2gtdGFyZ2V0cy13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLXRvdWNoLXRhcmdldHMtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GY8grhtcDuXGhhUkT4uzv459tagL) | [Preview](https://nowonlikeus-git-useong-touch-targets-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T06:55:23.967Z">Oct 7, 2026 6:55am UTC</relative-time> |


---

<a id="pr-46"></a>

### #46 Docs: 질문 로그인 · 승격 조건 · AI 역할을 구현에 맞게 정리

- 작성 정우성(@wo0oo) · `useong/docs-sync` → `dev` · 머지 · 올림 2026-10-07 16:01 · 머지 2026-10-07 22:18
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/46

문서가 구현과 어긋난 곳 정리. 본선 발표 · 질의응답에서 문서와 시연이 다르게 보이지 않게.

구현에 맞춘 것
- 질문은 로그인 없이 (익명) — 기획서 5.3 · 설계안 2.1. 답변 · 맞아요만 로그인, 승격은 운영자
- 승격 큐는 확인 수 임계값 없음, 정렬 기준만 — 기획서 3.3 · 5.2 (설계안 · 승격 흐름 문서는 이미 이쪽)
- AI 는 근거 카드만 고르고 문장은 안 씀, 안내는 서버 고정 문구 — 기획서 5.1 · 설계안 1.5 · 3.1 · 3.2 · README · team/README (#31 · #32)

갱신
- 기획서 8절 남은 검증 항목 8개 전부 확인 완료로 체크, 항목별 확인 경로 기재
- 구현계획 현황표 10/7 저녁 기준 — 본선 범위 표(#36 · #38 · #39 · #41 · #42 · #43 · #44 머지, #45 리뷰 중), Task 9 완료(#40 근거 id 보정), 테스트 366건

그대로 둔 것
- 질문 중복 판정 · 신고 · "바뀌었어요" · 질문 상세 화면 — 범위 결정 전이라 문구 유지
- README AI 문장 2곳 — #40 이 고치는 줄이라 겹치지 않게 제외
- 순환 그림의 "[AI 답변]" 칸 — 폭이 바뀌면 그림 정렬이 깨져 본문 설명만 수정

확인 사항
- 최신 dev(#40 · #42 · #43 머지 후)와 충돌 없음

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-07 22:11

#### 코멘트

- @vercel · 2026-10-07 16:01

  > [vc]: #IJ1+NGtcsjhPEburNgb0+6axd/e8SWDzj9D67U6/dq0=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9EWDVtVVFZNUpqMnJ0R2U4elM0c01wV2pLaGt0IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy1zeW5jLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy1zeW5jLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/DX5mUQY5Jj2rtGe8zS4sMpWjKhkt) | [Preview](https://nowonlikeus-git-useong-docs-sync-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T13:15:39.438Z">Oct 7, 2026 1:15pm UTC</relative-time> |


---

<a id="pr-47"></a>

### #47 Chore: dev → master 배포 반영 (본선 — 질문 · 답변 · 승격 순환)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-07 22:21 · 머지 2026-10-08 10:49
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/47

본선(10/8~9) 시연용 배포. 상황 입력 → 할 일 → 질문 → 주민 답변 → 운영자 승격 → 다음 사람 목록 노출까지 한 바퀴.
master 는 dev 에 포함돼 있어 충돌 없이 앞으로만 이동. 스키마 변경 X — 마이그레이션 실행 안 함.

받는 쪽 (9/28 범위)
- /setup 상황 입력 · /tasks 내 할 일 · /tasks/[id] 상세 · 완료 체크 · 진행률 (#17 · #18)
- 시드 17건 — 공식 자료 · 기관 전화로 확인, 전 항목 sourceNote · verifiedAt (#21 · #22)
- 터치 영역 44px, WCAG AAA 색, 다크 모드 (#17 · #45)

질문 (AI)
- /ask 질문 화면 · 신뢰도 배지 · 결과 정리 (#28 · #34)
- /api/ask — 상황 필터 후 후보 선정, AI 실패 · AI 가 모름이면 키워드 검색 (#24 · #25 · #30 · #32 · #33 · #48)
- 키워드 검색 정확도 — 질문 표현 · 한 글자 단어로 엉뚱한 카드가 걸리지 않게 (#48)
- AI 는 근거 카드만 선택, 문장 미사용 · 근거 id 서버 검증 (#31 · #40)
- **운영에서 AI 켬** — 켜졌을 때만 질문 화면에 "Google(Gemini)로 전송" 고지, 대기 문구 "10초쯤" (#49)

로그인 · 주민 답변 · 승격 (본선 범위)
- 가입 · 로그인 · 로그아웃, httpOnly 세션 쿠키 (#36 · #39)
- /questions 이웃의 질문 — 답변 · 맞아요, 내 답변 구분, 질문자 닉네임 비공개 (#38 · #41 · #42)
- /admin/promotions 운영자 승격 — 큐 → 편집 → 발행, 출처 · 직접 확인 체크 필수 (#38 · #43)
- 트랜잭션 시간 초과 대응 (#44)

저장소
- CI (lint · typegen · tsc · test · build) (#19), 설치 시 Prisma generate (#29)
- 문서를 구현에 맞게 정리 · 현황표 (#20 · #35 · #46, 배포 직전 현황표는 별도 문서 PR)

배포 전 확인
- [x] Vercel Production 환경변수: DATABASE_URL · SESSION_SECRET
- [x] AI 운영 적용 결정 → 켬. GEMINI_API_KEY · GEMINI_ALLOW_USER_INPUT=true · GEMINI_MODEL 등록, /ask 외부 전송 고지(#49)
- [x] 운영자 계정 준비
- [ ] 머지 후 운영 URL 에서 한 바퀴 확인

확인 사항
- dev 기준 vitest 381건 · CI 통과
- 각 PR 에서 실제 API · 브라우저로 확인, 테스트 데이터는 공용 DB 에서 삭제

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-08 10:48

#### 코멘트

- @vercel · 2026-10-07 22:21

  > [vc]: #NvB3s4q98Yujxj6x5g78lwH3cnCkv8VzI25ftzQMp3c=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8yUVFNTVgxUjg4bnBqZlYzeEh4UHZFd2JUQU1MIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/2QQMMX1R88npjfV3xHxPvEwbTAML) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T01:46:56.935Z">Oct 8, 2026 1:46am UTC</relative-time> |


---

<a id="pr-48"></a>

### #48 Fix: 질문 검색 정확도와 AI 폴백 결과 개선

- 작성 김권섭(@kwonseop) · `kwonseop/ask-search-quality` → `dev` · 머지 · 올림 2026-10-07 23:18 · 머지 2026-10-08 00:25
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/48

##### 변경 내용

- `어떻게`, `해야`, `하나요` 등 일반적인 질문 표현을 검색 키워드에서 제외
- 조사와 문장부호가 붙은 질문도 주요 키워드를 정상적으로 찾도록 처리
- 서술부와 한 글자 키워드를 약한 표현으로 구분
- 한 글자 키워드만 일치한 카드는 검색 결과에서 제외하고, 다른 조건이 같은 경우의 마지막 순위 비교에만 사용
- 검색 점수가 같으면 제목에 주요 키워드가 일치하는 카드를 우선하도록 수정
- AI 근거 검증 결과가 `UNKNOWN`이면 키워드 검색으로 전환하도록 변경
- AI가 선택한 카드 순서를 유지하고 최대 3개만 응답·저장하도록 제한
- 로그인 사용자의 `askerId` 저장 및 외부 미전송 규칙을 문서에 맞게 반영

##### 확인한 사례

- `인터넷 설치 하려면 어떻게 해야 하나요` → 관련 없는 카드 없음
- `고양이 등록 어디서 하나요` → 월세 세액공제 카드 없음
- `확정일자는 왜 받아야 돼요` → 확정일자 카드 우선
- `차` → `주차`가 부분 일치하는 카드 없음
- AI가 존재하지 않는 근거를 반환하면 키워드 검색으로 전환
- AI가 여러 근거를 반환해도 선택 순서대로 최대 3개만 표시

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-08 00:24

  > 승인. 실제 시드로 전후 비교 — 엉뚱한 카드 제거, 시연 질문(전입신고 · 음식물 · 큰 가구 등) 결과 그대로
  > - (참고) '주민센터 전화번호' 는 전 3개 → 후 0개. 두 단어 중 '주민센터'만 본문에 걸리고 제목엔 없어서 걸러짐. AI 켜면 AI 가 찾을 테니 막지는 않음


#### 코멘트

- @vercel · 2026-10-07 23:18

  > [vc]: #nnHRRV+hZPmIoWSHAR9Af71JL3jWXYpnUcxaQv8o36E=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stc2VhcmNoLXF1YWxpdHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HQnFKc3VOVTdhaUxQcFhUQXo5azhuTGh3Rkc0IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stc2VhcmNoLXF1YWxpdHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GBqJsuNU7aiLPpXTAz9k8nLhwFG4) | [Preview](https://nowonlikeus-git-kwonseop-ask-search-quality-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T14:18:48.018Z">Oct 7, 2026 2:18pm UTC</relative-time> |


---

<a id="pr-49"></a>

### #49 Feat: AI를 켜면 질문 화면에 외부 전송 안내 표시

- 작성 정우성(@wo0oo) · `useong/ai-notice` → `dev` · 머지 · 올림 2026-10-08 00:03 · 머지 2026-10-08 09:04
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/49

운영에서 AI 켜기로 결정 → 질문이 Google 로 나간다는 사실을 제출 직전에 고지.

- 스위치(GEMINI_ALLOW_USER_INPUT=true) + 키가 둘 다 있을 때만 "Google(Gemini)로 전송" 문구 표시 — 서버 /api/ask · askGemini 와 같은 조건 (sendsQuestionsToGoogle, 테스트 8건)
- 꺼져 있으면 기존 문구 그대로 — 전시 후 꺼도 틀린 고지 안 남음
- AI 켜져 있으면 대기 문구에 "10초쯤 걸릴 수 있음" — 응답 7~13초
- app/ask/page.tsx 는 서버에서 요청 시점에 스위치를 읽어 넘김(connection()), 화면은 components/AskScreen.tsx 로 이동
- 대체 결과 문구 "확인된 답을 찾지 못했습니다" — #48 이후 AI 가 모름이라 판단한 경우도 같은 화면이라 "자동 답변 불가" 문구가 안 맞음

확인 사항
- next build 결과로 켬 / 스위치 끔 / 키 없음 세 상태 확인 — 문구는 켬일 때만
- AI 켜고 실제 질문: "쓰레기봉투 어디서 사요?" → 11.4초 → 확인된 정보 + 종량제봉투 카드
- vitest 374건 · tsc · eslint · next build 통과, 테스트 질문 삭제

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-08 01:29

#### 코멘트

- @vercel · 2026-10-08 00:03

  > [vc]: #hyjuD267WvfDz7niNPay282ct1b2HQiR73g88LaKaBM=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy81bzZRWGlHOFB3ZDlrVHJUR0xQZUxrdUxUaUI2IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYWktbm90aWNlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctYWktbm90aWNlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/5o6QXiG8Pwd9kTrTGLPeLkuLTiB6) | [Preview](https://nowonlikeus-git-useong-ai-notice-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-07T15:40:11.184Z">Oct 7, 2026 3:40pm UTC</relative-time> |


---

<a id="pr-50"></a>

### #50 Docs: 배포 직전 현황표 갱신 (#45 · #48 · #49)

- 작성 정우성(@wo0oo) · `useong/docs-release` → `dev` · 머지 · 올림 2026-10-08 10:40 · 머지 2026-10-08 10:46
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/50

배포(#47) 직전 현황표 맞춤. 문서만 변경.

- Task 7 — #45 머지 반영
- Task 9 — #48 (검색 정확도 · AI 모름이면 키워드 검색), 운영에서 AI 켜기로 결정 · 고지 #49
- 단위 테스트 381건 (dev 기준 직접 집계)

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-08 10:46

#### 코멘트

- @vercel · 2026-10-08 10:40

  > [vc]: #RQDlvvgghlXFGwl4t5/BgixG+dWjn3N4P271aFygzGQ=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9FTDZTVnYzd1dNeEFGakVGcWUyMkxzOHo5cFBCIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy1yZWxlYXNlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy1yZWxlYXNlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/EL6SVv3wWMxAFjEFqe22Ls8z9pPB) | [Preview](https://nowonlikeus-git-useong-docs-release-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T01:41:15.063Z">Oct 8, 2026 1:41am UTC</relative-time> |


---

<a id="pr-51"></a>

### #51 Feat: 서비스 소개 표지화면 추가

- 작성 정우성(@wo0oo) · `useong/cover` → `dev` · 머지 · 올림 2026-10-08 11:21 · 머지 2026-10-08 11:26
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/51

`/` 에 서비스 표지 추가. 전시 · QR 로 처음 들어온 사람이 입력 양식부터 보지 않게, 무슨 서비스인지 먼저 보여줌.

표지 (/)
- 누구든 항상 표지에서 시작 — 기존 자동 이동(/setup · /tasks) 대신
- 큰 제목 "월계1동에 처음 왔나요?" + 한 줄 소개 (집 형태 · 계약 형태만 → 해당 할 일만 기한과 함께)
- 분류 띠 행정 · 쓰레기 · 주거 · 생활 — 할 일 목록 색띠와 같은 색, 글자로도 구분
- 시작 버튼: 처음이면 "내 할 일 받기" → /setup, 상황 입력했으면 "내 할 일 보기" → /tasks (같은 자리 · 크기라 흔들림 X)
- "회원가입 없이 바로 시작, 상세 주소 안 받음" 안내
- "먼저 와 본 사람이라면" → 이웃의 질문에 답하기 (주는 쪽 입구)
- 톤은 기존 화면과 동일 (공공 에디토리얼, 색은 기존 변수만 — 다크 모드 그대로)

문서
- 설계안 2.4 화면 목록의 / 설명 갱신

확인 사항
- 처음 온 사람 / 상황 입력한 사람 두 상태 브라우저 확인
- 360px 가로 넘침 X, 제목 두 줄, 버튼 44px 이상
- vitest 381건 · tsc · eslint · next build 통과

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 11:22

#### 코멘트

- @vercel · 2026-10-08 11:21

  > [vc]: #EQNbeZ+/lWjjjAH+K2OIYbmGlqQEkAZQiOeJYEmeBOw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy81S3hmVDFlQWVoakFVTG1iVFZTRVBtdll0cmppIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctY292ZXItd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1jb3Zlci13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/5KxfT1eAehjAULmbTVSEPmvYtrji) | [Preview](https://nowonlikeus-git-useong-cover-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T02:21:42.951Z">Oct 8, 2026 2:21am UTC</relative-time> |


---

<a id="pr-52"></a>

### #52 Docs: 심사 · 외부 공개용으로 README 재작성

- 작성 정우성(@wo0oo) · `useong/readme` → `dev` · 머지 · 올림 2026-10-08 11:25 · 머지 2026-10-08 11:26
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/52

심사위원 · 외부 사람이 처음 보는 README 로 재작성. 위에서부터 읽는 순서로 배치.

구성
- 한 줄 소개 + 서비스 바로가기(운영 URL) + 30초 요약
- 풀려는 문제 → 어떻게 동작하나(순환 그림을 실제 동작에 맞게 다시 그림) → 주요 기능 표(처음 온 사람 · 주민 · 운영자)
- 무엇이 다른가 → 믿을 수 있게 만든 장치(원칙 4개 + 오정보 방지 표) → 직접 조사한 데이터 17건
- 기술 · 구조 그림 · 접근성 → 개발 관리(PR · CI · 테스트 381건 · 커밋 규칙) → 직접 실행하기
- 프로젝트 구조 · 문서 · 일정 · 팀

바로잡은 것
- "구현 진행 중" 상태 문구 → 본선 배포 완료
- 아직 없는 기능(신고 · "바뀌었어요" 갱신 요청)은 "예정"으로 표시 — 있는 것처럼 쓰지 않음
- 출처 설명: 전화 확인 기관은 노원구청 자원순환과 · 빛솔재 행정실 (주민센터는 홈페이지 확인)
- "구역만 넣으면" 등 옛 표현, 환경 변수(SESSION_SECRET · ADMIN_* 추가), 실행 방법(seed:admin), 프로젝트 구조

다음
- 화면 스크린샷은 표지(#51) 배포 후 운영 화면으로 별도 PR

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 11:26

#### 코멘트

- @vercel · 2026-10-08 11:25

  > [vc]: #bPCkeBAFRT1O6Td+e5NecgvF6hGpIjm3tSwCdIjMl+Y=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9DdGU4YlRkeVNEcENBcHp0ZlhFcms5S3hVUTdSIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcmVhZG1lLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcmVhZG1lLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/Cte8bTdySDpCApztfXErk9KxUQ7R) | [Preview](https://nowonlikeus-git-useong-readme-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T02:25:53.635Z">Oct 8, 2026 2:25am UTC</relative-time> |


---

<a id="pr-53"></a>

### #53 Chore: dev → master 배포 반영 (표지 · README)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-08 11:27 · 머지 2026-10-08 11:30
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/53

본선 배포(#47) 이후 추가분 배포. 표지와 README.

- `/` 서비스 소개 표지 — 기존 자동 이동 대신 항상 표지에서 시작. 처음이면 "내 할 일 받기", 입력했으면 "내 할 일 보기" + 이웃의 질문 입구 (#51)
- README 심사 · 외부 공개용 재작성 (#52)
- 설계안 화면 목록의 / 설명 갱신 (#51)

변경 파일 4개 (README · app/page.tsx · app/globals.css · docs/설계안.md). 스키마 · 환경 변수 변경 X.

확인 사항
- dev 와 충돌 없음 (master 에만 있는 커밋은 #47 머지 커밋 하나)
- 표지: 처음 온 사람 / 상황 입력한 사람 두 상태, 360px 폭, 버튼 44px 이상 확인
- 머지 후 운영 URL 에서 표지 확인

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 11:30

#### 코멘트

- @vercel · 2026-10-08 11:27

  > [vc]: #I+MPsWjtqvPCeHAtKq2q73rIEC1FHPzJMXo/uyslAwg=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HR0RnYXBYWW1HallyeVAzcDV1YjQyaWQ4Znl3IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GGDgapXYmGjYryP3p5ub42id8fyw) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T02:27:57.185Z">Oct 8, 2026 2:27am UTC</relative-time> |


---

<a id="pr-54"></a>

### #54 Docs: README에 오픈소스 · 출처 절 추가

- 작성 정우성(@wo0oo) · `useong/readme-credits` → `dev` · 머지 · 올림 2026-10-08 15:31 · 머지 2026-10-08 15:32
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/54

심사 규정 "라이선스 준수 및 README 출처 명시" 대응. 코드 변경 X.

- README 맨 끝에 「오픈소스 · 출처」 절 추가
- 라이브러리 10종 표 — 용도 · 라이선스 (MIT / Apache-2.0 / BSD-3-Clause / OFL)
- 외부 서비스 — Gemini API(카드 id 선택만), Vercel, Neon
- 데이터 출처 — seed-data.ts sourceNote 17건의 기관 목록 + 10/2 전화 확인 2곳
- 로고 출처는 로고 PR 때 추가

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 15:32

#### 코멘트

- @vercel · 2026-10-08 15:31

  > [vc]: #J/kSO7s8UwBRGih9upe6TCuWLQ4tQo++hertS/oOzVU=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9BcXVoQ1BkWkMybU1rRnYzSG15bWN2SlgzRkdiIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcmVhZG1lLWNyZWRpdHMtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1yZWFkbWUtY3JlZGl0cy13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/AquhCPdZC2mMkFv3HmymcvJX3FGb) | [Preview](https://nowonlikeus-git-useong-readme-credits-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T06:31:25.155Z">Oct 8, 2026 6:31am UTC</relative-time> |


---

<a id="pr-55"></a>

### #55 Feat: 서비스 로고 적용과 표지 디자인 개편

- 작성 정우성(@wo0oo) · `useong/logo` → `dev` · 머지 · 올림 2026-10-08 16:06 · 머지 2026-10-08 16:08
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/55

용민 최종 로고(nowonlikeus_logo_fixed.svg) 서비스 전체 적용 + 표지 디자인 개편.

**로고**
- public/logo.svg — 원본 그대로 (글자까지 패스, 투명 배경)
- 집 아이콘 — 원본에서 글자 영역 잘라 정사각형으로 (public/logo-mark.svg, app/icon.svg)
- 파비콘 16/32/48, apple-icon 180 재생성
- 제호 — 집 아이콘 + 표지(/) 링크, 누를 자리 44px
- README — 맨 위 로고, 출처 절에 로고 제작 한 줄

**표지 개편 (시안 기준)**
- 위 칸 — 은은한 그라데이션 + 흐린 집 로고 배경, 위치 라벨, "처음 왔나요?" 초록 강조, 아이콘 붙은 분류 이름표, 화살표 버튼
- 아래 칸 — "막혔던 걸 물어본 이웃이 있어요." + 답을 기다리는 질문 카드 3장
- 질문 카드는 실제 OPEN 질문 (`/api/questions?status=OPEN`). 지어낸 예시 X, 없으면 목록 자리 통째로 숨김
- 질문자 닉네임 · 얼굴 그림 X — 사람 모양 아이콘만 (#41 방침 유지)
- 표지만 폭 1080px, 다른 화면 640px 그대로. 제호 줄은 공용이라 그대로

**확인**
- 320 / 360 / 390 / 414 / 768px — 가로 스크롤 X, 제목 두 줄, 누를 자리 44px 이상
- 720~900px — 집 그림이 글자 뒤로 겹쳐서 휴대폰처럼 오른쪽 위 · 흐리게 처리
- tsc · eslint · vitest 381건 통과
- 실제 기기 · 다크 모드 화면 확인은 아직 X — 미리보기 URL로 확인 예정

#### 리뷰

- **승인** — 박용민(@parkyongminn) · 2026-10-08 16:07

#### 코멘트

- @vercel · 2026-10-08 16:06

  > [vc]: #D10sOYd5PM+grkmo7LbDUEwM93INuVb0/liZ219Bgq0=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9IY2IxWkREWVliWkdMNVV0TXExUGlLdVl1am5LIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbG9nby13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLWxvZ28td28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/Hcb1ZDDYYbZGL5UtMq1PiKuYujnK) | [Preview](https://nowonlikeus-git-useong-logo-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T07:06:55.674Z">Oct 8, 2026 7:06am UTC</relative-time> |


---

<a id="pr-56"></a>

### #56 Chore: dev → master 배포 반영 (로고 · 표지 개편 · README 출처)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-08 16:08 · 머지 2026-10-08 16:10
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/56

#53 이후 추가분 배포. 로고 · 표지 개편 · README 출처. 10/9 07:00 아카이브 전 반영용.

- 서비스 로고 적용 — 파비콘 · apple-icon · 제호 집 아이콘 · README 맨 위 (#55)
- 표지 디자인 개편 — 그라데이션 · 흐린 집 배경, 분류 이름표 아이콘, 답을 기다리는 실제 질문 카드 3장 (#55)
- README 「오픈소스 · 출처」 절 — 라이브러리 라이선스, 외부 서비스, 데이터 출처, 로고 제작 (#54, #55)

변경 파일 9개 (README · app/page.tsx · app/globals.css · components/Masthead.tsx · 아이콘 · 로고 SVG). 스키마 · 환경 변수 변경 X.

확인 사항
- dev 와 충돌 없음 (master 에만 있는 커밋은 #47 · #53 머지 커밋)
- #55 CI · Vercel 미리보기 통과
- 머지 후 운영 URL 에서 표지 · 파비콘 확인

#### 리뷰

- **승인** — 박용민(@parkyongminn) · 2026-10-08 16:10

#### 코멘트

- @vercel · 2026-10-08 16:08

  > [vc]: #vlu1qTNOr6VEOq8dqprQ+wUe/5r2xZXyCMjHhDdvI60=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9BR1VrUkI2elR2TXl6bXlaa0NCUzdLYmE2NTNkIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/AGUkRB6zTvMyzmyZkCBS7Kba653d) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T07:08:55.971Z">Oct 8, 2026 7:08am UTC</relative-time> |


---

<a id="pr-57"></a>

### #57 Fix: 폴백 검색 정확도 개선

- 작성 김권섭(@kwonseop) · `kwonseop/search-fallback-precision` → `dev` · 머지 · 올림 2026-10-08 16:25 · 머지 2026-10-08 17:32
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/57

##### 변경 내용

- 폴백 검색에서 `방법`을 일반 질문어로 처리했습니다.
  - `와이파이 설치 방법 알려주세요`
  - `계약서 작성 방법`
  
  위 질문에서 음식물쓰레기·대형폐기물 카드가 노출되던 문제를 해결했습니다.

- 쉼표와 가운데점으로 붙인 검색어도 각각 분리하도록 수정했습니다.
  - `전입신고,확정일자`
  - `전입신고·확정일자`

- 실제 시드 데이터를 사용한 회귀 테스트를 추가했습니다.
  - 일반어만 일치하는 결과 제외
  - 유효한 다른 키워드가 있는 경우 기존 카드 검색 유지
  - `방법`이 제목에 포함된 정상 카드 검색 유지
  - 쉼표·가운데점으로 나열된 검색어 처리

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-08 17:32

#### 코멘트

- @vercel · 2026-10-08 16:25

  > [vc]: #IfI4+YuLWxOdHanwDKA+adPWoCmp2Fsh++fTWsZgLYo=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1zZWFyY2gtZmFsbGJhY2stNTdiNTlkLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvSkFGeWVtWXBGRTVBcUtac3k0Ykg3djVadVViQSIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQta3dvbnNlb3Atc2VhcmNoLWZhbGxiYWNrLTU3YjU5ZC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCJ9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/JAFyemYpFE5AqKZsy4bH7v5ZuUbA) | [Preview](https://nowonlikeus-git-kwonseop-search-fallback-57b59d-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T07:25:24.915Z">Oct 8, 2026 7:25am UTC</relative-time> |


---

<a id="pr-58"></a>

### #58 Fix: D-day 한국 날짜 기준 계산, 운영자 질문 삭제·답변 숨김 API, 지운 계정 401

- 작성 우희태(@Heetaeeee) · `heetae/review-fixes` → `dev` · 머지 · 올림 2026-10-08 16:57 · 머지 2026-10-08 17:33
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/58

프로젝트 점검에서 나온 백엔드(B) 항목 정리.

##### D-day 한국 날짜 기준
- 서버(Vercel)가 UTC 라 한국 새벽 0~9시에 "오늘"이 어제로 잡혀 남은 날짜가 하루 많게 나오던 문제
- lib/dday.ts: 오늘을 Asia/Seoul 날짜로 자름(seoulDay). 한국 새벽 · 자정 경계 테스트 추가 (옛 코드에선 실패 확인)

##### 운영자 정리 API (ADMIN, role DB 재조회)
- DELETE /api/admin/questions/[id] — 질문 삭제, 답변 · 맞아요 같이 삭제(CASCADE). PROMOTED 는 409, 없으면 404
- PATCH /api/admin/answers/[id] { isHidden: boolean } — 답변 숨김 · 되돌리기
  - 보이는 답변이 없어지면 ANSWERED → OPEN, 되돌리면 OPEN → ANSWERED, PROMOTED 는 그대로
  - 응답 { answerId, isHidden, questionStatus }
- 마이그레이션 없음 (Answer.isHidden 기존 필드 사용)
- 타입: DeleteQuestionResponse · HideAnswerRequest · HideAnswerResponse, 버튼 판정용 canDeleteQuestion (lib/moderation.ts)

##### 계정 확인 · 맞아요
- requireUser 가 DB 에서 계정 존재 확인 → 지운 계정 쿠키면 500 대신 401 + 쿠키 삭제 (requireAdmin 도 같은 함수 사용)
- 할 일로 정리된 질문의 답변에 맞아요 → 409 (답변 작성과 같은 규칙)

##### 시드
- 전부 지우고 새로 만들기 → 제목으로 찾아 갱신. 다시 시딩해도 할 일 id 유지 (완료 체크 · 링크 · sourceIds 안 끊김)
- 삭제는 마지막에 → 중간 실패해도 목록이 비지 않음. 시드 제목 중복 검사 테스트

##### 일부러 안 한 것
- 요청 횟수 제한: 전시장 와이파이는 여러 명이 IP 하나를 써서 IP 제한이 관람객을 막고, Vercel 은 인스턴스가 나뉘어 메모리 제한 효과가 약함

##### 확인
- lint · tsc · vitest 408건 · next build 통과
- 로컬 서버 + 실제 DB 로 21개 시나리오 확인 (숨김 → 목록에서 빠짐 · 상태 OPEN, 되돌리기, 회원 403, 삭제 후 404, PROMOTED 삭제 · 맞아요 409, 지운 계정 401 + 쿠키 삭제). 테스트 데이터 전부 삭제

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-08 17:33

#### 코멘트

- @vercel · 2026-10-08 16:57

  > [vc]: #ns6DnJoBv1lxCDlWi4kCssJLBm6V9OMrKOh8p3rMzI0=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtcmV2aWV3LWZpeGVzLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvQ1JubnRTcmNWaEdpRXJGR2p6RDhFSFpweHlFSCIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLXJldmlldy1maXhlcy13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCJ9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/CRnntSrcVhGiErFGjzD8EHZpxyEH) | [Preview](https://nowonlikeus-git-heetae-review-fixes-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T07:57:55.105Z">Oct 8, 2026 7:57am UTC</relative-time> |


---

<a id="pr-59"></a>

### #59 Feat: 이웃의 질문에 운영자 질문 지우기 · 답변 숨기기 버튼

- 작성 정우성(@wo0oo) · `useong/moderation` → `dev` · 머지 · 올림 2026-10-08 17:42 · 머지 2026-10-08 17:44
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/59

#58 운영자 정리 API 화면 연결. 시연 중 장난 · 욕설 질문을 화면에서 바로 내리기 위함.

- /questions 에 운영자(ADMIN)에게만 정리 버튼
  - 답변 숨기기 → 그 자리에 "숨겼습니다" + 되돌리기 (새로고침 전까지)
  - 질문 지우기 → 같은 자리 확인 칸에서 한 번 더 확인 (브라우저 confirm 창 X)
  - PROMOTED 질문은 지우기 버튼 X (canDeleteQuestion)
- 질문 상태는 서버 응답(questionStatus) 그대로 — 답변 다 숨기면 OPEN
- 401 · 403 이면 세션 다시 읽어 버튼 거둠
- lib/questionBoard: isModerator · withoutQuestion · withAnswerHidden · withAnswerRestored + 테스트 11건

확인
- tsc · eslint · vitest 424건 통과
- 로컬 + 공용 DB, e2e 운영자 · 주민 계정으로 숨기기 · 되돌리기 · 전부 숨김 → OPEN · 지우기 확인. 비로그인 버튼 0개
- e2e 계정 · 질문 · 답변 전부 삭제

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 17:43

#### 코멘트

- @vercel · 2026-10-08 17:42

  > [vc]: #bX++ymx0b982N2dWvxI/C5xJhUNjI1PBW+2vEPRIGu8=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zckIyd3RLdjhpUkFwUExneUdLVUs5WWZOMVJyIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbW9kZXJhdGlvbi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLW1vZGVyYXRpb24td28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3rB2wtKv8iRApPLgyGKUK9YfN1Rr) | [Preview](https://nowonlikeus-git-useong-moderation-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T08:43:20.954Z">Oct 8, 2026 8:43am UTC</relative-time> |


---

<a id="pr-60"></a>

### #60 Chore: dev → master 배포 반영 (D-day · 운영자 정리 · 폴백 검색)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-08 17:44 · 머지 2026-10-08 17:46
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/60

#56 이후 추가분 배포. 점검 지적 대응(D-day · 운영자 정리) + 폴백 검색 개선. 10/9 07:00 아카이브 전 반영용.

- D-day 한국 날짜 기준 계산 — 한국 새벽 0~9시 하루 어긋나던 문제 (#58)
- 운영자 질문 삭제 · 답변 숨김 API, 지운 계정 쿠키 401, 할 일로 정리된 질문 맞아요 409 (#58)
- 시드 다시 실행해도 할 일 id 유지 (#58) — 배포로 시드가 다시 돌지는 않음
- /questions 운영자 질문 지우기 · 답변 숨기기 버튼 (#59)
- 폴백 키워드 검색 정확도 개선 (#57)

변경 파일 20개. DB 스키마 · 환경 변수 변경 X (Answer.isHidden 기존 필드 사용).

확인 사항
- dev 와 충돌 없음 (master 에만 있는 커밋은 #47 · #53 · #56 머지 커밋)
- dev 기준 tsc · eslint · vitest 424건 통과
- 머지 후 운영에서 운영자 계정으로 리허설 질문 2건 정리, 표지 · D-day 확인

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 17:45

#### 코멘트

- @vercel · 2026-10-08 17:44

  > [vc]: #IUD6rpi+HVA6M5K4NRHuUBASDR73UNN20LwL2SSAOLw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy83Tkdub1lUNlI3YzlIcWtkb0VyZnkyUkdNaVF2IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LWRldi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/7NGnoYT6R7c9HqkdoErfy2RGMiQv) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T08:45:03.072Z">Oct 8, 2026 8:45am UTC</relative-time> |


---

<a id="pr-61"></a>

### #61 Feat: 상황 입력 · 할 일 상세 화면에 상단바 추가

- 작성 정우성(@wo0oo) · `useong/setup-masthead` → `dev` · 머지 · 올림 2026-10-08 18:01 · 머지 2026-10-08 18:07
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/61

상단바(로고 · 제호 · 로그인)가 빠져 있던 두 화면에 추가. 이제 모든 화면에 같은 상단바.

- /setup — 상단바 추가, 조건 줄은 비움 (입력 중인 값과 예전 값이 같이 보이면 헷갈림)
  - 제목 "월계는 처음이라" → "지금 상황을 알려 주세요" (상단바 제호와 중복)
- /tasks/[id] — 불러오는 중 · 없는 항목 · 상세 세 상태 모두 상단바 추가
  - 남은 날짜가 이사일로 계산되므로 목록 화면처럼 조건 줄 표시

확인
- tsc · eslint 통과
- 로컬에서 /setup, /tasks/[id] 상세 · 없는 항목 화면 확인

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 18:04

#### 코멘트

- @vercel · 2026-10-08 18:01

  > [vc]: #NovT/0/0sYsuNvflc3yDebd6L9UNyEQQDTQuy5jCozc=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zS0VSRE0zWnlkTDl3ZjhlYjZxYXhOSHd1ekxGIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2Vvbmctc2V0dXAtbWFzdGhlYWQtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1zZXR1cC1tYXN0aGVhZC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3KERDM3ZydL9wf8eb6qaxNHwuzLF) | [Preview](https://nowonlikeus-git-useong-setup-masthead-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T09:02:20.764Z">Oct 8, 2026 9:02am UTC</relative-time> |


---

<a id="pr-62"></a>

### #62 Chore: dev → master 배포 반영 (상황 입력 · 할 일 상세 상단바)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-08 18:07 · 머지 2026-10-08 18:09
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/62

#60 이후 추가분 배포. 상단바가 빠져 있던 두 화면.

- /setup 상단바 추가, 제목 "지금 상황을 알려 주세요" (#61)
- /tasks/[id] 상단바 + 조건 줄 (#61)

변경 파일 2개 (app/setup/page.tsx · app/tasks/[id]/page.tsx). 스키마 · 환경 변수 변경 X.

확인 사항
- dev 와 충돌 없음
- #61 CI 통과 · 승인
- 머지 후 운영 URL 에서 두 화면 상단바 확인

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-08 18:08

#### 코멘트

- @vercel · 2026-10-08 18:07

  > [vc]: #L4so76YCQ0VlkA4ph4qOtdrm9Fv39P22bx/mf7mWL1M=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HZHBEbUFTNzRYdnBLeEJTdGNGbkJoaHZrZjJnIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LWRldi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GdpDmAS74XvpKxBStcFnBhhvkf2g) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T09:07:50.371Z">Oct 8, 2026 9:07am UTC</relative-time> |


---

<a id="pr-63"></a>

### #63 Fix: AI 실패 진단과 질문 API 요청 검증 강화

- 작성 김권섭(@kwonseop) · `kwonseop/ai-api-stability` → `dev` · 머지 · 올림 2026-10-08 20:40 · 머지 2026-10-08 21:57
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/63

##### 변경 사항

- Gemini 키·HTTP·타임아웃·파싱·스키마 실패를 고정된 안전한 분류로 기록합니다.
- 질문·프로필·API 키·응답 본문과 임의 오류 값은 로그에 남기지 않습니다.
- `/api/ask`에서 정확한 `application/json` 요청만 허용하고, 잘못된 본문은 DB·Gemini 접근 전에 거절합니다.
- 올바른 Content-Type을 포함하도록 C 역할 문서의 curl 예시를 수정했습니다.

##### 기존 동작 유지

- Gemini 실패 시 `null`을 반환하고 기존 키워드 검색 폴백을 그대로 사용합니다.
- 정상 요청의 응답 형식과 사용자 화면 문구는 변경하지 않습니다.

##### 검증

- 최신 `dev` 결합 상태 테스트 447개 통과
- `npm run lint` 통과
- `npx tsc --noEmit` 통과
- `npm run build` 통과

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-08 21:56

  > AI 실패 종류만 로그로 남기고 질문·키·응답 본문은 제외하는 것 확인. /api/ask JSON 요청만 허용, 화면은 이미 application/json 보내서 영향 없음. 승인


#### 코멘트

- @vercel · 2026-10-08 20:40

  > [vc]: #1FLaD+ZY1Wrx+C0HyCwRLWKg9kI0aAfYC9KD4mrd8KA=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1haS1hcGktc3RhYmlsaXR5LXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvRExoZzUyVDZ6QU1GZlhjQUZFMlpRaHFZRWtUUiIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQta3dvbnNlb3AtYWktYXBpLXN0YWJpbGl0eS13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCJ9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/DLhg52T6zAMFfXcAFE2ZQhqYEkTR) | [Preview](https://nowonlikeus-git-kwonseop-ai-api-stability-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T11:40:56.213Z">Oct 8, 2026 11:40am UTC</relative-time> |


---

<a id="pr-64"></a>

### #64 Fix: 폴백 검색 동의어와 쓰레기 질문 정확도 개선

- 작성 김권섭(@kwonseop) · `kwonseop/search-synonyms` → `dev` · 머지 · 올림 2026-10-08 21:52 · 머지 2026-10-08 21:57
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/64

##### 변경 사항

- 프로필에 맞는 후보를 먼저 선별한 뒤 키워드 검색을 수행하도록 검증
- 분리수거·재활용·페트병·비닐·스티로폼 등 흔한 표현을 주거형태별 재활용 카드와 연결
- `분리 수거`처럼 띄어 쓴 표현도 동일하게 처리
- 쓰레기 질문의 `버리는` 표현이 대형폐기물 등 관계없는 카드를 끌어오지 않도록 검색 우선순위를 조정
- 소파·침대 등 가구와 전자레인지·드라이기 등 소형가전의 폐기 표현을 연결
- 청소 문맥을 폐기로 오인하지 않도록 대상과 폐기 표현의 관계를 제한
- 검증된 안내가 없는 대형가전 질문은 잘못된 카드를 표시하지 않고 빈 결과로 처리
- 동의어로 확장된 여러 표현은 원래 질문 키워드 하나로 계산

##### 주요 확인 사례

- `분리 수거 언제 해요?`
- `쓰레기봉투 어디서 사요?`
- `음식물 쓰레기 버리는 법`
- `페트병 버리는 날`
- `침대 버리기`
- `전자레인지 버리기`
- `냉장고 버리는 법`
- `소파 얼룩 없애기`

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-08 21:57

  > 시드 17건으로 직접 돌려 확인. 쓰레기봉투·분리 수거·침대/소파·전자레인지 질문이 맞는 카드를 찾고, 음식물·페트병 질문의 엉뚱한 카드가 빠짐. 냉장고 등 대형 가전은 확인된 카드가 없어 빈 결과 — 원칙과 맞음. 기존 전입신고·확정일자 결과 그대로. 승인


#### 코멘트

- @vercel · 2026-10-08 21:52

  > [vc]: #5nm82YULpZ+FY1JRlf+UTkBJO6x1H35QjQTfrDtlVHQ=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1zZWFyY2gtc3lub255bXMtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9FbVhnZGhWdGliMUZBVWpHaTd5S291VGVLQW9BIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1zZWFyY2gtc3lub255bXMtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/EmXgdhVtib1FAUjGi7yKouTeKAoA) | [Preview](https://nowonlikeus-git-kwonseop-search-synonyms-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T12:52:28.898Z">Oct 8, 2026 12:52pm UTC</relative-time> |


---

<a id="pr-65"></a>

### #65 Chore: dev → master 배포 반영 (검색 동의어 · AI 실패 로그)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-08 21:57 · 머지 2026-10-08 21:59
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/65

#62 이후 추가분 배포. 시연 3번 질문 안정화가 핵심. 10/9 07:00 아카이브 · 09:00 시연 전 반영용.

- 폴백 키워드 검색 동의어 · 쓰레기 질문 정확도 (#64)
  - "쓰레기봉투 어디서 사요?" — AI 실패 시 0건 → 종량제봉투 카드
  - 분리수거 · 페트병 → 재활용, 침대 · 소파 → 대형폐기물, 전자레인지 → 작은 가전
  - 냉장고 등 대형 가전은 확인된 카드가 없어 빈 결과
- AI 실패 종류만 로그로 남김(질문 · 키 X), /api/ask 는 application/json 요청만 (#63)
- 상단바: 상황 입력 · 할 일 상세 (#61, #62 로 이미 배포)

변경 파일: lib/search.ts · lib/gemini.ts · app/api/ask/route.ts · 테스트 · team/C-ai.md. 스키마 · 환경 변수 변경 X.

확인 사항
- dev 기준 vitest 505건 통과
- 머지 후 운영에서 "쓰레기봉투 어디서 사요?" 확인

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-08 21:58

#### 코멘트

- @vercel · 2026-10-08 21:57

  > [vc]: #Tpz7DU/NeAA4+j//GPLLvpiJu3bDHcuomsun900nfV8=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zTXJDdE1pdGZGaXh6WXg5VnBjVTJwRGZia3lUIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LWRldi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3MrCtMitfFixzYx9VpcU2pDfbkyT) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T12:58:06.630Z">Oct 8, 2026 12:58pm UTC</relative-time> |


---

<a id="pr-66"></a>

### #66 Docs: AI 초안 · 중복 판정을 다음 단계로 표시하고 테스트 건수 갱신

- 작성 정우성(@wo0oo) · `useong/docs-1008` → `dev` · 머지 · 올림 2026-10-08 22:00 · 머지 2026-10-09 00:51
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/66

아카이브(10/9 07:00) 전 문서를 실제 구현과 맞춤. 코드 변경 X.

- AI 승격 초안 · 질문 중복 판정 → "다음 단계(본선 미구현)" 표시
  - 설계안: AI 역할 문단 아래 안내, 3.3 · 3.4 제목, 흐름도 · 화면 목록의 "AI 초안"
  - 승격시스템흐름 ⑤, 기획서 AI 역할 3번
  - 지금은 새 질문으로 등록되고, 운영자가 빈 양식에서 직접 작성
- 테스트 건수 381 → 505 (README, 구현계획 — 파일별 건수 다시 셈, #63 · #64 포함)

확인
- dev(310a1f4) 기준 vitest 505건 통과

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-08 22:01
- **승인** — 김권섭(@kwonseop) · 2026-10-08 22:04

#### 코멘트

- @vercel · 2026-10-08 22:00

  > [vc]: #6ktHVocwuxm0YyNmwlXORz+xvWXf/DTWYqy1qywje7I=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HZHpLUllMV29mcWtxRFFDZHFaY25QaVhTTDVnIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy0xMDA4LXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy0xMDA4LXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GdzKRYLWofqkqDQCdqZcnPiXSL5g) | [Preview](https://nowonlikeus-git-useong-docs-1008-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T13:01:00.313Z">Oct 8, 2026 1:01pm UTC</relative-time> |


---

<a id="pr-67"></a>

### #67 Feat: 원하는 답이 아니면 이웃에게 다시 묻기

- 작성 김권섭(@kwonseop) · `kwonseop/ask-escalate-to-neighbors` → `dev` · 머지 · 올림 2026-10-08 23:50 · 머지 2026-10-09 01:54
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/67

##### 변경 사항

- 확인된 답이 질문 의도와 다를 때 질문자가 `이웃에게 물어보기`로 질문을 공개할 수 있게 수정
- 로그인 질문은 작성자만 전환할 수 있고, 익명 질문은 응답으로 받은 질문 ID를 이용해 전환
- 이웃 질문 목록에 직접 전환된 질문도 노출하고, 안내 문구와 화면 상태를 실제 동작에 맞춤
- JSON 미디어 타입을 정확히 검사해 다른 사이트의 단순 폼 요청 우회를 막음
- `Question.askNeighbors` 필드와 마이그레이션, 권한·노출·요청 형식 회귀 테스트를 추가
- 
##### 적용 참고

- 배포 전 Prisma 마이그레이션 적용이 필요

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-09 01:54

  > 공용 DB에 마이그레이션(askNeighbors) 먼저 적용 완료 후 승인. 확인됨 답 아래 이웃에게 물어보기, 로그인 질문은 질문자만 · 비로그인은 질문 id 아는 사람만 넘김, 목록은 GROUNDED 제외하되 넘긴 질문 포함. readJsonBody 엄격화는 기존 화면 요청이 모두 application/json 이라 영향 없음 확인. 승인


#### 코멘트

- @vercel · 2026-10-08 23:50

  > [vc]: #LpjTdPp4q7jgUAaK5TlN3Hjq5n1Cc8YPjUM3b7Do3og=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1hc2stZXNjYWxhdGUtdG8tZTdlZWNhLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvNHFQR2ttZTF6VG5WRkZmM2JvZVFKdHZhZFFWMyIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQta3dvbnNlb3AtYXNrLWVzY2FsYXRlLXRvLWU3ZWVjYS13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCJ9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/4qPGkme1zTnVFFf3boeQJtvadQV3) | [Preview](https://nowonlikeus-git-kwonseop-ask-escalate-to-e7eeca-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T14:50:12.606Z">Oct 8, 2026 2:50pm UTC</relative-time> |


---

<a id="pr-68"></a>

### #68 Chore: dev → master 배포 반영 (이웃에게 다시 묻기 · 문서 정리)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-09 01:23 · 머지 2026-10-09 01:57
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/68

#65 이후 추가분 배포. 10/9 07:00 아카이브 · 09:00 시연 전 반영용.

- 원하는 답이 아니면 이웃에게 다시 묻기 (#67)
  - 질문하기 결과가 "확인됨"이어도 카드 아래 "이웃에게 물어보기" → '이웃의 질문'에 공개
  - 로그인 질문은 질문자만, 비로그인 질문은 결과 화면의 질문 id 로만 넘김
  - readJsonBody 가 미디어 타입을 정확히 application/json 으로 판정
- AI 승격 초안 · 질문 중복 판정 "다음 단계(본선 미구현)" 표시, 테스트 건수 갱신 (#66)

**DB 마이그레이션 적용 완료** — `20261008120000_question_ask_neighbors` (Question.askNeighbors, 기본값 false) 를 공용 DB 에 먼저 적용함. 이 배포가 들어가도 스키마 불일치 X.

확인 사항
- dev 기준 tsc · vitest 514건 통과
- 머지 후 운영에서 이웃의 질문 · 표지 미리보기 · 질문하기 "이웃에게 물어보기" 확인

#### 리뷰

- **승인** — 박용민(@parkyongminn) · 2026-10-09 01:57

#### 코멘트

- @vercel · 2026-10-09 01:23

  > [vc]: #ORYSmUdQ4upzEUnB7njsriVjedyUterLEofX6S72yCg=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HNjJ5S1I1MWVjUXc0UFdEbjRiYU1CWmV1cUhvIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/G62yKR51ecQw4PWDn4baMBZeuqHo) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-08T16:55:31.551Z">Oct 8, 2026 4:55pm UTC</relative-time> |


---

<a id="pr-69"></a>

### #69 Feat: 하단 탭으로 할 일 · 물어보기 · 이웃 질문 오가기

- 작성 정우성(@wo0oo) · `useong/bottom-tab-bar` → `dev` · 머지 · 올림 2026-10-10 16:06 · 머지 2026-10-10 20:23
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/69

직접 써 본 사람들이 질문 화면 · 할 일 화면을 찾고 오가는 걸 어려워함. 화면 아래에 늘 붙는 탭 3개로 해결.

##### 원인
- 질문하기 · 이웃의 질문 링크가 할 일 목록 **맨 아래**에만 있음 (`app/tasks/page.tsx`)
- 원룸이면 할 일 10개 → 끝까지 내려야 보임
- 다른 화면은 "← 내 할 일" 하나뿐. 지금 어디 있는지 표시 X

##### 하단 탭 (`components/TabBar.tsx`)
- **할 일 · 물어보기 · 이웃 질문** — 화면 아래 고정, 스크롤과 상관없이 보임
- 지금 화면은 초록 글자 + 위쪽 막대 4px (색만으로 구분 X), `aria-current="page"`
- 할 일 상세(`/tasks/[id]`)에서도 "할 일" 켜짐
- 표지 · 상황 입력 · 로그인 · 운영자 화면에는 안 띄움 — 다음 행동이 하나뿐인 화면
- `layout.tsx` 에서 본문 뒤에 렌더 → 키보드 · 스크린리더가 본문보다 먼저 지나치지 않음. 건너뛰기 링크 불필요

##### 크기 · 접근성
- 탭 높이 64px, 글자 15px 굵게, 아이콘 26px (인라인 SVG, `aria-hidden`)
- 대비: 기본 `--text-soft`, 켜짐 `--accent` — 밝은 · 어두운 모드 모두 AAA
- 아이폰 홈 막대만큼 띄움 — `viewport` 에 `viewportFit: 'cover'` 추가 + `env(safe-area-inset-bottom)`. 확대는 막지 않음
- 탭과 같은 높이의 빈 자리를 본문 끝에 둬서 마지막 카드가 안 가려짐
- 인쇄 시 숨김

##### 정리한 링크 (탭과 중복)
- 할 일 목록 맨 아래 "질문하기", "이웃의 질문에 답하기" 삭제 — "상황 다시 입력하기"는 탭에 없어서 유지
- 물어보기 · 이웃의 질문 화면의 "← 내 할 일" 삭제
- 할 일 상세 · 로그인 · 가입 화면의 "← 내 할 일"은 유지

##### 확인 사항
- `tsc` / `eslint` / Vitest 514건 통과 (UI 변경이라 새 단위 테스트 없음)
- 로컬 390px 폭: 화면별 탭 노출 · 켜지는 탭 · 마지막 링크가 탭 위에 있는지 확인
- 휴대폰(아이폰) 실기기 확인

**시연 대본에 "목록 아래 질문하기 링크"가 있으면 "아래 물어보기 탭"으로 바꿔야 함.**

다음 PR #70(내 질문 탭)이 이 브랜치 위에 쌓여 있음. **이 PR 먼저 머지.**

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-10 19:58

#### 코멘트

- @vercel · 2026-10-10 16:07

  > [vc]: #CegqPKVYGNFCnU8vCdvaunAbavaE4hDKDqYVMZ1uBAo=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6IiJ9LCJpbnNwZWN0b3JVcmwiOiJodHRwczovL3ZlcmNlbC5jb20vd28wb29zLXByb2plY3RzL25vd29ubGlrZXVzL0RqcXJyb2pvNWtGZGdjcW5qUzFEbUVTZFhreVQiLCJwcmV2aWV3VXJsIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1ib3R0b20tdGFiLWJhci13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJQRU5ESU5HIn1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Building](https://vercel.com/static/status/building.svg) [Building](https://vercel.com/wo0oos-projects/nowonlikeus/Djqrrojo5kFdgcqnjS1DmESdXkyT) | [Preview](https://nowonlikeus-git-useong-bottom-tab-bar-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T07:07:04.434Z">Oct 10, 2026 7:07am UTC</relative-time> |


---

<a id="pr-70"></a>

### #70 Feat: 로그인하면 내 질문 모아 보기 · 질문하기 로그인 안내

- 작성 정우성(@wo0oo) · `useong/my-questions` → `dev` · 머지 · 올림 2026-10-10 16:07 · 머지 2026-10-10 20:23
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/70

로그인하면 내가 남긴 질문에 답이 달렸는지 바로 보는 "내 질문" 탭. 질문하기 화면에 로그인 안내도 추가.

**하단 탭 PR #69 위에 쌓인 PR.** 이 PR 커밋은 2개(`f1404fb`, `9e348f7`)만 보면 됨. #69 머지 후 base 를 `dev` 로 변경.

##### API — `GET /api/questions?mine=1`
- 로그인한 사람이 쓴 질문만, 상태 섞어서 최신순. 비로그인 **401** (`requireUser`)
- 조건 `mineWhere(viewerId)` = 이웃의 질문 목록 조건(`boardWhere(null)`) + `askerId`
- 응답 모양은 기존 목록과 같음. 질문자 닉네임은 여기서도 싣지 않음
- **DB 변경 X** — `askerId` 는 이미 `/api/ask` 가 저장 중
- 기존 `?status=` 목록 동작은 그대로

##### 이웃의 질문 화면
- 로그인하면 탭 맨 앞에 **내 질문** (`?status=MINE`). 로그인 여부는 서버에서 세션으로 판단
- 비로그인이 `?status=MINE` 으로 오면 "답을 기다려요" 탭으로
- 카드마다 진행 상태 표시 — 답이 달렸어요(실선) / 답을 기다려요(점선) / 할 일로 정리됨(기존). 색이 아니라 선 모양 · 명도로 구분
- 내 질문 탭에서는 답변 쓰기 칸 X — 답을 보러 오는 곳
- 보는 중 세션이 끝나면 401 → 로그인 안내 + 링크

##### 질문하기 화면
- 비로그인이면 입력칸 위에 안내: "로그인하고 질문하면 이웃이 단 답을 나중에 '내 질문'에서 바로 볼 수 있습니다. 로그인하기"
  - 쓰기 전에 읽히게 입력칸 위. 세션 확인 전에는 안 띄움 (깜빡임 방지)
- 로그인했으면 결과의 "이웃의 질문에서 보기" → **"내 질문에서 보기"** (`onBoardLink`)

##### 내 질문에 안 나오는 것
| 질문 | 이유 |
|---|---|
| 비로그인으로 쓴 질문 | `askerId` 없음. 나중에 로그인해도 안 이어짐 |
| 확인된 정보로 바로 답한(GROUNDED) 질문 | 이웃의 질문 목록에도 안 올라감. "이웃에게 물어보기" 누르면 나옴 |

##### 확인 사항
- `tsc` / `eslint` / Vitest **528건** 통과 (새 테스트 14건 — `parseTab` · `visibleTabs` · `boardUrl` · `mineStateLabel` · `mineWhere` · `onBoardLink`)
- 로컬 서버 + `[e2e]` 계정으로 API 확인
  - 로그인해서 쓴 질문만 나옴, 비로그인 질문 섞이지 않음
  - 비로그인 401
  - 탭 순서 · 켜진 탭 확인
- `[e2e]` 계정 · 질문 삭제 완료 (남은 `[e2e]` 0건)
- 아이폰 실기기 확인

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-10 19:58

#### 코멘트

- @vercel · 2026-10-10 16:07

  > [vc]: #kNOFJMVU3Dy8YSDMMe8vxo71HIVYTRE1Wa94k7BhK3I=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zbUI0UTFoTkRRU0tLNFBmNUNDTUZVV3ZzdlhBIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbXktcXVlc3Rpb25zLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbXktcXVlc3Rpb25zLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3mB4Q1hNDQSKK4Pf5CCMFUWvsvXA) | [Preview](https://nowonlikeus-git-useong-my-questions-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T07:07:40.190Z">Oct 10, 2026 7:07am UTC</relative-time> |


---

<a id="pr-71"></a>

### #71 Feat: 카카오 로그인 추가

- 작성 정우성(@wo0oo) · `useong/kakao-login` → `dev` · 머지 · 올림 2026-10-10 19:57 · 머지 2026-10-10 20:23
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/71

로그인 · 가입 화면에 카카오 로그인 추가. 이메일 로그인은 그대로 둠 (운영자 계정 이메일).

##### 받는 정보
- **카카오 회원번호만.** 동의항목 요청 X → 닉네임 · 이메일 · 전화번호 안 받음
- 카카오 닉네임은 실명인 경우가 많음 → **처음 카카오 로그인 시 이 서비스용 닉네임을 따로 정함** (`/signup/kakao`)
- 카카오 액세스 토큰은 회원번호 읽는 데 한 번만 쓰고 저장 X

##### 흐름 (`lib/kakao.ts`)
| 단계 | 경로 | 내용 |
|---|---|---|
| 1 | `GET /api/auth/kakao?next=` | state(32바이트 난수)를 쿠키에 → 카카오 로그인 화면 |
| 2 | `GET /api/auth/kakao/callback` | state 확인 → 코드로 토큰 → 회원번호. 가입한 번호면 바로 로그인, 처음이면 서명 쿠키(10분) → 닉네임 화면 |
| 3 | `POST /api/auth/kakao/complete` | 닉네임 받아 계정 생성(MEMBER) → 세션 → 시작한 화면으로 |

- 실패 · 취소 · 키 없음 → `/login?kakao=failed|cancelled|unavailable` 로 돌아와 한 줄 안내. 카카오 오류 내용은 화면에 안 실음
- 서버에 `KAKAO_REST_API_KEY` 없으면 버튼 숨김 — Preview 배포에선 버튼 안 보임 (리다이렉트 URI 등록 불가라 일부러)

##### 보안
- state 불일치 · 재사용 거절 (CSRF). state 쿠키는 콜백에서 읽자마자 삭제
- `next` 는 시작 · 콜백 · 완료 모두 `safeNext` 로 다시 거름 (오픈 리다이렉트 X)
- 회원번호는 요청 본문이 아니라 **서버가 서명한 쿠키에서만** 읽음 — 본문의 `kakaoId` · `role` 무시
- 서명 쿠키는 세션과 같은 비밀키라 `audience` 로 구분 — 서로 대신 쓸 수 없음 (테스트 있음)
- 쿠키 코드는 `lib/auth.ts` 한 곳에 (기존 규칙). httpOnly · SameSite=Lax · 경로 좁힘
- 같은 번호로 동시 가입 → unique 위반 잡아서 먼저 만든 계정으로 로그인

##### DB — 마이그레이션 `20261010120000_user_kakao_login`
- `User.kakaoId` 추가 (unique), `email` · `passwordHash` 필수 해제
- 기존 계정 · 데이터 영향 X
- **공용 DB에 이미 적용함** (`prisma migrate deploy`). 적용 후 실서버 주요 화면 · API 200 확인

##### 화면
- 로그인 "카카오 로그인" / 가입 "카카오로 시작하기" — 카카오 디자인 가이드(#FEE500, 검정 말풍선)
- 버튼 아래 "카카오에서는 회원번호만 받습니다" + "또는 이메일로" 구분선
- 닉네임 검사는 이메일 가입과 같은 규칙 (`validateNickname` · `nicknameFieldError` 로 분리)

##### 환경변수
- `KAKAO_REST_API_KEY`, `KAKAO_CLIENT_SECRET` — 콘솔 > 앱 > 플랫폼 키 > REST API 키 (클라이언트 시크릿은 새 키 기본 ON)
- Vercel **Production 에만** 등록함 (Sensitive)
- 콘솔 리다이렉트 URI: `https://nowonlikeus.vercel.app/api/auth/kakao/callback`, `http://localhost:3000/api/auth/kakao/callback`

##### 확인 사항
- `tsc` / `eslint` / Vitest **565건** 통과 (새 37건 — `lib/kakao.ts` 전부, 닉네임 검증, 로그인 화면 판정)
- 로컬에서 시작 · 실패 경로: 버튼 표시 · 카카오 주소 · state 쿠키 속성 · 잘못된/재사용 state · 취소 · 잘못된 코드 · 키 없음 · 닉네임 시간 만료 · 잘못된 닉네임
- **실제 카카오 로그인 확인** (localhost): 첫 로그인 → 닉네임 화면 → 시작한 화면 복귀, 다시 로그인 → 바로 로그인
- 테스트 카카오 계정 삭제 (남은 카카오 계정 0)

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-10 19:58

#### 코멘트

- @vercel · 2026-10-10 19:57

  > [vc]: #zaGONOAkLNdbZT9RjMd0yrVUtVEAXsZUAmwwsApgGAM=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy84dEdCdjJjM2plYVpEdEdLQjhwOGhIRDI0UnZSIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2Vvbmcta2FrYW8tbG9naW4td28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LXVzZW9uZy1rYWthby1sb2dpbi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/8tGBv2c3jeaZDtGKB8p8hHD24RvR) | [Preview](https://nowonlikeus-git-useong-kakao-login-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T10:57:45.840Z">Oct 10, 2026 10:57am UTC</relative-time> |


---

<a id="pr-72"></a>

### #72 Feat: 주민 답변 기반 승격 AI 초안 추가

- 작성 김권섭(@kwonseop) · `kwonseop/promote-ai-draft` → `dev` · 머지 · 올림 2026-10-10 20:14 · 머지 2026-10-10 20:28
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/72

##### 변경 사항
- 운영자 승격 화면에서 사용하는 `POST /api/admin/promote/draft` API를 추가
- 답변이 달린 질문과 숨기지 않은 주민 답변만 Gemini에 전달
- `title`, `why`, `howTo`는 한 주민 답변의 완전한 원문 문장과 일치할 때만 초안에 남김
- 링크·장소·주소·전화번호도 주민 답변에 실제로 있는 값만 허용
- 이사·전입과 직접 연결되고 부정되지 않은 기한만 `dueOffsetDays`로 인정
- 노출 조건은 질문자의 주거·계약 상황 안에서만 제안하며, 차량·반려동물·학생 조건은 AI가 설정하지 않음
- AI 호출 실패, 비정상 응답 또는 외부 전송 스위치 비활성화 시 `draft: null`로 안전하게 전환
- 기존 질문 AI 경로의 응답 계약과 동작은 유지

##### 운영 참고
- `GEMINI_ALLOW_USER_INPUT=true`이고 `GEMINI_API_KEY`가 있을 때만 질문과 주민 답변이 Gemini로 전송됨
- 초안은 자동 저장되지 않으며, 운영자가 공식 자료를 확인하고 출처를 입력해야 발행할 수 있음
- 원문 검증을 통과하지 못한 항목은 빈칸으로 남겨둠

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-10 20:27

#### 코멘트

- @vercel · 2026-10-10 20:14

  > [vc]: #FqG331QG7+MWLSq3fYGRjFGijb5sS2aVk8z4uUTys9Y=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1rd29uc2VvcC1wcm9tb3RlLWFpLWRyYWZ0LXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sImluc3BlY3RvclVybCI6Imh0dHBzOi8vdmVyY2VsLmNvbS93bzBvb3MtcHJvamVjdHMvbm93b25saWtldXMvZDRwR256eFZ5WTh0WHJLUFdwM2I1QnpzcVpUZiIsInByZXZpZXdVcmwiOiJub3dvbmxpa2V1cy1naXQta3dvbnNlb3AtcHJvbW90ZS1haS1kcmFmdC13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCJ9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/d4pGnzxVyY8tXrKPWp3b5BzsqZTf) | [Preview](https://nowonlikeus-git-kwonseop-promote-ai-draft-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T11:14:32.611Z">Oct 10, 2026 11:14am UTC</relative-time> |


---

<a id="pr-73"></a>

### #73 Feat: 동네 인증용 노원구 경계 데이터 추가

- 작성 정우성(@wo0oo) · `useong/neighborhood-badge` → `dev` · 머지 · 올림 2026-10-10 20:42 · 머지 2026-10-10 21:50
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/73

노원구 동네 인증 배지에 쓸 경계 데이터. 판정 로직 · 테스트 · DB · API 는 희태 작업 — 이 파일을 dev 에서 받아 시작하면 됨.

##### 무엇
- `lib/nowonBoundary.ts` 하나 추가 (다른 파일 변경 X)
  - `NOWON_BOUNDARY` — 노원구 외곽선 꼭짓점 301개, **[경도, 위도]** (GeoJSON 순서), 닫는 점 없음
  - `NOWON_BOUNDARY_SOURCE` — 출처 · 시군구코드 11350 · 버전

##### 데이터
- 원자료: 통계청 SGIS 행정동 경계 (공공누리 제1유형)
- 가공본: vuski/admdongkor **ver20260701** (2026-07-01 기준), CC BY 4.0
- 이 저장소 가공: 노원구 행정동 **19개**를 shapely `unary_union` 으로 합침
  - 결과: Polygon 1개, 구멍 · 섬 X, 유효(valid)
  - **단순화 X** — 좌표만 소수 6자리(약 0.1m)로 반올림, 반올림 전후 판정 같은지 확인
  - 범위 약 6.2km × 9.1km, 파일 9.7KB
- **파일 맨 위 출처 표기는 라이선스 조건** — 지우면 안 됨

##### 왜 월계1동이 아니라 노원구
- 할 일 상당수가 노원구 단위 규칙 (쓰레기 요일 · 대형폐기물 · 구청 민원)
- 광운대가 월계1동 남쪽 끝 · 성북구 경계라 GPS 오차로 "밖" 오판이 잦음
- 배지로 드러나는 정보가 더 넓어서 개인 특정이 어려움
- 서비스 대상(월계1동에 처음 온 사람)은 그대로, **인증 범위만** 노원구

##### 원칙 (희태 작업에도 적용)
- 선택 배지 — 답변 · 맞아요 막지 X
- **판정은 브라우저 안에서만.** 좌표는 서버로 보내지 않고 저장도 X. DB 에는 인증 날짜만, 180일 만료

##### 확인 사항
- `tsc` 통과
- 기준점 판정 (지도 기준 근사 좌표)
  - 안: 광운대 정문 · 노원역 · 수락산역 · 태릉입구역
  - 밖: 도봉구청 · 성북구 석관동 · 서울시청

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-10 21:50

#### 코멘트

- @vercel · 2026-10-10 20:42

  > [vc]: #uapw8vMbaBv0lCEmohCpQQUvUT/Bs4mavLv0nHUQaiE=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zZkdIR2V6Mkd3QzdlVGJXRXVLNkJDOUt4d3hoIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbmVpZ2hib3Job29kLWJhZGdlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbmVpZ2hib3Job29kLWJhZGdlLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3fGHGez2GwC7eTbWEuK6BC9Kxwxh) | [Preview](https://nowonlikeus-git-useong-neighborhood-badge-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T11:42:44.423Z">Oct 10, 2026 11:42am UTC</relative-time> |


---

<a id="pr-74"></a>

### #74 Revert "Feat: 동네 인증용 노원구 경계 데이터 추가"

- 작성 우희태(@Heetaeeee) · `revert-73-useong/neighborhood-badge` → `dev` · 닫힘 · 올림 2026-10-10 21:53
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/74

노원구 경계 데이터 확인했습니다. 꼭짓점 301개, 면적 약 35.4㎢로 실제 노원구와 일치하고, 브리프 기준점 7개(광운대 · 노원역 · 수락산역 · 태릉입구는 안, 도봉구청 · 한예종 · 시청은 밖)가 모두 기대대로 판정됩니다. lint · tsc · 테스트 619개 통과했고, 출처 표기도 그대로 있습니다.

#### 코멘트

- @vercel · 2026-10-10 21:54

  > [vc]: #U+/rlFIbBeSh+ZPPXQU2WsqzDM2l9pmF/cLaEAmq7bI=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy82Z1Y1OU5KZ2lNQVJRNDZrSExSanRpNXVKN3c0IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1yZXZlcnQtNzMtdXNlb25nLW5laWdoYm8tZjQ0ZWEzLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1yZXZlcnQtNzMtdXNlb25nLW5laWdoYm8tZjQ0ZWEzLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/6gV59NJgiMARQ46kHLRjti5uJ7w4) | [Preview](https://nowonlikeus-git-revert-73-useong-neighbo-f44ea3-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T12:54:44.147Z">Oct 10, 2026 12:54pm UTC</relative-time> |

- 우희태(@Heetaeeee) · 2026-10-10 21:55

  > Revert 버튼을 잘못 눌러 생긴 PR입니다. #73 은 그대로 유지하고 이 PR 은 닫습니다.


---

<a id="pr-75"></a>

### #75 Feat: 노원 동네 인증 판정 로직과 저장 API 추가

- 작성 우희태(@Heetaeeee) · `heetae/neighborhood-verify` → `dev` · 머지 · 올림 2026-10-10 22:12 · 머지 2026-10-10 22:31
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/75

##### 무엇을
동네 인증 브리프의 판정 로직 · DB · API 부분입니다. 이름과 모양은 브리프 그대로입니다.

- `lib/neighborhood.ts` — `isInNowon`(광선 교차, 경계 위는 안) · `checkPosition`(오차 200m 초과는 `inaccurate`) · `isNeighborhoodVerified`(180일). 서버 코드 import 없음 → 브라우저에서 그대로 사용
- DB — `User.neighborhoodVerifiedAt DateTime?`, 마이그레이션 `20261010200000_user_neighborhood_verified` (nullable 컬럼 하나)
- API — `POST` · `DELETE /api/me/neighborhood`, `/api/auth/me` 에 `neighborhoodVerified`, `AnswerItem.authorNeighborhoodVerified`
- 타입 — `MeResponse.neighborhoodVerified`, `AnswerItem.authorNeighborhoodVerified`, `NeighborhoodResponse`

##### 위치정보 원칙
- 서버는 좌표를 받지도 저장하지도 않습니다. POST 본문은 JSON 형식만 확인하고, 좌표가 실려 와도 버립니다 (테스트로 고정)
- 다른 사람에게는 참 · 거짓만 내려가고 인증 날짜는 내려가지 않습니다 (테스트로 고정)

##### 화면 작업 때 알아 둘 것
- 브라우저 연결: `checkPosition({ lng: coords.longitude, lat: coords.latitude, accuracy: coords.accuracy })` — 경도 · 위도 순서 주의
- 오차 경계: 200m 는 판정, 201m 부터는 안 · 밖 상관없이 `inaccurate`
- 180일 경계: 인증 시각부터 정확히 180일이 되는 순간 false (179일 true · 180일 false · 181일 false)
- 다시 POST 하면 시각이 새로 찍혀 180일이 다시 시작됩니다
- 배지는 답변을 쓴 시점이 아니라 지금 기준입니다
- `lib/useSession.ts` 는 타입만 맞췄습니다(/me 실패 시 기본값에 `neighborhoodVerified: false`). 화면 상태로 꺼내 쓰는 건 화면 작업에서 해 주세요

##### DB 적용
- 팀 공지 후 공용 DB에 `npx prisma migrate deploy` 로 적용 완료했습니다 (migrate dev 아님)
- nullable 컬럼이라 지금 master 코드도 그대로 동작합니다

##### 확인
- lint · tsc · 테스트 662개 통과 (새로 43개: 판정 28 · API 11 · 답변 변환 4)
- 판정: 브리프 기준점 7개, 꼭짓점 301개 전부, 모든 변의 가운데 → 기대대로
- 로컬(공용 DB): `/api/auth/me` false → POST 후 true → DELETE 후 false 로 원상복구

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-10 22:31

#### 코멘트

- @vercel · 2026-10-10 22:12

  > [vc]: #9JIk8W0eesx6gWxX1fOewy1hTSZtjAdkuVoP9dEkqAM=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy84Y2lhSExiamhDZnpiYzhteVFIRTlOTW5taGhzIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtbmVpZ2hib3Job29kLXZlcmlmeS13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtaGVldGFlLW5laWdoYm9yaG9vZC12ZXJpZnktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/8ciaHLbjhCfzbc8myQHE9NMnmhhs) | [Preview](https://nowonlikeus-git-heetae-neighborhood-verify-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T13:12:40.875Z">Oct 10, 2026 1:12pm UTC</relative-time> |


---

<a id="pr-76"></a>

### #76 Feat: 노원 동네 인증 버튼과 답변 배지 추가

- 작성 정우성(@wo0oo) · `useong/neighborhood-ui` → `dev` · 머지 · 올림 2026-10-10 22:36 · 머지 2026-10-10 22:39
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/76

노원 동네 인증의 화면 부분. 판정 · API 는 #75(희태), 경계 데이터는 #73.

##### 답변 배지
- 작성자가 인증했으면(`authorNeighborhoodVerified`) 닉네임 옆 **노원 인증** 표시
- 테두리만 있는 작은 배지 — 답 내용을 확인했다는 뜻 X, "운영자 확인 전" 문구 그대로

##### 인증 버튼 (`components/NeighborhoodVerify.tsx`)
- 답변 쓰기 칸 아래, 로그인한 사람만. 버튼 이름 **노원 동네 인증하기 (선택)**
- 흐름: 위치 한 번(`enableHighAccuracy`, 15초, `maximumAge 0`) → `checkPosition` → `inside` 일 때만 `POST /api/me/neighborhood` (본문 `{}`, 좌표 X)
- 인증 후: 배지 + **인증 지우기**(`DELETE`)
- 인증 · 지우기 직후 화면에 떠 있는 내 답변 배지를 새로고침 없이 맞춤
- 버튼 아래 고지: 위치는 휴대폰 안에서만 확인 · 서버 전송 X · 날짜만 남고 180일 뒤 사라짐

##### 결과별 안내 (`lib/neighborhoodView.ts`)
| 결과 | 안내 |
|---|---|
| inside | 인증 완료 · 배지 붙음 · 180일 뒤 재인증 |
| outside | 노원구 밖 → 노원구 안에서 다시 |
| inaccurate | 오차 200m 초과 → GPS 켜고 실외 · 창가에서 |
| denied | 위치 권한 꺼짐 → 브라우저 설정에서 허용 |
| timeout | 위치 찾기 시간 초과 → 잠시 후 다시 |
| unavailable | 위치 못 씀(https 아님 · 미지원) → 인증 없이도 답변 가능 |
| failed | 저장 실패 → 잠시 후 다시 |

##### 세션
- `useSession` 에 `neighborhoodVerified` 추가, `setNeighborhoodVerified` 로 성공 직후 상태만 맞춤 (서버 재조회 X)

##### 확인 사항
- `tsc` · `eslint` 통과, 테스트 674개 통과 (새로 12개: 문구 · 위치 오류 변환 · 내 답변 배지 갱신)
- 로컬(PC) 브라우저에서 인증 · 배지 · 안내 문구 확인
- 휴대폰 실제 인증은 https 필요 → 이 PR 의 Vercel 미리보기 주소로 확인

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-10 22:38

#### 코멘트

- @vercel · 2026-10-10 22:36

  > [vc]: #9b8KbcI5SXoeqw9lZ/75uraYP+6JHPTLenYJuZvsSZ4=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy80cDh6Qzk3SkxuOUM0ZGtiN0FKWlVITnUzc01ZIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbmVpZ2hib3Job29kLXVpLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctbmVpZ2hib3Job29kLXVpLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/4p8zC97JLn9C4dkb7AJZUHNu3sMY) | [Preview](https://nowonlikeus-git-useong-neighborhood-ui-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T13:37:06.825Z">Oct 10, 2026 1:37pm UTC</relative-time> |


---

<a id="pr-77"></a>

### #77 Chore: dev → master 배포 반영 (카카오 로그인 · 동네 인증 · 하단 탭)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-10 22:36 · 머지 2026-10-10 22:40
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/77

#68 이후 추가분 배포. 10/12~14 전시 전 반영용.

- 하단 탭 바 — 할 일 · 물어보기 · 이웃 질문 (#69)
- 이웃 질문 "내 질문" 탭 · 질문하기 로그인 안내 (#70)
- 카카오 로그인 — 회원번호만 받음, 닉네임은 따로 정함 (#71)
- 주민 답변 기반 승격 AI 초안 (#72, 권섭)
- 노원 동네 인증
  - 노원구 경계 데이터 (#73)
  - 판정 로직 · 저장 API (#75, 희태)
  - 인증 버튼 · 답변 배지 (#76) — **#76 머지 후 이 PR 에 자동 포함, 그 뒤 머지**

**DB 마이그레이션 적용 완료** — 공용 DB 에 먼저 적용함. 배포가 들어가도 스키마 불일치 X
- `20261010120000_user_kakao_login` (User.email · passwordHash nullable, kakaoId)
- `20261010200000_user_neighborhood_verified` (User.neighborhoodVerifiedAt)

**환경변수** — `KAKAO_REST_API_KEY` · `KAKAO_CLIENT_SECRET` Production 에 등록 완료. Preview 는 키 없음 → 카카오 버튼 숨김

##### 확인 사항
- dev 기준 tsc · vitest 통과 (#76 포함 674건)
- 머지 후 운영에서
  - 카카오 로그인 · 가입
  - 휴대폰(https)에서 노원 인증 · 답변 배지
  - 승격 화면 AI 초안 채우기
  - 하단 탭 · 내 질문

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-10 22:38

#### 코멘트

- @vercel · 2026-10-10 22:36

  > [vc]: #/98FxUypkAOrX4jB8eiRSTFzEz17U17HkT+DYyDeKfc=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9IQkVaWnhFUldkOWV5Q0tzVUw3NkhLVVNwOG1yIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/HBEZZxERWd9eyCKsUL76HKUSp8mr) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T13:40:05.331Z">Oct 10, 2026 1:40pm UTC</relative-time> |


---

<a id="pr-78"></a>

### #78 Docs: 전시 일정 · 새 기능 · 테스트 건수 반영

- 작성 정우성(@wo0oo) · `useong/docs-1010` → `dev` · 머지 · 올림 2026-10-10 22:47 · 머지 2026-10-11 01:17
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/78

10/12~14 전시 배포(#77) 내용을 문서에 반영. 코드 변경 X.

##### README
- 주요 기능: 내 질문 탭 · 노원 동네 인증(선택) · 승격 AI 초안 · 하단 탭 바
- 믿을 수 있게: 카카오 로그인(회원번호만), 동네 인증 좌표 서버 전송 X
- 기술 · 구조도: 카카오 로그인, `/api/me/neighborhood`
- 환경 변수: `KAKAO_REST_API_KEY` · `KAKAO_CLIENT_SECRET` (비우면 카카오 버튼 숨김)
- 테스트 505 → **674건**
- 일정: 전시 **10/11~13 → 10/12~14**, 배포 완료
- 외부 서비스: 카카오 로그인
- 데이터 출처: **노원구 경계 출처 표기 추가** (SGIS 공공누리 제1유형 · vuski/admdongkor CC BY 4.0 — 라이선스 조건)

##### docs
- `구현계획.md`: AI 승격 초안 완료(#72), 전시 범위 표 추가(#69~#76), 테스트 674건 파일별 내역, 기준일 10/10
- `기획서.md` · `설계안.md`: 전시 일정 10/12~14

##### 확인 사항
- 테스트 건수는 `vitest --reporter=json` 파일별 합계와 일치 (674)

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-10 22:49

#### 코멘트

- @vercel · 2026-10-10 22:47

  > [vc]: #h37waPBCWwxR3zN7Hh64FldIu0bQAbNo6q66b+7jExo=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9HRVd1V0dyeTY1Q2M2ZEo0d0o2TTZYMTk2QjFYIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy0xMDEwLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIiwibmV4dENvbW1pdFN0YXR1cyI6IkRFUExPWUVEIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9jcy0xMDEwLXdvMG9vcy1wcm9qZWN0cy52ZXJjZWwuYXBwIn0sInJvb3REaXJlY3RvcnkiOm51bGx9XX0=
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/GEWuWGry65Cc6dJ4wJ6M6X196B1X) | [Preview](https://nowonlikeus-git-useong-docs-1010-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T13:47:57.762Z">Oct 10, 2026 1:47pm UTC</relative-time> |


---

<a id="pr-79"></a>

### #79 Style: 화면 표면을 표지 기준으로 통일 · 평가 개선점 반영

- 작성 정우성(@wo0oo) · `useong/soft-surfaces` → `dev` · 머지 · 올림 2026-10-11 01:13 · 머지 2026-10-11 11:00
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/79

UI/UX 평가에서 나온 고칠 점 1~7 반영. 표지와 안쪽 화면이 다른 앱처럼 보이던 문제가 중심.

##### 1. 표면 통일 (표지 기준)
- 머리글 아래 굵은 검은 선 X, 상황 줄은 둥근 칩
- 할 일 · 상세: 왼쪽 색 띠 → 둥근 흰 카드 + 표지와 같은 **분류 칩**(아이콘 · 글자 · 연한 분류색)
- 분류 아이콘을 `components/CategoryIcon.tsx` 로 분리 — 표지 · 목록 · 상세 공용
- 기한: 날짜 있는 기한은 붉은 알약, "기한 없음"은 회색 작은 글자
- 하단 탭: 지금 탭은 아이콘 뒤 알약 배경, 위쪽 선 얇게
- 진행률 막대: 바탕색, 0건이어도 점 하나

##### 2 · 6. 할 일 목록
- 카드 왼쪽 동그라미로 **목록에서 바로 완료 체크** → "끝낸 일"로 이동 (저장 막힌 환경은 카드 아래 안내)
- 기한 없는 일은 "알아 두기"로 한 단계 낮춤 — 이유 한 줄, 전문은 상세
- 목록 높이 2,711px → 2,134px (390px, 예시 상황 10건)

##### 3. 상황 입력 기본값
- 집 · 계약 형태 미리 선택 X — 기숙사생이 그냥 넘어가 원룸 · 월세 목록을 받던 문제
- 안 고르면 브라우저 필수 안내 (날짜 칸과 같은 방식)

##### 4. 왼쪽 색 띠 정리
- 분류 · 인용 · 알림 세 뜻으로 쓰이던 띠를 전부 걷음
- 주민 답변: 말풍선 / 안내: 연한 색 둥근 상자 / 경고: 붉은 테두리 상자(색만으로 알리지 X) / AI 답 카드: 신뢰도 색은 둘레 테두리

##### 5. 고지 문구
- 질문하기 · 상황 입력 고지를 문단 → 짧은 줄 목록
- 외부 전송(Gemini) 고지는 접어 숨기지 X, 내용 그대로

##### 7. 작은 다듬기
- 표지 분류 이름표를 작게 — 누르는 곳처럼 안 보이게
- 표지 이웃 질문 제목 두 줄까지
- "로그인하고 답하기" 밑줄 링크 → 테두리 버튼
- 남은 굵은 검은 선(이웃 질문 탭 · 하단 링크 · 질문 결과) 얇게

##### 상세 전화 걸기
- "어디서" 카드의 전화 줄 → 카드 폭 전체 연한 초록 버튼 "번호 전화 걸기" (52px, `tel:` 링크 그대로, 번호는 DB 원문)

##### 안 한 것
- 상세 "← 내 할 일": 하단 탭과 겹치지만 공유 링크로 바로 들어온 사람의 돌아갈 길이라 유지
- 표지 "생활" 이름표 390px 줄바꿈: 카드 안쪽 폭 문제, 그대로

##### 확인 사항
- lint · tsc 통과, 테스트 674건 통과, `npm run build` 통과
- 로컬 390px 캡처로 표지 · 상황 입력 · 할 일 · 상세 · 물어보기 · 이웃 질문 확인 (라이트 · 다크)
- 새 브라우저에서 상황 입력 미선택 상태 · 제출 막힘 확인
- 휴대폰 확인은 이 PR 미리보기 주소로

#### 리뷰

- **승인** — 김권섭(@kwonseop) · 2026-10-11 02:01

#### 코멘트

- @vercel · 2026-10-11 01:13

  > [vc]: #+oUg/32bOOpoeirOG+OJon+LvTWa0EJ5W90NHXzpKK4=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9IRWNQR2s4aDlwVlNlTXBpek1vMmNtQ290M1NWIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2Vvbmctc29mdC1zdXJmYWNlcy13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCIsIm5leHRDb21taXRTdGF0dXMiOiJERVBMT1lFRCIsImxpdmVGZWVkYmFjayI6eyJyZXNvbHZlZCI6MCwidW5yZXNvbHZlZCI6MCwidG90YWwiOjAsImxpbmsiOiJub3dvbmxpa2V1cy1naXQtdXNlb25nLXNvZnQtc3VyZmFjZXMtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwicm9vdERpcmVjdG9yeSI6bnVsbH1dfQ==
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/HEcPGk8h9pVSeMpizMo2cmCot3SV) | [Preview](https://nowonlikeus-git-useong-soft-surfaces-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-10T16:21:58.439Z">Oct 10, 2026 4:21pm UTC</relative-time> |


---

<a id="pr-80"></a>

### #80 Chore: dev → master 배포 반영 (화면 통일 · 문서 정리)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-11 12:19 · 머지 2026-10-11 12:21
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/80

#77 이후 추가분 배포. 10/12~14 전시 직전 반영용.

- 화면 표면을 표지 기준으로 통일 · UI/UX 평가 개선점 반영 (#79)
  - 할 일 · 상세: 둥근 카드 + 표지와 같은 분류 칩, 머리글 굵은 선 X
  - 할 일 목록에서 바로 완료 체크, 기한 없는 일은 한 줄
  - 상황 입력: 집 · 계약 형태 미리 선택 X (안 고르면 제출 막힘)
  - 왼쪽 색 띠 정리 — 답변 말풍선 · 안내 둥근 상자 · 경고 테두리
  - 질문하기 · 상황 입력 고지를 짧은 줄로 (외부 전송 고지는 그대로 노출)
  - 상세 전화번호 → 전화 걸기 버튼
- README · 문서: 전시 일정 10/12~14, 새 기능, 테스트 674건, 노원구 경계 출처 (#78)

**DB · 환경변수 변경 X** — 화면 · 문서만

##### 확인 사항
- dev 기준 lint · tsc · vitest 674건 · build 통과
- 머지 후 운영에서
  - 할 일 목록 완료 체크 · 상세 전화 걸기
  - 상황 입력 새로 시작 시 미선택 상태
  - 물어보기 화면 Gemini 전송 고지 노출 (운영만 AI 켜짐)

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-11 12:21

#### 코멘트

- @vercel · 2026-10-11 12:20

  > [vc]: #L6QCw/usRTmnN/ZhFPeULrkxFFvkNdyoFDlFM2B/Qwc=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy80bTREZUcyaldrc2JZZm93OGZDY2tXVXlndXdRIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/4m4DeG2jWksbYfow8fCckWUyguwQ) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-11T03:20:01.983Z">Oct 11, 2026 3:20am UTC</relative-time> |


---

<a id="pr-81"></a>

### #81 Fix: 상황 입력 반려동물 항목을 강아지로 좁히기

- 작성 정우성(@wo0oo) · `useong/dog-only` → `dev` · 머지 · 올림 2026-10-11 14:22 · 머지 2026-10-11 18:42
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/81

상황 입력의 반려동물 항목을 "강아지를 키워요"로 좁힘. 동물등록 의무가 개에만 있어서, 고양이를 키우는 사람에게 "반려견 동물등록하기"가 뜨는 걸 막기 위함.

##### 근거
- 동물등록 의무 대상: 2개월 이상 개 (동물보호법)
- 고양이: 2026년 현재 선택 등록. 의무화 법안은 발의 단계(미확인)라 반영 X

##### 변경
- `ProfileForm` — "반려동물과 살아요" → **"강아지를 키워요"**
- `PromotionEditor` — 노출 조건 "반려동물 키우는 사람" → **"강아지 키우는 사람"**
- `lib/promotionForm.ts` `audienceSummary` — `'강아지 있음'` (+ 테스트 수정)
- `lib/types.ts` · `prisma/schema.prisma` — `hasPet` / `requiresPet` 뜻을 **강아지**로 적은 주석만 추가

##### 안 바꾼 것
- 필드 이름 `hasPet` / `requiresPet` 그대로 — **스키마 변경 · 마이그레이션 X**
- 종류와 상관없는 반려동물 규칙(기숙사 반입 금지 등)은 `requiresPet` 대신 **기숙사 조건**으로 거는 걸로 정리

##### 확인 사항
- `npx tsc --noEmit` / `npm run lint` 통과
- `npm test` 통과

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-11 18:41

#### 코멘트

- @vercel · 2026-10-11 14:22

  > [vc]: #K5bEbM0CGyVybqMNYGq73nVq5yznByfesvnoH4x1nXE=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9nLW9ubHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9FdVVyZXNGelFaaFJ3aTN6amczVFhQS3RvRjNtIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctZG9nLW9ubHktd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/EuUresFzQZhRwi3zjg3TXPKtoF3m) | [Preview](https://nowonlikeus-git-useong-dog-only-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-11T05:22:13.984Z">Oct 11, 2026 5:22am UTC</relative-time> |


---

<a id="pr-82"></a>

### #82 Feat: 승격 화면에 같은 조건으로 이미 보이는 할 일 표시

- 작성 정우성(@wo0oo) · `useong/promotion-overlap` → `dev` · 머지 · 올림 2026-10-11 14:22 · 머지 2026-10-11 18:42
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/82

승격 화면에서 노출 조건을 고르면 **"이 사람들에게 이미 보이는 할 일"**을 보여 주는 패널. 새 할 일이 기존 할 일과 서로 모르는 문장으로 나란히 뜨는 걸 막기 위함.

**#81 위에 쌓은 브랜치.** #81 먼저 머지하면 이 PR 차이는 마지막 커밋 하나만 남음.

##### 왜
- 승격된 할 일은 목록에 더해지기만 하고, 기존 할 일과의 관계는 아무도 안 봄
- 예: "빛솔재 강아지 반입 금지" 승격 → 기숙사 · 강아지 사람 화면에 **"반려견 동물등록하기"와 나란히** 뜸
- 동물등록은 개를 가진 사람의 의무라 한쪽을 숨기면 안 됨 → **운영자가 같이 보고 이어지는 문장으로 쓰게 함**
- 보여 주기만 함. 자동 숨김 · 발행 막기 X

##### 변경
- `lib/promotionOverlap.ts` — 겹침 판정 순수 함수
  - `canShareViewer` — 주거 · 계약 형태가 엇갈리면 같은 사람에게 안 보임 (빈 목록 = 조건 없음)
  - `sharedConditions` — 둘 다 좁힌 조건만 "기숙사 · 강아지"처럼 이름으로
  - `findOverlaps` — `related`(겹치는 조건 많은 순) / `general`(넓게 보이는 할 일)로 나눔
- `tests/promotionOverlap.test.ts` — 14건
- `components/TaskOverlapPanel.tsx` — "누구에게 보여줄까요?" 바로 아래. 조건 바꿀 때마다 다시 계산
  - 겹치는 할 일: 분류 칩 · 제목 · "겹치는 조건: …"
  - 넓게 보이는 할 일: "넓게 보이는 할 일 N건도 함께 보입니다"로 접음
  - 불러오기 실패: 안내만 띄우고 발행은 그대로
- `lib/types.ts` — `AdminTaskSummary` · `AdminTaskListResponse` 계약 타입
- `app/globals.css` — `.overlap*`

##### API (희태)
- `GET /api/admin/tasks` 필요 — 운영자 전용, 할 일 id · 제목 · 분류 · 노출 조건만
- **API 머지 전에는 "불러오지 못해 겹치는 할 일 확인을 건너뜁니다"만 뜸.** 머지 순서 상관없음
- 응답 모양은 위 계약 타입 그대로

##### 확인 사항
- `npx tsc --noEmit` / `npm run lint` 통과
- `npm test` 688건 통과
- 패널에 실제 목록 뜨는 건 **API 머지 후 확인 예정**

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-11 18:41

#### 코멘트

- @vercel · 2026-10-11 14:22

  > [vc]: #2sOOnkOsg+GPpERH37SYlNjcHzqlZr9JvBJ6d7c7SMw=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcHJvbW90aW9uLW92ZXJsYXAtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9IS1h5RkxpcGlDMlp6TE5KeXJxdTJYQVl4bW10IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC11c2VvbmctcHJvbW90aW9uLW92ZXJsYXAtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/HKXyFLipiC2ZzLNJyrqu2XAYxmmt) | [Preview](https://nowonlikeus-git-useong-promotion-overlap-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-11T05:22:31.127Z">Oct 11, 2026 5:22am UTC</relative-time> |


---

<a id="pr-83"></a>

### #83 Feat: 승격 화면용 발행된 할 일 목록 API 추가

- 작성 우희태(@Heetaeeee) · `heetae/admin-tasks` → `dev` · 머지 · 올림 2026-10-11 17:45 · 머지 2026-10-11 18:44
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/83

##### 무엇을
승격 화면 "이미 보이는 할 일" 브리프의 API 부분 — `GET /api/admin/tasks`.

- `requireAdmin()` (role DB 재조회, `/api/admin/promotions` 와 같게). 비로그인 401 · 일반 회원 403
- 발행된(`isPublished: true`) 할 일 전부. 시드 · 승격 구분 없음. 내린 할 일은 목록에 안 뜨므로 제외
- `select` 는 id · title · category · housingTypes · contractTypes · requiresCar · requiresPet · studentOnly 만. 이유 · 방법 · 장소 · 출처는 DB 에서부터 안 꺼냄
- 응답 `AdminTaskListResponse`, `Cache-Control: no-store`, 만든 순(createdAt → id)으로 고정

##### 머지 순서
#82(useong/promotion-overlap) 위에 쌓았습니다 — 타입이 #82 에 있습니다. **#81 → #82 → 이 PR** 순서로 머지해 주세요.

##### 확인
- lint · tsc · 테스트 694개 통과 (새로 6개: 401 · 403 · 200 + 필드 8개만 · 발행된 것만 · no-store · 빈 목록), 빌드 통과
- 로컬: 운영자로 `/api/admin/tasks` 확인(17건, 필드 8개만), 승격 화면 겹침 패널이 목록을 불러오는 것 확인 (발행은 하지 않음)

#### 리뷰

- **승인** — 정우성(@wo0oo) · 2026-10-11 18:40

#### 코멘트

- @vercel · 2026-10-11 17:45

  > [vc]: #xb0Aeq6sg/ZqQ1UM4bw4hR5bKvAlbBPVA6zWRnvT9+M=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwibGl2ZUZlZWRiYWNrIjp7InJlc29sdmVkIjowLCJ1bnJlc29sdmVkIjowLCJ0b3RhbCI6MCwibGluayI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtYWRtaW4tdGFza3Mtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAifSwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy8zUDg3cHd0QUt1dUVweWsxTHVEVGd6am1WTVN0IiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1oZWV0YWUtYWRtaW4tdGFza3Mtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQifV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/3P87pwtAKuuEpyk1LuDTgzjmVMSt) | [Preview](https://nowonlikeus-git-heetae-admin-tasks-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-11T08:45:51.363Z">Oct 11, 2026 8:45am UTC</relative-time> |


---

<a id="pr-84"></a>

### #84 Chore: dev → master 배포 반영 (강아지 조건 · 승격 겹침 패널 · API)

- 작성 정우성(@wo0oo) · `dev` → `master` · 머지 · 올림 2026-10-11 18:43 · 머지 2026-10-11 18:47
- 원본: https://github.com/2026-KW-HACKATHON/13_NowonLikeUs/pull/84

﻿#80 이후 추가분 배포. 10/12~14 전시 직전 반영용.

- 상황 입력 반려동물 항목 → **"강아지를 키워요"** (#81)
  - 동물등록 의무가 개에만 있음. 고양이 키우는 사람에게 "반려견 동물등록하기" 안 뜨게
  - 승격 화면 노출 조건 · 요약도 "강아지"로
- 승격 화면에 **"이 사람들에게 이미 보이는 할 일"** 패널 (#82)
  - 조건 고르면 같은 사람에게 함께 보일 할 일을 겹치는 조건과 함께 표시. 숨김 · 발행 막기 X
  - 운영자 화면에만 영향
- 패널용 `GET /api/admin/tasks` (#83) — 운영자 전용, 발행된 할 일의 제목 · 분류 · 노출 조건만

**DB · 환경변수 변경 X** — 스키마는 주석만, 마이그레이션 X

##### 확인 사항
- dev 기준 lint · tsc · vitest 694건 · build 통과
- 머지 후 운영에서
  - 상황 입력 "강아지를 키워요" 표시
  - 승격 화면 패널에 겹치는 할 일 목록 표시, 발행 정상

#### 리뷰

- **승인** — 우희태(@Heetaeeee) · 2026-10-11 18:46

#### 코멘트

- @vercel · 2026-10-11 18:43

  > [vc]: #S+D9napthaH3BpQGRdB+HGdPgzbuUHPwCMEEXouTe0M=:eyJpc01vbm9yZXBvIjp0cnVlLCJ0eXBlIjoiZ2l0aHViIiwicHJvamVjdHMiOlt7Im5hbWUiOiJub3dvbmxpa2V1cyIsInByb2plY3RJZCI6InByal9lMW9oTGkxc3NCUExRWE80UEo3VVVBVkZzaTBzIiwiaW5zcGVjdG9yVXJsIjoiaHR0cHM6Ly92ZXJjZWwuY29tL3dvMG9vcy1wcm9qZWN0cy9ub3dvbmxpa2V1cy9FQzdBdHM5QVlpRURiRjhnRHhCUW14b0JiTUZBIiwicHJldmlld1VybCI6Im5vd29ubGlrZXVzLWdpdC1kZXYtd28wb29zLXByb2plY3RzLnZlcmNlbC5hcHAiLCJuZXh0Q29tbWl0U3RhdHVzIjoiREVQTE9ZRUQiLCJsaXZlRmVlZGJhY2siOnsicmVzb2x2ZWQiOjAsInVucmVzb2x2ZWQiOjAsInRvdGFsIjowLCJsaW5rIjoibm93b25saWtldXMtZ2l0LWRldi13bzBvb3MtcHJvamVjdHMudmVyY2VsLmFwcCJ9LCJyb290RGlyZWN0b3J5IjpudWxsfV19
  > The latest updates on your projects. Learn more about [Vercel for GitHub](https://vercel.link/github-learn-more).
  > 
  > | Project | Deployment | Actions | Updated |
  > | :--- | :----- | :------ | :------ |
  > | <a href="https://vercel.com/wo0oos-projects/nowonlikeus"><sup><img src="https://vercel.com/api/www/avatar?projectId=prj_e1ohLi1ssBPLQXO4PJ7UUAVFsi0s&teamId=team_0Mw7tPAfXKOcFhu7nyeMolT9&s=32" width="16" height="16" align="middle" alt="" /></sup></a> [nowonlikeus](https://vercel.com/wo0oos-projects/nowonlikeus) | ![Ready](https://vercel.com/static/status/ready.svg) [Ready](https://vercel.com/wo0oos-projects/nowonlikeus/EC7Ats9AYiEDbF8gDxBQmxoBbMFA) | [Preview](https://nowonlikeus-git-dev-wo0oos-projects.vercel.app) | <relative-time datetime="2026-10-11T09:45:02.951Z">Oct 11, 2026 9:45am UTC</relative-time> |


---
