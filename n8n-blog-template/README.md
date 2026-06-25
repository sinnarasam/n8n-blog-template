# n8n-blog-template

n8n + Upstage Solar AI로 블로그 글을 자동 생성·발행하는 템플릿입니다.  
**Beautiful Jekyll** 기반 인디고 테마 · fortune cookie 🥠 애니메이션 홈 화면

## 시작하기

### 1. 이 템플릿으로 내 레포 만들기

오른쪽 위 **Use this template → Create a new repository** 클릭

- Repository name: `n8n-blog`
- Public 선택 (GitHub Pages 무료 사용)
- **Create repository** 클릭

### 2. GitHub Pages 활성화

내 레포 → **Settings → Pages**

- Source: `Deploy from a branch`
- Branch: `main` / `/ (root)`
- **Save** 클릭

약 1분 후 `https://[내 GitHub 아이디].github.io/n8n-blog/` 에서 블로그 확인

### 3. _config.yml 수정

```yaml
title: "나의 AI 블로그"          # ← 블로그 이름으로 변경하세요
github-username: your-github-id  # ← 본인 GitHub 아이디로 변경하세요

navbar-links:
  홈: ""
  GitHub: "https://github.com/your-github-id/n8n-blog"  # ← 본인 GitHub 아이디로 변경하세요
```

> `github-username`과 GitHub 링크 2곳을 본인 아이디로 바꾸세요.  
> 나머지 색상·테마 설정은 변경 불필요합니다.

### 4. n8n 워크플로우 연결

강사가 제공한 워크플로우 JSON을 n8n에 붙여넣고  
GitHub Credential과 레포 정보(owner, repository)를 본인 것으로 변경

## 폴더 구조

```
n8n-blog/
├── _config.yml        # 블로그 기본 설정 (제목·GitHub 아이디 수정 필요)
├── _posts/            # n8n이 자동으로 글을 여기 저장
├── _data/
│   └── posts.yml      # n8n이 자동으로 관리 (직접 수정 X)
├── assets/
│   └── css/
│       └── style.scss # 인디고 테마 디자인 (fortune cookie 애니메이션 포함)
└── index.md           # 블로그 홈 화면
```

## 디자인

Beautiful Jekyll 기반 인디고 테마

| 요소 | 값 |
|------|----|
| 배경색 | `#F4F4FA` (라이트 그레이) |
| 포인트색 | `#5B67E8` (인디고) |
| 네비게이션/푸터 | `#1A1C2E` (다크 네이비) |
| 카드 모서리 | `border-radius: 12px` |
| 폰트 | Noto Sans KR |
| 홈 애니메이션 | fortune cookie 🥠 float + star twinkle |

## 포스트 형식 (마크다운)

n8n이 자동으로 아래 형식으로 글을 만들어 `_posts/`에 저장합니다.

```markdown
---
layout: post
title: "글 제목"
date: 2026-06-25
categories: [AI]
---

## 서론

...

## 본론

...

## 결론

...
```
