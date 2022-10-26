<template>
    <section id="imgType" class="image__wrap" :class="attr">
        <h2>화사한 봄꽃처럼</h2>
        <p>햇살이 반기는 맑은 하늘과 포근한 공기, 그 사이로 스며든 기분 좋은 향조들.</p>
        <div class="image__inner image__box" :class="layout">
            <article class="image img1">
                <h3 class="image__title">SPRING COOLTON</h3>
                <p class="image__desc">
                    연분홍빛 꽃을 닮은 부드럽고 사랑스러운 향기.
                    <br />로즈와 스위트 재스민삼박, 프리지어의 폭발적인 달콤함을 느낄 수 있습니다.
                </p>
                <a class="image__btn" href="#" title="자세히 보기">자세히 보기</a>
            </article>
            <article class="image img2">
                <h3 class="image__title">FLOWER BOM</h3>
                <p class="image__desc">
                    생동감이 폭발하는 봄을 닮은 향수.
                    <br />아이리스와 은방울꽃으로 시작해 센티폴리아 로즈, 우드 노트로 끝나는 향기를 느껴보세요.
                </p>
                <a class="image__btn yellow" href="#" title="자세히 보기">자세히 보기</a>
            </article>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        attr: String,
        layout: String,
    },
};
</script>

<style>
.image__inner {
    display: flex;
    justify-content: space-between;
}
.image {
    width: 49%;
    color: #fff;
    padding: 200px 30px 30px 30px;
    box-sizing: border-box;
}
.image.img1 {
    background: url(../../assets/img/image_type01_01_1.jpg) no-repeat center;
    background-size: cover;
    border-radius: 8px;
    box-sizing: border-box;
}
.image.img2 {
    background: url(../../assets/img/image_type01_02_1.jpg) no-repeat center;
    background-size: cover;
    border-radius: 8px;
    box-sizing: border-box;
}
.image__title {
    font-size: 32px;
    margin-bottom: 10px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.image__desc {
    font-size: 16px;
    margin-bottom: 10px;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    font-weight: 300;
}
.image__btn {
    font-size: 16px;
    color: #fff;
    background-color: #c38687;
    border-radius: 20px;
    display: inline-block;
    padding: 10px 20px;
}
.image__btn:hover {
    background-color: #eeaeaf;
    transition: all 0.3s ease;
}

.image__btn.yellow {
    background-color: #ab675f;
}
.image__btn.yellow:hover {
    background-color: #ee9187;
}
@media (max-width: 768px) {
    .image__inner {
        display: block;
    }
    /* .image{
        width: 49%;
        height: 300px;
        padding: 100px 30px 30px 30px;
        display: flex;
        align-items:flex-end;
        align-content: flex-end;
        flex-wrap: wrap;
    } */
    /* .image.img1 {
        margin-right: 4px;
        padding: 8px;
    } */
    .image__title {
        font-size: 25px;
    }

    .image__btn,
    .image__btn.yellow {
        font-size: 14px;
        padding: 8px 15px;
    }
}
@media (max-width: 480px) {
    .image__inner {
        display: block;
    }
    .image__desc {
        font-size: 15px;
    }
}
</style>
