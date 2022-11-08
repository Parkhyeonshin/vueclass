<template>
    <section id="imgTextType" class="imgText__wrap" :class="attr">
        <h2 class="blind">유용한 사이트 살펴보기</h2>
        <div class="imgText__inner" :class="layout">
            <div class="imgText__txt">
                <span class="blind">이미지 텍스트 유형01</span>
                <h3>
                    {{ ImgTexts[0].h3 }}
                </h3>
                <p>{{ ImgTexts[0].p }}</p>
                <ul>
                    <li>
                        <a href="#">{{ ImgTexts[0].li }}</a>
                    </li>
                    <li>
                        <a href="#">{{ ImgTexts[0].li2 }}</a>
                    </li>
                    <li>
                        <a href="#">{{ ImgTexts[0].li3 }}</a>
                    </li>
                    <li>
                        <a href="#">{{ ImgTexts[0].li }}</a>
                    </li>
                    <li>
                        <a href="#">{{ ImgTexts[0].li2 }}</a>
                    </li>
                    <li>
                        <a href="#">{{ ImgTexts[0].li3 }}</a>
                    </li>
                </ul>
            </div>
            <div class="imgbox">
                <div class="imgText__img" :class="imgBox.divClass" v-for="imgBox in ImgBox" v-bind:key="imgBox.imgBox">
                    <a href="#" :class="aClass">{{ imgBox.text }}</a>
                </div>
                <!-- <div class="imgText__img img1">
                    <a href="#">PERSONAL</a>
                </div>
                <div class="imgText__img img2">
                    <a href="#" class="blue">CUSTOM</a>
                </div> -->
            </div>
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
            ImgTexts: [
                {
                    h3: "당신의 향수에\n만족하시나요?",
                    p: "수 만개의 향수 중 당신의 향수를 찾는 것\n그것은 운명과도 같은 일입니다.",
                    li: "당신만의 향수",
                    li2: "무료로 시향하세요",
                    li3: "당일 주문 / 당일 출고",
                },
            ],
            ImgBox: [
                {
                    divClass: "img1",
                    aClass: "",
                    text: "PERSONAL",
                },
                {
                    divClass: "img2",
                    aClass: "blue",
                    text: "CUSTOM",
                },
            ],
        };
    },
};
</script>

<style>
.imgText__inner {
    display: flex;
    justify-content: space-between;
}
/* .imgText__inner > div {
    height: 500px;
} */
.imgText__txt {
    width: 30%;
}
.imgbox {
    width: 69%;
    display: flex;
    justify-content: space-between;
}
.imgText__txt span {
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 20px;
    display: block;
}
.imgText__txt h3 {
    font-size: 50px;
    font-weight: normal;
    word-break: keep-all;
    line-height: 1.4;
    margin-bottom: 20px;
}
.imgText__txt p {
    font-size: 22px;
    font-weight: 300;
    line-height: 1.5;
    color: #666;
    margin-bottom: 10px;
}
.imgText__txt ul {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
    margin-left: 20px;
}
.imgText__txt ul li {
    position: relative;
    padding-left: 0px;
    list-style: disc;
}
.imgText__txt ul li a {
    color: #666;
}
.imgText__txt ul li::before {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
    background: #666;
}
.imgText__txt ul li a:hover {
    text-decoration: underline;
}
.imgText__img {
    width: 49%;
    border-radius: 10px;
    position: relative;
}
.imgText__img a {
    position: absolute;
    left: 30px;
    bottom: 30px;
    background-color: #000;
    color: white;
    font-size: 18px;
    padding: 10px 30px;
    border-radius: 30px;
    display: inline-block;
}
.imgText__img a:hover {
    background-color: rgb(43, 43, 43);
    transition: all 0.3s ease;
}

.imgText__img.img1 {
    background: url(../../assets/img/imgText_bg01_1.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
    background: url(../../assets/img/imgText_bg02_1.jpg) no-repeat center / cover;
}

@media (max-width: 1080px) {
    .imgText__txt h3 {
        font-size: 35px;
    }

    .imgbox {
        width: 68%;
    }
}
@media (max-width: 768px) {
    .imgText__txt {
        width: 48%;
    }
    .imgText__txt h3 {
        word-break: break-all;
        font-size: 40px;
    }
    .imgText__txt p {
        font-size: 20px;
    }
    .imgbox {
        width: 50%;
        display: flex;
        flex-wrap: wrap;
    }
    .img1 {
        width: 100%;
        margin-bottom: 5%;
    }
    .img2 {
        width: 100%;
    }
}
@media (max-width: 480px) {
    .imgText__inner {
        display: block;
    }
    .imgText__inner > div {
        height: 250px;
    }
    div.imgText__txt {
        width: 100%;
        height: auto;
    }
    .imgText__txt h3 {
        font-size: 30px;
        text-align: center;
    }
    .imgText__txt p {
        font-size: 16px;
        text-align: center;
    }
    .imgText__txt > ul {
        display: none;
    }
    .imgbox {
        width: 100%;
        display: flex;
        justify-content: space-between;
    }
    .imgText__img {
        width: 49%;
    }

    .imgText__img.img1 a {
        font-size: 14px;
        left: 15%;
        bottom: 20px;
        padding: 5px 10px;
    }
    .imgText__img.img2 a {
        font-size: 14px;
        left: 20%;
        bottom: 20px;
        padding: 5px 10px;
    }
    .imgText__img.img1 {
        margin-bottom: 0;
    }
}
</style>
