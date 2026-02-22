# Note Taking Skill

`docker-kubernetes/notes/README.md`를 노트 템플릿 원본으로 사용해서,
코드베이스 분석 내용을 같은 형식으로 빠르게 작성한다.

## 목표
- `코드베이스 분석 => 노트테이킹` 흐름만 수행
- 템플릿 섹션명/순서를 최대한 유지해 사용
- `notes/README.md`는 기본 템플릿 문서로 유지하고, 실노트는 별도 파일에 작성
- 주차 입력(`W{N}`) 기반의 `notes/Week_{N}/` 경로 사용을 권장
- 필요하면 웹 리서치 후 `참고 링크`를 채움
- 학습 도움을 위한 `Suggestions by AI (optional)`를 작성

## 호출 추천 포맷
- 추천 명령: `/note-taking W{N} <주제>`
- `W{N}` 입력을 권장 (예: `W4`)
- 출력 경로 권장:
  - 폴더: `docker-kubernetes/notes/Week_{N}/`
  - 파일: `YYYY-MM-DD-주제.md`

## 실행 절차
1. 코드베이스 스캔
- `rg --files`로 파일 목록 확인
- `README.md`, 설정 파일, 핵심 디렉터리만 우선 확인

2. 핵심 정보 추출
- 프로젝트가 무엇을 하는지
- 실행/테스트 방법
- 주요 파일/모듈 역할
- 구현상 중요한 의사결정
- 현재 리스크/미해결 항목
- (필요 시) 웹 리서치로 공식 문서/신뢰 가능한 참고 링크 수집

3. 노트 작성
- `docker-kubernetes/notes/README.md`의 템플릿을 복사해 사용
- 주차 방식 사용 시, 대상 폴더가 없으면 `notes/Week_{N}/` 생성
- 근거 없는 추측 금지
- 가능하면 파일 경로/명령어를 함께 기록
- `참고 링크`에는 링크만 두지 말고 왜 참고할 만한지 짧게 덧붙임
- `Suggestions by AI (optional)`에는 학습 순서/미니 실습/체크 질문을 제안
- 노트 저장 후 커밋이 필요하면 `/commit docs <요약>` 포맷으로 이어서 실행

## 노트 템플릿
```md
> 주차(추천): W4 | 날짜: YYYY-MM-DD

# 제목

## 배경/목표
- 

## 핵심 내용
- 

## 기록
- 명령어:
- 결과:

## 트러블슈팅
- 문제:
- 원인:
- 해결:

## 자랑하고 싶은 것
- 

## 참고 링크
- 

## Suggestions by AI (optional)
- 추천 학습 순서:
- 20분 실습 과제:
- 셀프 체크 질문:
- 다음에 보면 좋은 자료:
```

## 호출 예시
- `/note-taking W4 ingress 정리`
- `/note-taking W7 kubernetes service type 비교`
