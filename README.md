# 💣Mine Sweeper

이 프로젝트는 지뢰찾기 게임을 웹 기반으로 구현한 것입니다.  

##### 제작날짜 2025.04.12

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

![지뢰찾기 플레이](https://github.com/user-attachments/assets/463060a4-5086-47ee-9bc7-4b38c915c7a5)

---

<br>

## 🖥️ 상세 사진
|Description|Image|
|--|--|
|기본 화면|<img src="https://github.com/user-attachments/assets/ab499d14-be7e-4d54-bc92-f1d146220e48">|  
|필드 생성 시|<img src="https://github.com/user-attachments/assets/3c4cc947-4e91-40b4-b8ca-cf15b3d53f4b">|
|지뢰 찾기 실패|<img src="https://github.com/user-attachments/assets/1738d77d-4e45-40f2-b800-8c9fc6426594">|
|게임 클리어|<img src="https://github.com/user-attachments/assets/5563fb65-e96d-49cb-84e1-b019b2e8f1e2">|

---
<br>

## 🎮 플레이해 보세요!
<br>

👉 [**Legend of Poly 지금 플레이하기** 🚀](https://waltdev29.github.io/LegendOfPoly/)

<br>

## 📃 라이선스

본 프로젝트는 자유롭게 수정/재배포할 수 있습니다. 학습 및 개인 포트폴리오 용도로 사용 가능합니다.  
