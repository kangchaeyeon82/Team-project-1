# 우리 팀 취미 모음 🎨

팀원들이 각자 좋아하는 취미를 소개하는 사이트입니다.
홈(`index.html`)에서 팀원 카드를 누르면 각 팀원의 페이지로 이동합니다.

빌드 도구 없이 HTML / CSS 만으로 만들어져 있어서, `index.html` 을 브라우저로 열면 바로 볼 수 있습니다.

## 폴더 구조

```
index.html            홈 화면
assets/
  home.css            홈 화면 스타일
  members.js          팀원 목록 (홈 카드가 이걸로 만들어짐)
members/
  member1/            팀원 1 전용 폴더
    index.html
    style.css
  member2/ ...
```

## 내 페이지 꾸미는 법

1. `members/` 안에서 **내 폴더**를 찾습니다. (예: `members/member1`)
2. `index.html` 에서 이름, 취미, 소개글을 내 것으로 바꿉니다.
3. `style.css` 로 색, 글꼴, 배경 등을 마음대로 꾸밉니다.
4. 사진은 내 폴더 안에 `images/` 폴더를 만들어 넣고 `<img src="images/사진.jpg" alt="설명">` 으로 넣습니다.
5. `assets/members.js` 에서 내 줄의 `name`, `hobby`, `emoji`, `color` 를 바꾸면 홈 카드에 반영됩니다.

> 각자 **자기 폴더만** 수정하면 서로 충돌이 나지 않습니다.

## 팀원 추가하기

1. `members/member1` 폴더를 복사해서 `members/member5` 같은 새 이름으로 만듭니다.
2. `assets/members.js` 에 한 줄을 추가합니다.
   ```js
   { id: "member5", name: "팀원 5", hobby: "그림", emoji: "🎨", color: "#db2777" },
   ```

## 작업 흐름 (Git)

```bash
git pull                      # 최신 내용 받기
# ... 내 폴더 수정 ...
git add members/member1 assets/members.js
git commit -m "member1: 독서 페이지 꾸미기"
git push
```

## 웹에 공개하기 (GitHub Pages)

GitHub 저장소 → **Settings → Pages** → Branch 를 `main` / `/ (root)` 로 선택하고 저장하면
`https://kangchaeyeon82.github.io/Team-project-1/` 주소로 사이트가 열립니다.
