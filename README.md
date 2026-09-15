# BAI 작업 공유

BAI 소모임원들이 각자 AI 에이전트(Claude Code/Codex 등)로 만든 **프로젝트 파일**과, 그 작업 맥락을 정리한 **핸드오프 문서**를 한 저장소에서 주고받기 위한 공간입니다.

## 폴더 구조

```
bai-shared/
├── handoffs/                  — 세션이 끝날 때 남기는 짧은 요약 문서
│   ├── template.md
│   └── YYYY-MM-DD-이름-핸드오프.md
└── projects/                  — 실제 프로젝트 코드·데이터, 사람(GitHub 아이디)별로 구분
    ├── trbb82349/
    │   └── careerlens-mvp/
    └── (다른 팀원 GitHub 아이디)/
        └── (그 사람의 프로젝트)/
```

프로젝트 폴더는 **사람 기준**으로 나뉩니다 — 팀원이 늘어나도 "누가 만든 건지" 한눈에 보이도록 하기 위해서입니다.

## 사용 방법 (전원 공통)

자기 AI 코딩 에이전트(Claude Code·Codex·Cursor 등 무엇이든)에게 아래처럼 한 줄만 시키세요. 이 저장소의 [AGENTS.md](AGENTS.md)에 자세한 절차가 적혀 있어서, 그 파일을 읽을 줄 아는 에이전트라면 알아서 따라합니다.

<img src="https://img.shields.io/badge/%ED%8C%80%EC%9B%90%20%EC%9E%91%EC%97%85%20%EA%B3%B5%EC%9C%A0%20%EB%B0%9B%EA%B8%B0-yellow?style=for-the-badge" alt="팀원 작업 공유 받기" height="34">

> 처음 받을 때나, 나중에 다시 동기화할 때나 똑같이 (오른쪽 위 복사 아이콘 클릭)
>
> ```text
> 이 저장소를 clone 받고 AGENTS.md 안내를 따라서, handoffs/ 안의 문서들을 요약해서 보여줘: https://github.com/trbb82349/bai-shared.git
> ```

이미 한 번 받아본 적 있으면, AI가 알아서 **지난번 이후 새로 올라온 핸드오프 문서와 업데이트된 프로젝트만** 찾아서 알려줍니다 (이미 봤던 내용을 매번 다시 읽거나 설명하지 않음).

<img src="https://img.shields.io/badge/%EB%82%B4%20%EC%9E%91%EC%97%85%20%EA%B3%B5%EC%9C%A0%ED%95%98%EA%B8%B0-orange?style=for-the-badge" alt="내 작업 공유하기" height="34">

> 내 작업을 공유할 때 (오른쪽 위 복사 아이콘 클릭)
>
> ```text
> bai-shared 저장소의 AGENTS.md를 읽고, 지금 이 프로젝트를 내 GitHub 아이디 폴더 아래에 올리고 핸드오프 문서도 같이 써서 push해줘. 내 GitHub 아이디는 (여기에 아이디)야.
> ```

명령어를 직접 치고 싶다면 [AGENTS.md](AGENTS.md)에 적힌 절차를 그대로 따라 하면 됩니다 (clone → `projects/내GitHub아이디/`에 프로젝트 폴더 추가 → `handoffs/template.md` 복사해서 채우기 → add/commit/push).

**특정 팀원 작업만 받고 싶을 때**: 전체를 다 받지 않고 그 사람 폴더만 받을 수도 있습니다. AI에게 "OO 작업만 받고 싶어"라고 하면 [AGENTS.md](AGENTS.md)의 sparse-checkout 절차대로 그 사람 폴더만 골라 받아줍니다.

## 원칙

- 핸드오프 문서에 원본 대화를 통째로 붙여넣지 않습니다. 노이즈가 많아서 상대방 AI가 핵심을 못 고릅니다. 반드시 템플릿 항목별로 걸러서 요약합니다.
- 프로젝트 폴더 안의 자세한 기록(README 등)은 그대로 두고, 핸드오프 문서는 그 위에 얹는 짧은 요약 레이어로 씁니다.
- 이 저장소는 public입니다. 개인정보·API 키·비밀번호는 절대 올리지 않습니다.

## 참여하기

쓰기 권한(협업자 등록)이 필요합니다. GitHub 아이디를 저장소 관리자(trbb82349)에게 알려주세요.

## 예시

- [handoffs/template.md](handoffs/template.md) — 빈 템플릿
- [handoffs/2026-09-02-trbb82349-핸드오프.md](handoffs/2026-09-02-trbb82349-핸드오프.md) — 실제 프로젝트로 채운 작성 예시 (파일명 규칙을 따른 예시이기도 함)
- [projects/trbb82349/careerlens-mvp/](projects/trbb82349/careerlens-mvp/) — 그 예시가 가리키는 실제 프로젝트
