<template>
    <footer id="footerType" class="footer__wrap" :class="attr">
        <h2 class="blind">푸터 영역</h2>
        <div class="footer__inner" :class="layout">
            <div class="footer__menu">
                <div>
                    <h3>시즌</h3>
                    <ul>
                        <li>
                            <a href="/">봄</a>
                        </li>
                        <li>
                            <a href="/">여름</a>
                        </li>
                        <li>
                            <a href="/">가을</a>
                        </li>
                        <li>
                            <a href="/">겨울</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>회사 소개</h3>
                    <ul>
                        <li>
                            <a href="/">이용 약관</a>
                        </li>
                        <li>
                            <a href="/">광고 제휴</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>출처</h3>
                    <ul>
                        <li>
                            <a href="/">비레디</a>
                        </li>
                        <li>
                            <a href="/">UNSPLASH</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>메뉴</h3>
                    <ul>
                        <li>
                            <a href="/">메뉴</a>
                        </li>
                        <li>
                            <a href="/">신제품</a>
                        </li>
                        <li>
                            <a href="/">퍼스널 향수</a>
                        </li>
                        <li>
                            <a href="/">베스트셀러</a>
                        </li>
                        <li>
                            <a href="/">ABOUT US</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>회원</h3>
                    <ul>
                        <li>
                            <a href="/">회원 혜택</a>
                        </li>
                        <li>
                            <a href="/">회원 후기</a>
                        </li>
                        <li>
                            <a href="/">공지사항</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>고객지원</h3>
                    <ul>
                        <li>
                            <a href="/">A/S</a>
                        </li>
                        <li>
                            <a href="/">FAQ</a>
                        </li>
                        <li>
                            <a href="/">1:1 문의</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="footer__right">
            2022 SSHINY. Portfolio is Power
            <br />
            All rights reserved.
        </div>
    </footer>
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
.footer__menu {
    display: flex;
    margin-bottom: 70px;
    justify-content: space-between;
}
.footer__menu > div {
    width: 16%;
}
.footer__menu h3 {
    font-size: 18px;
    margin-bottom: 20px;
}

.footer__menu li a {
    font-size: 14px;
    color: #666;
    margin: 10px 0;
    display: block;
}
.footer__right {
    border-top: 1px solid #d9d9d9;
    text-align: center;
    padding-top: 40px;
    color: #666;
    line-height: 1.5;
}

@media (max-width: 960px) {
    .footer__menu {
        display: none;
    }
    .footer__right {
        padding-top: 0;
        border-top: 0;
    }
    .footer__wrap {
        padding: 40px 0;
    }
}

/* @media (max-width: 480px){
    .footer__menu {
      display: flex;
      flex-wrap: wrap;
      margin-bottom: 70px;
      justify-content: space-between;
    }
    .footer__menu > div {
      width: 33%;
    }
    .footer__menu div:first-child {
      margin-bottom: 20px;
    }
  } */
</style>
