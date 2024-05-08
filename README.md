# AD3 Docs

AD3 사용자 **튜토리얼 페이지** 작성을 위한 repository 입니다.


## Branch 및 Version 관리

### 개발 - next branch
**next** branch를 개발 branch로 쓰며, 해당 branch에 commit하는 내용은 일정 주기로 [docs.ad3.arontier.co.kr](http://docs.arontier.co.kr) 에 자동 업데이트 됩니다.

### 상용 - version release
새 version이 나오면, next branch를 main으로 merge한 후, version release를 합니다. 해당 버전은 정식 release를 통해 [docs.ad3.io](https://docs.ad3.io) 에 업데이트 됩니다.
- [Semantic Versioning](https://semver.org/) 을 따르며, `x.y.z` 형식으로 versioning 합니다.

## 디렉토리 및 문서 구조

### 디렉토리 구조

```bash
ad3-docs
├── img
│   ├── signUpPage.png
│   ├── aNewImage.png
│   └── a-new-category
│       ├── youCanAdd.png
│       └── moreImages.png
└── locale
    ├── en
    │   ├── intro.md
    │   ├── dashboard.md
    │   └── discovery
    │       ├── _category_.json
    │       └── docking-of-millions
    │           ├── _category_.json
    │           ├── create-a-job.md
    │           └── output-report.md
    └── ko
        ├── intro.md
        ├── dashboard.md
        └── discovery
            ├── _category_.json
            └── docking-of-millions
                ├── _category_.json
                ├── create-a-job.md
                └── output-report.md
```
- `/img/` - `.md`에 쓰일 이미지 파일들
- `/locale/` - 지원 언어 별로 구분 된 AD3 튜토리얼입니다. 디렉토리 구조가 그대로 튜토리얼 사이트의 sidebar가 됩니다. **_모든 언어가 같은 디렉토리 구조를 가져야 합니다._**


### Sidebar 관리

동일 레벨의 sidebar 사이의 display 순서는 sidebar position을 지정하여 정합니다.

- `.md` 파일의 경우:
  - 파일 상단에 `sidebar_position` 값을 지정합니다. (본문에는 드러나지 않습니다.)
  - `sidebar_position` 아래의 최상단의 header가 sidebar label이 됩니다.
```md
---
sidebar_position: 1
---
# Tutorial Intro
...
```

- directory의 경우:
  - `_category_.json` 파일 아래 sidebar position과 label을 작성합니다.
```json
{
  "label": "Discovery",
  "position": 3,
}
```
