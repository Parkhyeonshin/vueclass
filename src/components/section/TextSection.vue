<template>
    <section id="textType" class="text__wrap" :class="attr">
        <span class="blind">텍스트 유형01</span>
        <h2 class="mb70">ABOUT US</h2>
        <div class="text__inner" :class="layout">
            <div class="text t1">
                <h3 class="text__title">글루텐 프리</h3>
                <p class="text__desc">알레르기를 유발할 수 있는 글루텐을 넣지 않음으로써, 남녀노소 모두가 쓸 수 있는 향수를 만듭니다.</p>
                <a class="text_btn" href="#">더보기</a>
            </div>
            <div class="text t2">
                <h3 class="text__title">비건 향수</h3>
                <p class="text__desc">
                    끗한 향수를 만들어 믿고 사용할 수 있는 제품을 만드는데 힘쓰고 있습니다. 친환경 원료만 사용해서 만든 대표적인 비건 향수입니다.
                </p>
                <a class="text_btn" href="#">더보기</a>
            </div>
            <div class="text t3">
                <h3 class="text__title">크룰티 프리</h3>
                <p class="text__desc">동물 실험을 거치지 않고 만들어지는 향수입니다. 생명을 소중히 하며 윤리적인 기업이 되고자 노력하고 있습니다.</p>
                <a class="text_btn" href="#">더보기</a>
            </div>
            <div class="text t4">
                <h3 class="text__title">리사이클러블</h3>
                <p class="text__desc">
                    자연을 침해하지 않는 범위 내에서 만들어진 클린의 제품들은 사용 후 다시 그대로 자연으로 돌아가는 전제품 ‘리사이클러블’을 추구하고
                    있습니다.
                </p>
                <a class="text_btn" href="#">더보기</a>
            </div>
            <div class="text t5">
                <h3 class="text__title">환경친화</h3>
                <p class="text__desc">최초 환경친화적인 지속 가능한 원료를 사용하여 깨끗한 지구 만들기에 앞장서고 있습니다.</p>
                <a class="text_btn" href="#">더보기</a>
            </div>
            <div class="text t6">
                <h3 class="text__title">지속가능성</h3>
                <p class="text__desc">자연과 환경을 사랑하는 우리는 천연자원의 고갈을 피하기 위해 지속 가능한 원료를 사용합니다.</p>
                <a class="text_btn" href="#">더보기</a>
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
};
</script>
<style>
/* textType */
.text__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.text {
    width: 32%;
    margin-bottom: 2%;
    padding: 20px;
    box-sizing: border-box;
    border-radius: 10px;
    transition: background 0.4s;
    overflow: hidden;
}
.text:hover {
    background-color: #e9e9e9;
}
.text__title {
    font-size: 24px;
    line-height: 1;
    margin-bottom: 10px;
    white-space: nowrap;
    text-overflow: ellipsis;
    position: relative;
    padding-top: 75px;
}
.text__title::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 60px;
    height: 60px;
    background: url(../../assets/img/SITE01_ICON.svg);
    border-radius: 50%;
}
.text.t1 .text__title::before {
    background-position: 0 0;
}
.text.t2 .text__title::before {
    background-position: -100px 0;
}
.text.t3 .text__title::before {
    background-position: -200px 0;
}
.text.t4 .text__title::before {
    background-position: -300px 0;
}
.text.t5 .text__title::before {
    background-position: -400px 0;
}
.text.t6 .text__title::before {
    background-position: -500px 0;
}
.text__desc {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.4;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    color: #666;
    margin-bottom: 20px;
}
.text_btn {
    font-size: 16px;
    line-height: 1;
    text-decoration: underline;
    text-underline-position: under;
    color: #666;
}

@media (max-width: 768px) {
    .text__inner {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .text {
        width: 49%;
    }
}
@media (max-width: 480px) {
    .text__inner {
        display: block;
    }
    .text {
        width: 100%;
    }
    .text__title {
        font-size: 20px;
    }
    .text__title::before {
        transform: scale(0.8);
        left: -5px;
    }
    .text__desc {
        font-size: 16px;
    }
}
</style>
