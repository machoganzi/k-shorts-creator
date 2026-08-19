# ChatGPT + GitHub 사용 가이드

기준일: 2026-08-19 KST

## A. 공개 저장소: GitHub 연결 없이 사용

가장 단순한 방식이다.

1. 이 저장소를 GitHub에서 `Public`으로 만든다.
2. `START_HERE.md`의 GitHub 페이지 주소를 복사한다.
3. 새 ChatGPT 대화에서 `COPY_PASTE_PROMPTS.md`의 공개 GitHub 프롬프트를 붙여넣는다.
4. ChatGPT가 실제로 문서를 읽도록 `웹에서 열어 읽어`라고 명시한다.
5. 이후 같은 대화에서는 자연어로 `브리프 잠가줘`, `Grill me`, `대본 시작`, `리텐션 검수`처럼 전환한다.

이 방식은 Plugin/Skill 설치가 아니다. 새 대화마다 시작 문서를 다시 알려주는 것이 안전하다.

## B. 비공개 저장소: ChatGPT의 GitHub App 사용

GitHub App이 현재 ChatGPT 화면과 플랜에서 제공되는 경우 사용할 수 있다.

1. ChatGPT `Settings → Apps`에서 GitHub을 찾는다.
2. GitHub에서 ChatGPT 앱을 승인하고 접근시킬 저장소를 선택한다.
3. 필요한 경우 ChatGPT의 GitHub 설정에서 `Choose repositories` / `Configure Repositories on GitHub`로 접근 범위를 바꾼다.
4. 표준 Chat에서 GitHub 앱이 제공되는 경우 도구 메뉴(+) 또는 앱 호출 방식으로 GitHub을 추가하고, 저장소 이름과 `START_HERE.md`의 고유 제목 문구를 사용해 워크플로우를 찾게 한다.

GitHub 앱의 사용 가능 여부는 ChatGPT 플랜과 제품 화면에 따라 다를 수 있다. 일부 환경에서는 Deep Research/Agent Mode에서만 보이고 표준 Chat에서는 보이지 않을 수 있다.

새 저장소가 GitHub 앱 검색에서 바로 안 보이면 GitHub 검색에서 다음 형태를 검색해 색인 생성을 유도할 수 있다.

```text
repo:OWNER/REPO import
```

색인이 반영되기까지 시간이 걸릴 수 있다.

## 권장 운영

- 여자친구와 공유 목적이면 **공개 저장소 + START_HERE 직접 URL**이 가장 간단하다.
- 채널 정보가 비공개면 저장소를 Private으로 하고 GitHub App을 사용할 수 있는 계정인지 먼저 확인한다.
- Channel DNA는 저장소에 개인정보를 넣기보다 로컬에 보관하고 새 채팅 시작 시 붙여넣는 방식을 권장한다.
- 플랫폼 정책이나 `최근` 트렌드는 저장소에 적힌 내용을 그대로 믿지 않고 ChatGPT에게 최신 웹 검증을 지시한다.
