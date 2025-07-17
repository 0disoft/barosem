# 테마 토글 아이콘 가시성 및 모듈 임포트 문제 해결

## 1. 작업 개요

테마 토글 아이콘이 어두운 테마에서 보이지 않던 문제와 `lucide-svelte` 모듈 임포트 오류를 해결했습니다. `currentTheme` 변수의 반응성 문제와 `lucide-svelte`의 임포트 방식 및 Vite 설정 문제를 수정했습니다.

## 2. 변경된 파일 목록

- `src/lib/components/layout/Header.svelte`
- `vite.config.ts`
- `bun.lockb` (종속성 업데이트)

## 3. 특이사항 및 참고

- `Header.svelte`에서 `currentTheme` 변수를 `$state('')`로 선언하여 Svelte 5의 반응성 문제를 해결했습니다.
- `lucide-svelte` 아이콘 임포트 방식을 `lucide-svelte/icons/sun` 및 `lucide-svelte/icons/moon`으로 변경했습니다.
- `vite.config.ts`에 `optimizeDeps.include: ['lucide-svelte']`를 추가하여 Vite가 `lucide-svelte`를 제대로 번들링하도록 설정했습니다.
- 아이콘의 시인성 향상을 위해 `text-foreground` 클래스를 추가했습니다.
