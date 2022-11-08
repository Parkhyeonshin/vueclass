<template>
    <section id="sliderType" class="slider__wrap" :class="attr">
        <h2 class="blind">슬라이드영역</h2>
        <div class="slider__inner">
            <swiper
                :spaceBetween="30"
                :centeredSlides="true"
                :autoplay="{
                    delay: 2500,
                    disableOnInteraction: false,
                }"
                :pagination="{
                    clickable: true,
                }"
                :navigation="true"
                :modules="modules"
                class="mySwiper"
            >
                <swiper-slide v-for="slide in Slide" v-bind:key="slide.slide">
                    <div className="desc">
                        <span>{{ slide.span }}</span>
                        <h3>{{ slide.h3 }}</h3>
                        <p>
                            {{ slide.p }}
                        </p>
                        <div className="btn">
                            <a href="/">자세히 보기</a>
                            <a href="/" :class="slide.aClass">제품 보기 </a>
                        </div>
                    </div>
                </swiper-slide>
                <!-- <swiper-slide>
                    <div className="desc">
                        <span>NEW Product</span>
                        <h3>SPRING SEASON</h3>
                        <p>
                            따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금
                            <br />
                            향기를 타고 봄이 다가온다
                        </p>
                        <div className="btn">
                            <a href="/">자세히 보기</a>
                            <a href="/" className="black"> 제품 보기 </a>
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div className="desc">
                        <span>NEW Product</span>
                        <h3>SPRING SEASON</h3>
                        <p>
                            따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금
                            <br />
                            향기를 타고 봄이 다가온다
                        </p>
                        <div className="btn">
                            <a href="/">자세히 보기</a>
                            <a href="/" className="black"> 제품 보기 </a>
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div className="desc">
                        <span>NEW Product</span>
                        <h3>SPRING SEASON</h3>
                        <p>
                            따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금
                            <br />
                            향기를 타고 봄이 다가온다
                        </p>
                        <div className="btn">
                            <a href="/">자세히 보기</a>
                            <a href="/" className="black"> 제품 보기 </a>
                        </div>
                    </div>
                </swiper-slide> -->
            </swiper>
        </div>
    </section>
    <!--//sliderType-->
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css/pagination";
import "swiper/css/navigation";
import { Autoplay, Pagination, Navigation } from "swiper";
import "swiper/css";

export default {
    props: {
        attr: String,
    },
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Autoplay, Pagination, Navigation],
        };
    },
    data: function () {
        return {
            Slide: [
                {
                    span: "NEW Product",
                    h3: "SPRING SEASON",
                    p: "따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금\n향기를 타고 봄이 다가온다",
                    aClass: "black",
                },
                {
                    span: "NEW Product",
                    h3: "SPRING SEASON",
                    p: "따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금\n향기를 타고 봄이 다가온다",
                    aClass: "black",
                },
                {
                    span: "NEW Product",
                    h3: "SPRING SEASON",
                    p: "따스한 햇살을 타고 부드러운 꽃 향이 다가오는 지금\n향기를 타고 봄이 다가온다",
                    aClass: "black",
                },
            ],
        };
    },
};
</script>
<style>
.slider__inner {
    margin-top: 70px;
}
.slider {
    cursor: pointer;
    position: relative;
}
.slider__img {
    background: url(../../assets/img/sliderType01.jpg) no-repeat center / cover;
}
.slider__img .desc {
    width: 100%;
    margin: 0 auto;
    padding: 100px 120px;
    box-sizing: border-box;
}
.slider__img .desc span {
    font-size: 16px;
    background-color: #fff;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
}
.slider__img .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.slider__img .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}
.slider__img .desc .btn a {
    font-size: 16px;
    background-color: #fff;
    padding: 11px 50px;
    transition: all 0.5s;
    display: inline-block;
}
.slider__img .desc .btn a.black {
    transition: all 0.5s;
    background: #000;
    color: #fff;
}
.slider__img .desc .btn a:hover {
    background-color: rgb(0, 0, 0);
    color: white;
    transform: scale(0.95);
    border-radius: 10px;
}
.slider__img .desc .btn a.black:hover {
    transform: scale(0.95);
    border-radius: 10px;
}
.slider__arrow a {
    position: absolute;
    top: 50%;
    width: 30px;
    height: 56px;
    transform: translateY(-50%);
    background-image: url(../../assets/img/slider_icon.svg);
}
.slider__arrow a.left {
    left: 20px;
}
.slider__arrow a.right {
    right: 20px;
    background-position: -50px 0;
}
.slider__dot {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 25px;
}
.slider__dot a {
    display: inline-block;
    width: 16px;
    height: 16px;
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -20px -70px;
}
.slider__dot a.active {
    background-position: 0px -70px;
}
.slider__dot a.play {
    background-position: -40px -70px;
}
.slider__dot a.stop {
    background-position: -60px -70px;
}

/* @media (max-width: 1080px) {
  .slider__inner {
    margin-top: 0;
  }
  .slider__img .desc h3{
    font-size: 90px;
  }
  .slider__inner {
    margin-top: 0;
  }
  .slider__img .desc h3{
    font-size: 90px;
  }
  .slider__arrow a {
    position: absolute;
    top: 94%;
    width: 12px;
    height: 20px;
    background-image: url(../img/slider_icon.svg);
  }
  .slider__arrow a.left {
    left: 20px;
    background-position: -100px 0;
  }
  .slider__arrow a.right {
    right: 20px;
    background-position: -117px 0;
  }


}
@media (max-width: 768px) {
  .slider__inner {
    margin-top: 0;
  }
  .slider__img .desc {
    padding: 100px 90px;
  }
  .slider__img .desc h3{
    font-size: 52px;
  }
  .slider__img .desc p {
    font-size: 15px;
  }
  .slider__img .desc .btn a {
    font-size: 13px;
    padding: 11px 30px;
  }
}

@media (max-width: 480px) {
  .slider__img {
    background: url(../img/sliderType01.jpg) no-repeat center / cover;
  }
  .slider__img .desc {
    padding: 30px 15px;
  }
  .slider__img .desc span {
    font-size: 14px;
  }
  .slider__img .desc p {
    margin-bottom: 20px;
  }
  .slider__img .desc .btn a {
    font-size: 13px;
    padding: 8px 10px;
  }
  .slider__dot {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 10px;
  }
} */

.swiper-button {
    position: absolute;
    left: 50%;
    bottom: 27px;
    margin-left: 40px;
    z-index: 100000;
    display: flex;
}
.swiper-button-play {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -40px -69px;
    width: 16px;
    cursor: pointer;
    height: 16px;
    display: none;
}
.swiper-button-stop {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -60px -70px;
    width: 16px;
    height: 16px;
    cursor: pointer;
}

.swiper-button-next,
.swiper-button-prev {
    width: 30px;
    height: 56px !important;
    background-image: url(../../assets/img/slider_icon.svg);
}
.swiper-button-next:after,
.swiper-button-prev:after {
    transform: scale(0);
}

.swiper-button-next {
    background-position: -52px 0;
}

.swiper-pagination-bullet {
    width: 16px !important;
    height: 16px !important;
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -20px -70px;
    border: 1px solid white;
}
/* swiper */
.swiper-slide {
    background: url(../../assets/img/sliderType01.jpg) no-repeat center / cover;
}

.slide02 {
    background: url(../../assets/img/sliderType01.jpg) no-repeat center / cover;
}
.slide03 {
    background: url(../../assets/img/sliderType01.jpg) no-repeat center / cover;
}
.swiper-slide .desc {
    width: 100%;
    margin: 0 auto;
    padding: 100px 120px;
    box-sizing: border-box;
}
.swiper-slide .desc span {
    font-size: 16px;
    background-color: #fff;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
}
.swiper-slide .desc h3 {
    font-size: 100px;
    font-weight: 300;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.swiper-slide .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}
.swiper-slide .desc .btn a {
    font-size: 16px;
    background-color: #fff;
    padding: 11px 50px;
    transition: all 0.5s;
    display: inline-block;
}
.swiper-slide .desc .btn a.black {
    transition: all 0.5s;
    background: #000;
    color: #fff;
}
.swiper-slide .desc .btn a:hover {
    background-color: rgb(0, 0, 0);
    color: white;
    transform: scale(0.95);
    border-radius: 10px;
}
.swiper-slide .desc .btn a.black:hover {
    transform: scale(0.95);
    border-radius: 10px;
}
@media (max-width: 1080px) {
    .slider__inner {
        margin-top: 0;
    }
    .swiper-slide {
        text-align: center;
    }
    .swiper-slide .desc h3 {
        font-size: 63px;
    }
}
@media (max-width: 768px) {
    .swiper-slide .desc {
        padding: 80px 40px;
    }
    .swiper-slide .desc span {
        font-size: 13px;
    }
    .swiper-slide .desc h3 {
        font-size: 40px;
    }
    .swiper-slide .desc p {
        font-size: 16px;
        margin-bottom: 50px;
    }
    .swiper-slide .desc .btn a {
        font-size: 14px;
        padding: 8px 10px;
    }
    .swiper-button {
        left: 50%;
        bottom: 28.5px;
        margin-left: 40px;
    }
    .swiper-button-stop,
    .swiper-button-play {
        transform: scale(1.4);
    }
}
</style>
