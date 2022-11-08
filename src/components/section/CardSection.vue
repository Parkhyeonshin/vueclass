<template>
    <section id="cardType" class="card__wrap" :class="attr">
        <h2>{{ CardTypes[0].h2 }}</h2>
        <p>{{ CardTypes[0].p }}</p>
        <div class="card__inner" :class="layout">
            <article class="card" v-for="card in Cards" v-bind:key="card.cardInner">
                <figure class="card__header">
                    <img :src="card.img" alt="외형에 대한 오해 이미지" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">{{ card.tit }}</h3>
                    <p class="desc">
                        {{ card.desc }}
                    </p>
                    <a class="btn" href="#">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="35" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
            <!-- <article class="card">
                <figure class="card__header">
                    <img src="../../assets/img/card_bg01_02_1.jpg" alt="도베르만의 성격 이미지" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">무더운 날씨에도 꽃피우는 향기</h3>
                    <p class="desc">
                        청량한 느낌이 낯설다면, 아마 이 향수가 없어서가 아닐까요?
                        <br />고객님들이 사랑해주신 이 향수 <br />당신과 어울리는 밝고 신선한 향을 선사해드립니다.
                    </p>
                    <a class="btn" href="#">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="35" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
            <article class="card">
                <figure class="card__header">
                    <img src="../../assets/img/card_bg01_03_1.jpg" alt="도베르만을 키울때 주의할 점 이미지" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">Very Royal Cactus</h3>
                    <p class="desc">
                        오가닉 버베나와 선인장 추출물이 조화를 이루는 향으로 여름 갈증을 해소하는 이국적이고 상쾌한 기운을 느낄 수 있습니다.
                        <br />여름과 어울리는 밝고 신선한 향을 선사합니다.
                    </p>
                    <a class="btn" href="#">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="35" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article> -->
        </div>
    </section>
</template>
<script>
export default {
    props: {
        attr: String,
        layout: String,
    },

    data: function () {
        return {
            CardTypes: [
                {
                    h2: "선인장에서 추출한 이국적 향",
                    p: "지중해 연안을 상징하는 선인장 열매인 프리클리 페어를 메인으로 시작되는 BSET EDITION",
                },
            ],
            Cards: [
                {
                    img: "../../assets/img/card_bg01_01_1.jpg",
                    tit: "Cactus",
                    desc: "오가닉 버베나와 선인장 추출물이 조화를 이루는 향으로 여름 갈증을 해소하는 이국적이고 상쾌한 기운을 느낄 수 있습니다.\n 여름과 어울리는 밝고 신선한 향을 선사합니다.",
                },
                {
                    img: "../../assets/img/card_bg01_02_1.jpg",
                    tit: "무더운 날씨에도 꽃피우는 향기",
                    desc: "청량한 느낌이 낯설다면, 아마 이 향수가 없어서가 아닐까요?\n고객님들이 사랑해주신 이 향수 <br />당신과 어울리는 밝고 신선한 향을 선사해드립니다.",
                },
                {
                    img: "../../assets/img/card_bg01_03_1.jpg",
                    tit: "Very Royal Cactus",
                    desc: "오가닉 버베나와 선인장 추출물이 조화를 이루는 향으로 여름 갈증을 해소하는 이국적이고 상쾌한 기운을 느낄 수 있습니다.\n여름과 어울리는 밝고 신선한 향을 선사합니다.",
                },
            ],
        };
    },
};
</script>
<style>
#cardType > h2 {
    word-break: keep-all;
}
.card__inner {
    display: flex;
    justify-content: space-between;
}

.card {
    width: 32%;
    background: #f5f5f5;
    border: 2px solid black;
}
.card__header {
    border-bottom: 2px solid black;
    overflow: hidden;
}
.card__header img:hover {
    transform: scale(1.1);
    transition: all 0.3s ease-in;
    filter: brightness(110%) contrast(110%);
    cursor: pointer;
}
.card__header img:not(:hover) {
    transition: all 0.5s;
}
.card__body {
    padding: 24px;
    background-color: snow;
}
.card__body .tit {
    font-size: 24px;
    margin-bottom: 10px;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
.card__body .desc {
    font-size: 18px;
    line-height: 1.4;
    color: #666;
    margin-bottom: 20px;
    font-weight: 300;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
}
.card__body .btn {
    position: relative;
}
.card__body .btn:hover span svg {
    width: 65px;
    transition: width 0.5s ease-in;
}
.card__body .btn:hover ::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 60%;
    height: 10px;
    background-color: #f8c3614b;
    border-radius: 50px;
}
@media (max-width: 768px) {
    .card__inner {
        display: block;
        justify-content: space-between;
    }
    .card {
        width: 100%;
        background: #f5f5f5;
        margin-bottom: 10px;
    }
}
@media (max-width: 480px) {
    .card__body {
        padding: 13px;
    }
    .card__body .tit {
        font-size: 22px;
    }
    .card__body .desc {
        font-size: 16px;
        margin-bottom: 3px;
    }
    .card__body .btn {
        font-size: 14px;
    }
}
</style>
