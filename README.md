# 황촌 마을호텔 숙소 안내 페이지 — 깃허브 페이지 배포 안내

## 폴더 구성
- `index.html` — 숙소 안내 페이지 (34개 숙소 전체)
- `photos/` — 숙소 사진 파일들

## 깃허브 페이지로 올리는 방법

1. github.com 에서 새 저장소(Repository)를 만듭니다. (예: `hwangchon-hotel`)
   - Public(공개)으로 설정해야 외부에서 접속 가능합니다.
2. 이 폴더 안의 `index.html`과 `photos` 폴더 전체를 저장소에 업로드합니다.
   - 저장소 페이지에서 "Add file" → "Upload files"로 드래그 앤 드롭하면 됩니다.
3. 저장소의 Settings → Pages 메뉴로 이동합니다.
4. "Source"를 "Deploy from a branch"로 설정하고, 브랜치는 `main`(또는 `master`), 폴더는 `/ (root)`로 선택 후 저장합니다.
5. 몇 분 뒤 `https://[깃허브아이디].github.io/[저장소이름]/` 주소로 접속하면 페이지가 뜹니다.
   - 예: 저장소 이름이 `hwangchon-hotel`이고 깃허브 아이디가 `happyhwangchon`이면
     `https://happyhwangchon.github.io/hwangchon-hotel/`

## 이후 수정 방법
- `index.html` 파일 안의 `const accommodations = [...]` 부분에서 각 숙소의 이름, 주소, 인원, 요금, 연락처, 예약링크, 사진 경로를 직접 수정할 수 있습니다.
- 사진을 교체하려면 `photos` 폴더에 새 파일을 넣고, `index.html`의 해당 숙소 `photos` 배열 값을 그 파일명으로 바꾸면 됩니다.
- 수정 후에는 깃허브 저장소에 파일을 다시 업로드(또는 커밋)하면 1~2분 내로 사이트에 반영됩니다.

## 로고/브랜딩
- 이 방식은 클로드(Anthropic) 로고 없이, 조합 자체 도메인(원하시면 커스텀 도메인 연결도 가능)과 파비콘으로 운영할 수 있습니다.
- 파비콘은 `index.html`의 `<head>` 안 `<link rel="icon" ...>` 부분을 원하는 이미지로 교체하면 바뀝니다.
