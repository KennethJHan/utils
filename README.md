# utils

브라우저에서 쓰는 작은 도구 모음입니다. 정적 파일은 `docs/`에 두고 [GitHub Pages](https://docs.github.com/pages)로 호스팅합니다.

## GitHub Pages 설정

1. 저장소 **Settings → Pages**
2. **Build and deployment**에서 **Branch**를 `main`으로, 폴더는 **`/docs`** 를 선택합니다.

게시 후 사이트 URL은 보통 `https://<사용자명>.github.io/utils/` 형태입니다. (저장소 이름이 `utils`일 때)

## 유틸 목록

| 경로 | 설명 |
|------|------|
| [`docs/time-diff/`](docs/time-diff/) | 두 시각의 차이 (B − A), `YYYY-MM-DD HH:MM:SS` 또는 `HH:MM:SS` |

## 로컬에서 미리보기

`docs`를 웹 루트로 서빙합니다.

```bash
cd docs && python3 -m http.server 8080
```

브라우저에서 `http://127.0.0.1:8080/` 로 열면 허브 페이지가 보이고, 시간 차 계산기는 `/time-diff/` 입니다.
