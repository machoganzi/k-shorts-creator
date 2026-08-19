# K-Shorts Creator — GitHub Chat Workflow

한국 YouTube Shorts를 일반 ChatGPT 채팅에서 **GitHub URL 하나로 불러와 사용하는 대화형 제작 워크플로우**입니다.

이 저장소는 Plugin/Skill 설치물이 아닙니다. 사용자가 새 ChatGPT 대화에서 `START_HERE.md`를 읽고 적용하라고 명시하면, 그 대화에서 다음 흐름을 사용하도록 설계되어 있습니다.

```text
CHANNEL DNA
→ BRAINSTORM + K-CONTEXT
→ LOCK
→ GRILL
→ SCRIPT
→ K-LOCALIZE
→ RETENTION
→ LEARN
```

## 가장 빠른 사용법

GitHub에 업로드한 뒤 주소의 `OWNER/REPO`만 바꿔 새 ChatGPT 채팅에 붙여넣습니다.

```text
이 GitHub 워크플로우를 현재 대화에 적용해줘.
먼저 아래 START_HERE.md를 웹에서 실제로 열어 읽고, 현재 단계에 필요한 하위 파일만 추가로 읽어.

https://github.com/OWNER/REPO/blob/main/START_HERE.md

쇼츠 아이디어가 하나 있는데 아직 모호해. 대본은 쓰지 말고 한 질문씩 브레인스토밍부터 하자.
```

더 많은 시작 문구는 [`COPY_PASTE_PROMPTS.md`](COPY_PASTE_PROMPTS.md)를 참고합니다.

## 핵심 설계

- Brainstorm과 Grill은 한 질문씩 진행
- 사용자의 실제 생각과 채널 말투 우선
- 한국형 = 번역이나 억지 유행어가 아니라 `시청 상황 + 관계 + 화자 역할 + 감정 + 신뢰` 설계
- Creative Brief를 잠근 뒤 약점을 Grill
- 대본은 초 단위 내레이션·화면·자막·패턴 변화·리텐션 기능까지 작성
- 제목 / 첫 화면 / 첫 말을 서로 다른 역할로 설계
- 정확한 이탈 초와 원문을 지목하는 Retention Review
- 공개 조회수보다 채널 내부 Studio 지표와 비교해 다음 가설 학습
- `최근` 정보는 저장소가 아니라 최신 웹 자료로 재검증

## 저장소 구조

```text
START_HERE.md                # ChatGPT가 첫 번째로 읽을 핵심 문서
COPY_PASTE_PROMPTS.md        # 새 채팅에 붙여넣는 시작 프롬프트
CHATGPT_GITHUB_SETUP.md      # GitHub 공개/비공개 사용법
workflows/
  brainstorm.md
  lock.md
  grill.md
  script.md
  retention.md
  learn.md
  research.md
references/                  # 한국화, 훅, 리텐션, 근거, 분석 참고자료
templates/                   # Channel DNA, Creative Brief, 대본, 검수 템플릿
THIRD_PARTY_NOTICES.md
LICENSE
```

`START_HERE.md` 자체에 핵심 규칙을 충분히 넣어 두었기 때문에, 보조 파일 일부를 불러오지 못해도 기본 워크플로우는 유지됩니다.

## GitHub에 올리기

1. ZIP을 압축 해제합니다.
2. GitHub에서 새 저장소를 만듭니다. 여자친구와 URL로 바로 공유하려면 `Public`이 가장 간단합니다.
3. 빈 저장소에서 `Add file → Upload files`를 누릅니다.
4. 압축을 푼 **폴더 안의 파일과 폴더 전체**를 드래그해서 업로드하고 commit합니다.
5. 저장소의 `START_HERE.md`를 열고 주소를 복사합니다.

자세한 ChatGPT 연동은 [`CHATGPT_GITHUB_SETUP.md`](CHATGPT_GITHUB_SETUP.md)를 참고합니다.

## 처음 만들 Channel DNA

첫 사용 때 다음처럼 요청할 수 있습니다.

```text
이 워크플로우를 적용하고 우리 채널 DNA부터 한 질문씩 잡아줘.
```

정리된 Channel DNA는 별도로 보관한 뒤 새 채팅 시작 때 붙여넣는 것을 권장합니다. 저장소가 공개라면 개인 정보나 비공개 채널 데이터를 저장소에 올리지 마세요.

## 근거와 한계

- 최근 한국형 리서치의 출발점은 `references/evidence-register.md`에 정리되어 있습니다.
- 한국 시청자를 하나의 취향으로 일반화하지 않습니다.
- 경쟁 채널의 비공개 유지율을 추정하지 않습니다.
- Vyral Content Skills의 20만+ 분석은 프로젝트의 자체 주장으로만 취급하고, 공개되지 않은 성과 임계값은 가져오지 않습니다.
- 실제 채널 데이터가 일반 조사보다 우선합니다.

## License

MIT. Third-party methodological influences are documented in `THIRD_PARTY_NOTICES.md`.
