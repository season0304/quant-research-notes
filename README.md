# Quant Research Notes

한국어 기술 노트와 논문 리뷰를 Quarto로 발행하는 작은 블로그입니다.

## 새 글 추가

1. `posts/`에 새 `.qmd` 또는 Markdown 파일을 만듭니다.
2. 다음 front matter를 채웁니다.

```yaml
---
title: "글 제목"
date: "2026-10-13"
description: "한 줄 요약"
categories: ["기술"] # 또는 ["논문 리뷰"]
---
```

3. 논문 리뷰라면 `posts/review-template.md`의 질문, 핵심 아이디어/방정식, 구현/재현, 한계, 응용, 참고문헌 구조를 따릅니다.
4. `index.qmd`의 Quarto listing이 `posts/`를 자동으로 읽어 최신순 목록, 검색, 카테고리 필터에 반영합니다. 홈용 `script.js` 배열을 따로 수정할 필요가 없습니다.

## 로컬 미리보기

```bash
quarto preview
```

정적 미리보기만 필요하면:

```bash
python -m http.server 8000
```

## 배포

`main`에 push하면 GitHub Actions가 Quarto를 렌더하고 `_site`를 GitHub Pages에 배포합니다. 저장소 Settings → Pages에서 Source를 **GitHub Actions**로 설정해야 합니다.

workflow 권한은 `contents: read`, `pages: write`, `id-token: write`로 제한되어 있습니다.

## 개인정보

콘텐츠와 메타데이터에는 개인 실명이나 개인 이메일을 넣지 않습니다. GitHub 계정과 커밋 화면의 식별 정보는 계정 설정에 따라 별도로 보일 수 있습니다.
