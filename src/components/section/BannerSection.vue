<template>
    <section id="bannerType" class="banner__wrap" :class="attr">
        <h2 class="blind">배너 영역</h2>
        <div class="banner__inner">
            <h3 class="title">{{ banners[0].h3 }}</h3>
            <p class="desc">
                {{ banners[0].p }}
                <a href="#" title="새로운 페이지 열림" target="_blank">{{ banners[0].mail }}</a>
            </p>
            <span class="small">{{ banners[0].span }}</span>
        </div>
    </section>
</template>
<script>
export default {
    props: {
        attr: String,
    },

    data: function () {
        return {
            banners: [
                {
                    h3: "Daily Perfume",
                    p: "따스한 일요일 아침 화이트 셔츠의 두근거리는 설렘",
                    mail: "sshin4882.tistory.com",
                    span: "SSHINY PERFUME",
                },
            ],
        };
    },
};
</script>
<style>
.banner__inner {
    background-image: url(../../assets/img/banner_bg01_1.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    text-align: center;
    padding: 120px 0;
    color: white;
}
.banner__inner .title {
    font-size: 50px;
    line-height: 1;
    font-weight: 300;
    margin-bottom: 40px;
}
.banner__inner .desc {
    font-size: 24px;
    line-height: 1.5;
    font-weight: 300;
    margin-bottom: 70px;
}
.banner__inner .desc a {
    color: white;
    display: block;
    width: fit-content;
    margin: 0 auto;
}
.banner__inner .desc a:hover {
    text-decoration: underline;
    text-shadow: 1px 0px 3px blanchedalmond;
}
.banner__inner .small {
    font-size: 16px;
    text-decoration: underline;
}

@media (max-width: 768px) {
    .banner__inner .title {
        font-size: 40px;
    }
    .banner__inner .desc {
        font-size: 18px;
    }
    .banner__inner .small {
        font-size: 14px;
    }
    .banner__inner .desc a {
        font-size: 17px;
    }
}

@media (max-width: 480px) {
    .banner__inner {
        padding-left: 20px;
        padding-right: 20px;
        box-sizing: border-box;
    }
    .banner__inner .title {
        font-size: 30px;
    }
    .banner__inner .desc {
        font-size: 16px;
        word-break: keep-all;
    }
    .banner__inner .small {
        font-size: 13px;
    }
    .banner__inner .desc a {
        font-size: 16px;
    }
}
</style>
