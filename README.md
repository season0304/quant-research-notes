# Quant Research Notes

한국어로 읽고 기록하는 논문 리뷰 노트입니다. 논문의 핵심 질문을 수식과 구현 관점에서 다시 정리하고, 재현 가능한 실험 설계와 한계를 함께 기록합니다.

## 구조

- `index.html`: GitHub Pages 정적 홈
- `posts/`: 게시물 원문과 재사용 템플릿
- `styles.css`: 반응형 스타일
- `script.js`: 검색·카테고리 필터와 홈 카드 목록
- `about.qmd`: Quarto 원본 About
- `.github/workflows/pages.yml`: GitHub Pages 자동 배포

## 새 리뷰 추가

1. `posts/review-template.md`를 복사해 `posts/your-slug.md`로 저장합니다.
2. 질문, 핵심 아이디어/방정식, 구현/재현, 한계, 응용, 참고문헌을 채웁니다.
3. 검증하지 않은 수치나 결과는 쓰지 말고, 실행한 코드·환경·데이터 출처를 명시합니다.
4. `script.js`의 `posts` 배열에 제목, 날짜, 카테고리, 요약, 링크를 추가합니다. 홈 카드는 파일을 자동 검색하지 않으므로 이 한 곳을 함께 수정해야 합니다.

## 로컬 미리보기

Quarto가 설치되어 있다면:

```bash
quarto preview
```

정적 미리보기:

```bash
python -m http.server 8000
```

## 배포

`main`에 push하면 Actions가 Quarto를 렌더하고 손작성 정적 shell을 `_site`에 조립한 뒤 Pages artifact로 배포합니다. 저장소 설정에서 Pages의 Source를 **GitHub Actions**로 선택해야 합니다. workflow는 `contents: read`, `pages: write`, `id-token: write`만 사용합니다.

## 저자 정보

콘텐츠와 메타데이터에는 개인 실명이나 개인 이메일을 넣지 않습니다. GitHub 계정과 커밋 화면의 식별 정보는 계정 설정에 따라 별도로 보일 수 있습니다.
