# AD3 Docs

AD3 사용자 **튜토리얼 페이지** 작성을 위한 repository 입니다.

## Branch 및 Version 관리

### 개발 - next branch
**next** branch를 개발 branch로 쓰며, 해당 branch에 commit하는 내용은 일정 주기로 **[docs.ad3.arontier.co.kr](http://docs.arontier.co.kr)**에 자동 업데이트 됩니다.

### 상용 - version release
새 version이 나오면, next branch를 main으로 merge한 후, version release를 합니다. 해당 버전은 정식 release를 통해 **[docs.ad3.io](https://docs.ad3.io)**에 업데이트 됩니다.

## 디렉토리 및 문서 구조

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
