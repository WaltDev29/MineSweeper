# 💣Mine Sweeper (WEB ver.) 

이 프로젝트는 지뢰찾기 게임을 웹 기반으로 구현한 것입니다.  

<br>

## 🛠 기술스택
- HTML
- CSS
- JavaScript

<br>

## 📝주요코드
### Tile Class
```js
class Tile {
    constructor(mine, near, check) {
        // 기본 속성
        this.mine = mine;
        this.near = near;
        this.check = check;
        // 요소 생성
        this.div = document.createElement("span");
        this.div.classList.add("tile");
        this.div.addEventListener("click", () => {
            tileClicked(this);
        });
        // 우클릭 이벤트
        this.div.addEventListener("contextmenu", (e) => {
            e.preventDefault();

            if (flag != 0) return;
            if (this.check === 1) return;

            if (this.div.textContent === "🚩") {
                this.div.textContent = "";
            } else {
                this.div.textContent = "🚩";
            }
        });
    }
}
```

<br>

## 🎬 시연 영상 (GIF)

![지뢰찾기 시연](https://github.com/user-attachments/assets/a94a7c13-cb50-4d0b-90d1-26d06fbdc9d1)

---

<br><br>

## 🖥️ 상세 사진

### 👾기본 화면
![Image](https://github.com/user-attachments/assets/9e3ce25e-9be2-4979-9a24-96ce3100e783)

### 🧱필드 생성 시
![Image](https://github.com/user-attachments/assets/55babeec-c177-493d-bd4e-99b3c80b1dce)

### 💀지뢰 찾기 실패
![Image](https://github.com/user-attachments/assets/33b64261-86ae-4077-aa56-0e110f1a7baf)

### 🎉게임 클리어
![Image](https://github.com/user-attachments/assets/49dd95ed-9db1-457d-a69a-883363acfe69)

---

## 📂 기타

- 실행은 브라우저에서 `index.html`을 열어 확인 가능합니다.
- 제작 날짜 : 2025.04.12
