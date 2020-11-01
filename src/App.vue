<template>
  <div id="app">
    <Header></Header>
    <main>
      <div class="eyecatch">
        <p class="eyecatch-txt">機械ではできない仕事を</p>
        <div class="news-wrapper">
          <div class="news">
            <div class="date">2019/01/01</div>
            <div class="article">
              ニュースタイトルがここに入ります。3月の決算報告書
            </div>
          </div>
          <div class="news-logo">
            <div id="news-logo">news</div>
          </div>
        </div>
      </div>

      <div id="contents" class="wrap">
        <div class="mission">
          <img src="./assets/mission-img.jpg" />
        </div>
        <div class="contents">
          <h3>お客様のために進化する成長企業であり続ける</h3>
          <p>
            顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける企業支援会社を目指します。企業が現在直面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種マーケティングをご提供いたします。
          </p>
          <div class="button-submit">
            <button class="button" type="submit">ミッション詳細</button>
          </div>
        </div>
      </div>

      <div class="service">
        <div class="section-title">service</div>
        <div class="service2" v-for="(data, index) in service" :key="index">
          <img :src="data.img" alt />
          <div class="one">
            <h3>{{ data.title }}</h3>
            <p>{{ data.subtitle }}</p>
            <p>{{ data.description }}</p>
            <div class="button-submit">
              <button class="button-detail" type="submit">サービス詳細</button>
            </div>
          </div>
        </div>
        <div class="service1" v-for="(data, index) in service" :key="index">
          <img :src="data.img" alt />
        </div>
        <div class="two">
          <h3>{{ data.title }}</h3>
          <p>{{ data.subtitle }}</p>
          <p>{{ data.subtitle }}</p>
          <div class="button-submit">
            <button class="button-detail" type="submit">サービス詳細</button>
          </div>
        </div>
      </div>

      <div class="details">
        <div id="details">
          <div class="company">
            <div class="company-text">
              <h2>company</h2>
              <p>会社概要</p>
            </div>
          </div>
          <div class="recruit">
            <div class="recruit-text">
              <h2>recruit</h2>
              <p>採用情報</p>
            </div>
          </div>
        </div>
        <div class="FAQ">
          <div class="logo">FAQ</div>
          <div class="question">良くある質問</div>
        </div>
      </div>

      <div class="contact">
        <div class="contact-text">
          <h1>contact</h1>
          <h2>お問い合わせ</h2>
          <h3>お気軽にお問い合わせください。</h3>
          <p>
            資料請求・お問い合わせなどなんでも気軽にお問い合わせください。お仕事のご連絡もお問い合わせページに飛んでいただいて、入力フォームにご記入お願いいたします。
          </p>
          <button class="contact-button" type="submit">お問い合わせへ</button>
        </div>
      </div>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  data() {
    return {
      service: [
        {
          img: require("./assets/service2.jpg"),
          title: "web製作事業",
          subtitle: "コーチングのミッション",
          descrption:
            "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の製作実績があります。",
        },
        {
          img: require("./assets/service1.jpg"),
          title: "web製作事業",
          subtitle: "コーチングのミッション",
          descrption:
            "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の製作実績があります。",
        },
      ],
    };
  },
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
/* リセットcss */
html,
body,
div,
span,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
abbr,
address,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
samp,
small,
strong,
sub,
sup,
var,
b,
i,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

body {
  line-height: 1;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}

nav ul {
  list-style: none;
}

blockquote,
q {
  quotes: none;
}

blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}

a {
  margin: 0;
  padding: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

/* change colours to suit your needs */
ins {
  background-color: #ff9;
  color: #000;
  text-decoration: none;
}

/* change colours to suit your needs */
mark {
  background-color: #ff9;
  color: #000;
  font-style: italic;
  font-weight: bold;
}

del {
  text-decoration: line-through;
}

abbr[title],
dfn[title] {
  border-bottom: 1px dotted;
  cursor: help;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

/* change border colour to suit your needs */
hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid #cccccc;
  margin: 1em 0;
  padding: 0;
}

input,
select {
  vertical-align: middle;
}

/* 共通のスタイル */
.section-title {
  font-size: 30px;
  font-weight: bold;
  padding: 30px;
  text-align: center;
}

img {
  display: block;
  width: 100%;
}

.wrap {
  width: 80%;
  margin: 0 auto 150px;
}

.flex {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.between {
  justify-content: space-between;
}

.around {
  justify-content: space-around;
}

.eyecatch {
  height: 600px;
  background: url(./assets/eyecatch.jpg) no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}

.eyecatch p {
  position: absolute;
  top: 50%;
  left: 10%;
  font-size: 50px;
  font-style: italic;
  font-weight: bold;
  color: #fff;
  line-height: 1;
}

.news-wrapper {
  width: 50%;
  position: absolute;
  right: 0;
  bottom: 0;
}

.news {
  background: #fff;
  height: 50px;
  width: 80%;
}

.date {
  padding: 5px;
  font-size: 14px;
  color: #000;
}

.article {
  padding: 5px;
  margin-left: 10px;
  font-size: 16px;
  color: #000;
  line-height: 1.5;
}

.news-logo {
  background-color: gray;
  position: absolute;
  right: 0;
  bottom: 0;
  height: 50px;
  width: 20%;
}

#news-logo {
  font-size: 20px;
  font-weight: bold;
  color: #fff;
  text-align: center;
  line-height: 50px;
}

.mission img {
  width: 45%;
  position: absolute;
  top: 25%;
  right: 30px;
}

#contents {
  width: 100%;
  height: 600px;
  background: #000;
  position: relative;
}

.contents {
  width: 60%;
  color: white;
  position: absolute;
  top: 30%;
  left: 20%;
}

.contents h3 {
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 15px;
  line-height: 1.5;
}

.contents p {
  font-size: 21px;
  margin-bottom: 15px;
  line-height: 1.5;
}

.button {
  padding: 10px 20px;
  background-color: #fff;
  color: #000;
  margin: 10px 0;
}

.button:hover {
  background: #cccccc;
}

.service {
  background: #cccccc;
  width: 100%;
  height: 1400px;
  position: relative;
}

.service2 img {
  width: 50%;
  position: absolute;
  top: 10%;
  right: 0;
}

.service1 img {
  width: 50%;
  position: absolute;
  top: 60%;
  left: 0;
}

.one {
  width: 35%;
  height: 200px;
  background: #fff;
  padding: 75px;
  position: absolute;
  top: 15%;
  left: 15%;
}

.one h3,
.one p {
  padding: 10px;
  line-height: 1.5;
}

.two {
  width: 35%;
  height: 200px;
  background: #fff;
  padding: 75px;
  position: absolute;
  top: 65%;
  right: 15%;
}

.two h3,
.two p {
  padding: 10px;
  line-height: 1.5;
}

.button-detail {
  display: block;
  margin: 0 0 0 auto;
  padding: 10px 20px;
  background-color: #fff;
  color: #000;
}

.button-detail:hover {
  background: #cccccc;
}

.details {
  width: 100%;
  height: 1100px;
  background: #fff;
}

#details {
  position: relative;
  top: 200px;
}

.company-text h2,
.recruit-text h2 {
  font-size: 60px;
  font-weight: bold;
  padding-top: 170px;
  padding-bottom: 10px;
  text-align: center;
}

.company-text p,
.recruit-text p {
  font-size: 30px;
  font-weight: bold;
  padding: 10px;
  text-align: center;
}

.company {
  background: url(./assets/company.jpeg) no-repeat;
  background-size: cover;
  width: 45%;
  height: 500px;
  position: absolute;
  left: 0;
  color: #fff;
}

.recruit {
  background: url(./assets/recruit.jpg) no-repeat;
  background-size: cover;
  width: 45%;
  height: 500px;
  position: absolute;
  right: 0;
  color: #fff;
}

.FAQ {
  display: flex;
  width: 80%;
  height: 100px;
  background: #000;
  position: relative;
  top: 80%;
  left: 10%;
}

.logo {
  padding: 35px 50px;
  color: #fff;
  font-size: 30px;
  font-weight: bold;
}

.question {
  color: #fff;
  font-size: 20px;
  font-weight: bolder;
  margin: 40px;
  position: absolute;
  left: 42%;
}

.contact {
  background: url(./assets/contact-bg.jpg) no-repeat;
  width: 100%;
  height: 800px;
  color: #fff;
}

.contact-text h1,
.contact-text h2,
.contact-text h3,
.contact-text p {
  text-align: center;
  line-height: 1.5;
}

.contact-text h1 {
  padding-top: 200px;
  font-size: 40px;
  font-weight: bold;
}

.contact-text h2 {
  padding-top: 10px;
  font-size: 20px;
  font-weight: bold;
}

.contact-text h3 {
  padding-top: 50px;
  font-size: 45px;
  font-weight: lighter;
}

.contact-text p {
  padding-top: 50px;
  padding-bottom: 50px;
  font-size: 21px;
  font-weight: lighter;
}

.contact-button {
  display: block;
  margin: 0 auto 0 auto;
  padding: 10px 20px;
  border: 1px solid #fff;
  color: #fff;
  background-color: transparent;
}

@media screen and (max-width: 480px) {
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 15px;
    right: 20px;
    transition: 0.4s;
  }

  #hamburger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: #fff;
    transition: 0.8s;
  }

  #hamburger span:nth-of-type(1) {
    top: 10px;
  }

  #hamburger span:nth-of-type(2) {
    top: 20px;
  }

  #hamburger span:nth-of-type(3) {
    top: 30px;
  }

  .eyecatch p {
    width: 90%;
    position: absolute;
    top: 30%;
    left: 5%;
  }

  .news-wrapper {
    width: 100%;
  }

  .news {
    width: 80%;
    height: 80px;
  }

  .news-logo {
    width: 20%;
    height: 80px;
  }

  #news-logo {
    line-height: 80px;
  }

  .wrap {
    margin: 0 auto 50px;
  }

  .mission img {
    width: 40%;
    position: absolute;
    top: 90%;
    z-index: 1;
  }

  .contents {
    width: 76%;
    position: absolute;
    top: 8%;
    left: 12%;
    z-index: 2;
  }

  .contents h3 {
    font-size: 40px;
  }

  .button {
    font-size: 20px;
    padding: 10px 30px;
  }

  .section-title {
    font-size: 55px;
  }

  .service {
    height: 1300px;
  }

  .service1 img {
    width: 90%;
    position: absolute;
    top: 55%;
    left: 5%;
  }

  .service2 img {
    width: 90%;
    position: absolute;
    left: 5%;
  }

  .one {
    width: 86%;
    height: 260px;
    padding: 10px;
    position: absolute;
    top: 30%;
    left: 5%;
  }

  .one h3,
  .one p {
    padding: 10px;
    line-height: 1.5;
  }

  .two {
    width: 86%;
    height: 260px;
    padding: 10px;
    position: absolute;
    top: 73.5%;
    right: 5%;
  }

  .two h3,
  .two p {
    padding: 10px;
    line-height: 1.5;
  }

  .button-detail {
    font-size: 20px;
    padding: 10px 40px;
    margin: 0 0 10px auto;
  }

  #details {
    position: relative;
    top: 5%;
  }

  .company {
    width: 100%;
    height: 400px;
  }

  .recruit {
    position: absolute;
    top: 400px;
    width: 100%;
    height: 400px;
  }

  .FAQ {
    height: 150px;
  }

  .logo {
    padding: 60px;
  }

  .question {
    padding-top: 25px;
  }

  .contact-text {
    width: 80%;
    position: absolute;
    left: 10%;
  }

  .contact-text h1 {
    padding-top: 80px;
  }

  .contact-button {
    padding: 15px 60px;
    font-size: 16px;
  }
}
</style>
