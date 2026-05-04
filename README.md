# 한국 라디오 PWA

GitHub Pages에 올려서 휴대폰에서 앱처럼 쓰는 국내 라디오 앱입니다.

## 파일 구성

- `index.html` : 앱 본문
- `manifest.webmanifest` : 모바일 홈 화면 추가용 설정
- `service-worker.js` : 앱 껍데기 캐시
- `icon.svg` : 앱 아이콘

## GitHub Pages 배포 방법

1. GitHub에서 새 저장소를 만듭니다. 예: `korea-radio`
2. 이 폴더 안의 파일 4개를 저장소 최상단에 업로드합니다.
3. 저장소 메뉴에서 `Settings` → `Pages`로 갑니다.
4. `Build and deployment`에서 Source를 `Deploy from a branch`로 선택합니다.
5. Branch를 `main` / `/root`로 선택하고 Save 합니다.
6. 잠시 뒤 표시되는 Pages 주소로 접속합니다.

## 휴대폰에서 앱처럼 쓰기

### 아이폰 Safari
1. Pages 주소 열기
2. 공유 버튼
3. `홈 화면에 추가`

### 안드로이드 Chrome
1. Pages 주소 열기
2. 오른쪽 위 점 3개
3. `홈 화면에 추가` 또는 `앱 설치`

## 채널 추가 방법

`index.html` 안의 `stations` 배열에 아래처럼 추가하면 됩니다.

```js
{ name: "채널명", group: "그룹", desc: "설명", icon: "아이콘글자", accent: "#ffd479", query: "stn=ebs" }
```

라디오 주소는 `https://radio.bsod.kr/stream/?` 뒤의 쿼리만 `query`에 넣으면 됩니다.

예:
- `stn=kbs&ch=1radio`
- `stn=mbc&ch=fm4u`
- `stn=sbs&ch=powerfm`
- `stn=ebs`

## 참고

일부 라디오는 브라우저 정책이나 방송사 스트림 정책 때문에 바로 재생이 안 될 수 있습니다.
그럴 때 앱 안의 `새창 플레이어` 또는 `보조재생`을 누르면 됩니다.
