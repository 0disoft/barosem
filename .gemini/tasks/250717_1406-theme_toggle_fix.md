# 테마 토글 기능 수정

## 1. 작업 개요

`Toggle Theme` 버튼이 작동하지 않던 문제를 해결했습니다. `app.css`에서 `.dark` 클래스를 사용하여 테마를 관리하는 방식에 맞춰 `+layout.svelte`의 테마 토글 로직을 수정했습니다.

## 2. 변경된 파일 목록

- `src/routes/+layout.svelte`

## 3. 특이사항 및 참고

- `document.documentElement.setAttribute('data-theme', ...)` 방식 대신 `document.documentElement.classList.toggle('dark')`를 사용하여 CSS 클래스 토글 방식으로 변경했습니다.
