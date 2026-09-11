# BAI 작업 공유

BAI 소모임원들이 각자 AI 에이전트(Claude Code/Codex 등)로 만든 **프로젝트 파일**과, 그 작업 맥락을 정리한 **핸드오프 문서**를 한 저장소에서 주고받기 위한 공간입니다.

## 폴더 구조

```
bai-shared/
├── handoffs/     — 세션이 끝날 때 남기는 짧은 요약 문서
│   ├── template.md
│   └── (이름)-핸드오프.md
└── projects/     — 실제 프로젝트 코드·데이터
    └── (프로젝트 이름)/
```

## 사용 방법 (전원 공통)

1. 이 저장소를 처음 한 번만 `git clone https://github.com/trbb82349/bai-shared.git` 받습니다.
2. 작업할 땐 `projects/자기프로젝트이름/` 폴더 안에서 합니다. 새 프로젝트면 폴더를 새로 만듭니다.
3. 세션을 마칠 때 `handoffs/template.md`를 복사해서 `handoffs/날짜-이름-핸드오프.md`로 저장하고 채웁니다. "결과물 위치"에는 로컬 경로 대신 `projects/자기프로젝트이름/...`처럼 **이 저장소 안의 경로**를 적습니다.
4. `git add`, `git commit`, `git push`로 올립니다.
5. 팀원은 `git pull` 한 번으로 모든 사람의 프로젝트와 핸드오프 문서를 같이 받습니다. 다른 사람의 핸드오프 문서를 자기 AI 에이전트 대화창에 붙여넣으면 이어서 작업할 수 있습니다.

## 원칙

- 핸드오프 문서에 원본 대화를 통째로 붙여넣지 않습니다. 노이즈가 많아서 상대방 AI가 핵심을 못 고릅니다. 반드시 템플릿 항목별로 걸러서 요약합니다.
- 프로젝트 폴더 안의 자세한 기록(README 등)은 그대로 두고, 핸드오프 문서는 그 위에 얹는 짧은 요약 레이어로 씁니다.
- 이 저장소는 public입니다. 개인정보·API 키·비밀번호는 절대 올리지 않습니다.

## 참여하기

쓰기 권한(협업자 등록)이 필요합니다. GitHub 아이디를 저장소 관리자(trbb82349)에게 알려주세요.

## 예시

- [handoffs/template.md](handoffs/template.md) — 빈 템플릿
- [handoffs/예시-careerlens-mvp-핸드오프.md](handoffs/예시-careerlens-mvp-핸드오프.md) — 실제 프로젝트로 채운 작성 예시
- [projects/careerlens-mvp/](projects/careerlens-mvp/) — 그 예시가 가리키는 실제 프로젝트
