# utils

브라우저에서 쓰는 작은 도구 모음입니다. 정적 파일은 `docs/`에 두고 [GitHub Pages](https://docs.github.com/pages)로 호스팅합니다.

## GitHub Pages 설정

1. 저장소 **Settings → Pages**
2. **Build and deployment**에서 **Branch**를 `main`으로, 폴더는 **`/docs`** 를 선택합니다.

게시 후 사이트 URL은 보통 `https://<사용자명>.github.io/utils/` 형태입니다. (저장소 이름이 `utils`일 때)

## 유틸 목록

진입 허브는 [`docs/index.html`](docs/index.html)이며, 아래는 용도별 분류와 동일한 순서입니다.

| 분류 | 경로 | 설명 |
|------|------|------|
| 시간 | [`docs/time-diff/`](docs/time-diff/) | 두 시각의 차이 (B − A), `YYYY-MM-DD HH:MM:SS` 또는 `HH:MM:SS` |
| 시간 | [`docs/time-convert/`](docs/time-convert/) | 초 ↔ 분·초 ↔ 시·분·초 ↔ 일·시·분·초 단위 변환 (한쪽 수정 시 나머지 동기화) |
| 시간 | [`docs/run-pace/`](docs/run-pace/) | 달리기 km/h ↔ km당 페이스 ↔ 5·10km·하프·풀 예상 완주 시간 상호 변환 |
| 계산 | [`docs/percent-change/`](docs/percent-change/) | A → B로 바뀔 때 몇 % 증가·감소인지 `((B − A) ÷ A × 100)` |
| 계산 | [`docs/salary-tax/`](docs/salary-tax/) | 연봉·세전·세후 월급 상호 환산(추정 세액), 통계청 평균 임금·건강보험료 참고, 과세표준 누진 세액 |
| 데이터 · 시각화 | [`docs/venn-sets/`](docs/venn-sets/) | 네 칸에 항목을 넣고(줄 단위), 비어 있지 않은 집합만으로 Venn·영역별 목록 |
| 데이터 · 시각화 | [`docs/stats-boxplot/`](docs/stats-boxplot/) | 숫자 목록(두 칸) → 요약 통계·박스플롯, 두 그룹이면 Welch t·Mann–Whitney U |
| 데이터 · 시각화 | [`docs/sequence-align/`](docs/sequence-align/) | 두 문자열 전역 정렬(Needleman–Wunsch), 갭·일치 표시·최적 점수 |
| 텍스트 · 기호 | [`docs/symbols/`](docs/symbols/) | UTF-8 화살표·수학 기호·체크·이모지 등 카테고리별 클릭으로 클립보드 복사 |
| 텍스트 · 기호 | [`docs/password-gen/`](docs/password-gen/) | 길이·문자 종류 선택, `crypto.getRandomValues`로 임시 비밀번호 생성·복사(서버 미전송) |
| 바코드 · QR | [`docs/barcode-qr/`](docs/barcode-qr/) | 같은 문자열로 1D 바코드(CODE128·CODE39·EAN-13)와 QR 생성·SVG/PNG 저장 |
| 바코드 · QR | [`docs/barcode-scan/`](docs/barcode-scan/) | 카메라 실시간 인식 또는 이미지 파일로 QR·1D 바코드 읽기 |

## 로컬에서 미리보기

`docs`를 웹 루트로 서빙합니다.

```bash
cd docs && python3 -m http.server 8080
```

브라우저에서 `http://127.0.0.1:8080/` 로 열면 허브가 보입니다. 예: `/time-diff/`, `/barcode-qr/`, `/symbols/`, `/password-gen/` 등.
