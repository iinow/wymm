# wymm 💍

프로포즈용 단일 페이지 (GitHub Pages 배포용)

## 1) 영상 준비 (Google 포토에서)

1. Google 포토에서 원하는 영상 선택
2. `다운로드` 해서 이 폴더로 가져오기
3. 파일명을 아래처럼 맞추기:

```bash
mkdir -p assets
mv "내영상파일명.mp4" assets/proposal.mp4
```

## 2) (선택) 썸네일 포스터 만들기

`ffmpeg`가 있으면:

```bash
ffmpeg -i assets/proposal.mp4 -ss 00:00:02 -frames:v 1 assets/poster.jpg
```

없으면 poster.jpg 없이도 동작함(브라우저가 첫 프레임 사용).

## 3) GitHub repo 연결/푸시

```bash
git init
git add .
git commit -m "Initial proposal page"
git branch -M main
git remote add origin https://github.com/iinow/wymm.git
git push -u origin main
```

## 4) GitHub Pages 켜기

GitHub repo → **Settings → Pages**
- Source: `Deploy from a branch`
- Branch: `main` / `/ (root)`

저장 후 1~3분 기다리면:
- `https://iinow.github.io/wymm/`

## 커스텀 문구 수정

`index.html`에서 아래 텍스트 바꾸면 됨:
- `Will you marry me? 💍`
- `우리의 순간들을 담은 작은 영화`
- `너와 평생을 함께하고 싶어`
