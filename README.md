<p align="middle">
    <img width="200px"; src="./icons/Netflix_Logo_PMS.png">
</p>

<h2 align='middle'> NETFLEX CLONE CODEING <h2>

---

> 해당 레포지토리는 교육용으로 만들어졌으며 어떠한 상업적 용도를 취하지 않습니다.

## 🖥️ Projects!

---
### 🥇 Step 1. 블러 그라디언트 구현하기

<p align="middle">
    <img width="200px"; src="./Step1.png">
</p>

- 강의 중 배우지 않았던 블러가 그라디언트 방식으로 되어있는 부분 발견
- HTML : 메인 사진 이미지 클래스 아래에 blur-overlay 요소 추가
```html
<main class="main">
        <div class="top-section">
            <img class="mainimg" src="Main/moneyheist.jpg">
            <div class="blur-overlay"></div>
            <div class="main-info">
                <p class="main-title">
                    Money Heist
                </p>
                <button class="play">
                    Play
                </button>
                <button class="MyList">
                    My List
                </button>
                <p class="description">
                    To carry out the biggest heist in history, a mysterious man<br>
                    called The Professor recruits a band of eight robbers who<br>
                    have a single characteristic: n…
                </p>
            </div>
        </div>
    </main>
```
- CSS : main의 position을 relative로 설정해주고, blur-overlay의 position을 absolute로 설정 해줌
- background-image에 linear-gradient를 추가하여 to top(위로 갈수록) rgba 두 값의 투명도를 1과 0으로 맞추어 사용함

```css
.main {
    height: 455px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    position: relative;

}

.blur-overlay {
    position: absolute;
    bottom: 0%;
    left: 0;
    right: 0;
    height: 150px;
    background-image: linear-gradient(to top, rgba(25, 25, 25, 1), rgba(25, 25, 25, 0));
}
```

---
### 🥈Step 2. hover 값 주기

- 과제가 사진으로 주어졌기 때문에 고민했는데, 실제 넷플릭스라면 hover값이 있을 것으로 판단하여 진행
- .play와 .MyList 요소에 각각 cursor 값을 pointer로 주고 play:hover와 MyList:hover에 버튼과 유사한 색상인 rgb(80, 80, 80) 값을 넣어줌.

```css
.play {
    background-color: rgba(96, 95, 95, 0.3);
    color: white;
    border-radius: 2px;
    border: none;
    width: 90px;
    height: 30px;
    font-size: 12px;
    margin-right: 15px;
    cursor: pointer;
}

.MyList {
    background-color: rgba(96, 95, 95, 0.3);
    color: white;
    border-radius: 2px;
    border: none;
    width: 100px;
    height: 30px;
    font-size: 12px;
    cursor: pointer;
}

.play:hover {
    background-color: rgb(80, 80, 80);
}

.MyList:hover {
    background-color: rgb(80, 80, 80);
}
```

### 🥁결과화면

---

<img src="./2023-10-18 pm 2.48.29.png">
