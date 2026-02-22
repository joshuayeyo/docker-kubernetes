# Commit Skill

변경사항을 빠르게 점검하고, 일관된 포맷으로 커밋하도록 돕는 에이전트.

## 목표
- 변경 파일 확인 후 의도에 맞는 커밋 메시지 작성
- 커밋 전에 최소 점검(`git status`, `git diff --staged`) 수행
- 이 레포의 기존 스타일(`DOCS: ...`)을 우선 추천

## 호출 추천 포맷
- 추천 명령: `/commit <type> <요약>`
- 예시:
  - `/commit docs note-taking 템플릿 추천 문구 정리`
  - `/commit docs W4 노트 초안 추가`

## 커밋 타입 추천
- `docs`: 문서 변경
- `feat`: 기능 추가
- `fix`: 버그 수정
- `refactor`: 동작 변경 없는 구조 개선
- `chore`: 설정/정리 작업

## 메시지 추천 규칙
- 기본 형식: `TYPE: 변경 요약`
- `TYPE`은 대문자(uppercase) 사용 권장 (`DOCS`, `FEAT`, `FIX` ...)
- 한 줄에 핵심 변경 1개를 먼저 작성
- 필요한 경우 본문에 파일/배경을 2~4줄 추가

## 실행 절차
1. 변경 확인
- `git status --short`
- `git diff --staged --name-only`

2. 메시지 생성
- 스테이징된 파일 기준으로 타입 결정
- 요약은 짧고 구체적으로 작성

3. 커밋 실행
- 기본: `git commit -m "TYPE: 변경 요약"`
- 본문 필요 시:
  - `git commit -m "TYPE: 변경 요약" -m "- 변경 파일: ...\n- 이유: ..."`

## 호출 예시
- `/commit docs notes/README.md에 Suggestions by AI 섹션 추가`
- `/commit docs skills/note-taking.md 추천 기반 문구로 변경`
