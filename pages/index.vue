<template>
  <div class="sait">
    <div class="header">
      <div class="wrap">
        <div class="header_top">
          <div class="logo"></div>
          <div class="header_top_right"></div>
          <div class="clear"></div>
        </div>

        <div class="navigation">
          <ul class="nav">
            <li>
              <nuxt-link to="/">Главная</nuxt-link>
            </li>
            <li class="test , q-pa-md q-gutter-sm">
              <a href="#" onclick="alert('Функция пока не работает')"
                >Компьютеры</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Домашние приборы</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Кухонная техника</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Смартфоны</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Планшеты</a
              >
            </li>
            <li>
              <a href="#">Отзывы</a>
            </li>
            <li>
              <nuxt-link to="basket">Корзина</nuxt-link>
            </li>
            <li></li>
          </ul>
          <span class="left-ribbon"></span>
          <span class="right-ribbon"></span>
        </div>

        <div class="header_bottom">
          <div class="slider-text">
            <h2>
              ТехноДом
              <br />
              Или Сулпак
            </h2>
            <p>Магазин Техники и электроприборов впервые в Алматы .</p>
            <a href="https://github.com/A4U4UK/">Наш оффициальный сайт</a>
          </div>
          <div class="slider-img">
            <img src="/images/slider-img.png" alt="комп" />
          </div>
          <div class="clear"></div>
        </div>
      </div>
    </div>

    <div class="main">
      <div class="content">
        <div class="content_bottom">
          <div class="wrap">
            <div class="content-bottom-left">
              <div class="buters-guide">
                <h3>Buyers Guide</h3>
                <p>
                  <span
                    >Я устал придумывать текст на сайте но лорем не хочу
                  </span>
                </p>
                <p>
                  Большой ассортимент товаров доступен для ознакомления на
                  данном сайте, где вы можете получить информацию о продукте
                  перед покупкой. Однако извините, но на этом сайте невозможно
                  совершить покупку из-за технических проблем или других причин.
                </p>
              </div>
            </div>

            <div class="content-bottom-right">
              <h3>Browse All Categories</h3>
              <div class="section group">
                <div
                  v-for="item in data"
                  :key="item.id"
                  class="grid_1_of_4 images_1_of_4">
                  <h4 class="name_item">
                    <a>{{ item.name }}</a>
                  </h4>
                  <div class="img_cart">
                    <img
                      style="max-width: 120px; min-height: 80px"
                      :src="item.img"
                      alt="" />
                  </div>
                  <div class="price-details">
                    <div class="price-number">
                      <p>
                        <span class="rupees">₸{{ item.price }}</span>
                      </p>
                    </div>
                    <nuxt-link class="button-56" :to="`preview/${item.id}`"
                      >Подробнее</nuxt-link
                    >
                    <div class="clear"></div>
                  </div>
                </div>
              </div>
            </div>
            <div style="padding-top: 30px" class="product-articles">
              <ul>
                <li>
                  <div class="article">
                    <p>
                      Далеко-далеко за словесными горами в стране гласных, и
                      согласных живут рыбные тексты. Текст, рукописи текстов о
                      единственное продолжил речью скатился если сбить буквенных
                      пустился живет решила большого, агентство снова курсивных,
                      океана она выйти возвращайся безопасную он гор домах всеми
                      мир? По всей океана о рекламных запятой курсивных журчит
                      заглавных моей назад речью рыбного? Инициал, запятых даже.
                      Переулка вопрос дорогу грустный напоивший на берегу, путь
                      до приставка? Строчка, lorem всемогущая продолжил
                      безорфографичный вершину даже! Языкового букв коварных
                      подзаголовок власти это ipsum диких, пунктуация, ты
                      грамматики за пустился точках, первую они правилами она
                      даль своего проектах переписали предупредила грустный. Мир
                      пор если имени свое даже переулка!
                    </p>
                  </div>
                </li>
              </ul>
            </div>
          </div>
          <div class="clear"></div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="wrap">
        <div class="copy_right">
          <p>Здесь могла быть ваша реклама</p>
        </div>
        <div class="footer-nav">
          <ul>
            <li><a href="https://supabase.com/">Наши партнер</a> :</li>
            <li><a href="https://www.sulpak.kz/">Инфомация</a> :</li>
            <li><a href="https://t.me/Ot4imVlada">Контакты с автором</a> :</li>
            <li>
              <a href="https://www.youtube.com/watch?v=k9RU4uW0kSY">Sigma</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { createClient } from "@supabase/supabase-js";
const client = createClient(
  "https://nrdgebxynjkyfcrwohjo.supabase.co",
  "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im5yZGdlYnh5bmpreWZjcndvaGpvIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDE2ODc4NTYsImV4cCI6MjAxNzI2Mzg1Nn0.ML9-cPzQOD3BPeUMFq-4fqJZwL7D-KGz0EAhgzgDURk"
);
const { data } = await useAsyncData("goods", async () => {
  const { data } = await client.from("goods").select("*");
  return data;
});
console.log(data.value);
</script>
<style>
.button-56 {
  align-items: center;
  background-color: #fee6e3;
  border: 2px solid #111;
  border-radius: 8px;
  box-sizing: border-box;
  color: #111;
  cursor: pointer;
  display: flex;
  font-family: Inter, sans-serif;
  font-size: 16px;
  height: 48px;
  justify-content: center;
  line-height: 24px;
  max-width: 100%;
  padding: 0 25px;
  position: relative;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-56:after {
  background-color: #111;
  border-radius: 8px;
  content: "";
  display: block;
  height: 48px;
  left: 0;
  width: 100%;
  position: absolute;
  top: -2px;
  transform: translate(8px, 8px);
  transition: transform 0.2s ease-out;
  z-index: -1;
}

.button-56:hover:after {
  transform: translate(0, 0);
}

.button-56:active {
  transition: 0.5s;
  background-color: #040000;
  outline: 0;
}

.button-56:hover {
  transition: 0.5s;
  background-color: #eb8178;
  outline: 0;
}

@media (min-width: 768px) {
  .button-56 {
    padding: 0 40px;
  }
}

.img_cart {
  padding-top: 10px;
  padding-left: 10px;
  width: 150px;
  height: 180px;
}
.but_more {
  text-decoration: none;
  size: 40%;
  border-color: #666;
}
.name_item {
  margin-top: 20px;
}

.clear {
  clear: both;
}

img {
  max-width: 100%;
}
/*end reset*/
@font-face {
  font-family: "Ubuntu Condensed", sans-serif;
  src: url(../font/Amble-Regular-webfont.ttf) format("truetype");
}
body {
  font-family: "Ubuntu Condensed", sans-serif;
  background: #ebebeb;
}
.wrap {
  width: 80%;
  margin: 0 auto;
  transition: all 0.2s linear;
  -moz-transition: all 0.2s linear; /* firefox */
  -webkit-transition: all 0.2s linear; /* safari and chrome */
  -o-transition: all 0.2s linear; /* opera */
  -ms-transition: all 0.2s linear;
}
.header {
  background: #23272a;
  padding-bottom: 40px;
}
.header_top {
  padding-bottom: 25px;
}
.logo {
  float: left;
}
.header_top_right {
  float: right;
  padding-top: 10px;
}

.navigation {
  align-items: center;
  background: #e44f2b;
  padding: 5px 0;
  position: relative;
}
.navigation span.left-ribbon {
  position: absolute;
  left: -40px;
  top: 8px;
  width: 40px;
  height: 60px;
  background: url(../images/left-fold.png) no-repeat;
}
.navigation span.right-ribbon {
  position: absolute;
  right: -40px;
  top: 8px;
  width: 40px;
  height: 60px;
  background: url(../images/right-fold.png) no-repeat;
}
.toggleMenu {
  padding-left: 20px;
  display: block;
  padding: 16px 15px;
  color: #fff;
  width: 95%;
  border-top: 1px solid #db3c15;
  border-bottom: 1px solid #db3c15;
  background: url("../images/nav-icon.png") no-repeat 98% center;
}
.nav {
  list-style: none;
  zoom: 1;
  background: #e44f2b;
  border-bottom: 1px solid #db3c15;
}
.nav:before,
.nav:after {
  content: " ";
  display: table;
}
.nav:after {
  clear: both;
}
.nav ul {
  list-style: none;
  width: 11em;
}
.nav a {
  padding: 16px 33px;
  color: #ffb29f;
  border-top: 1px solid #db3c15;
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
.nav a:hover {
  color: #fff;
}
.nav li {
  position: relative;
}
.nav > li {
  float: left;
}
.nav > li:first-child,
.nav > li:last-child {
  background-image: none;
}
.nav > li {
  background-image: url("../images/line-divider.png");
  background-repeat: no-repeat;
  background-position: left;
}
.nav > li > a {
  display: block;
}
.nav li ul {
  position: absolute;
  left: -9999px;
}
.nav > li.hover > ul {
  left: 0;
}
.nav li li.hover ul {
  left: 100%;
  top: 0;
}
.nav li li a {
  display: block;
  background: #ea5e3c;
  position: relative;
  z-index: 100;
  border-top: 1px solid #ef7a5d;
  padding: 10px;
  font-size: 15px;
}
.nav li li a:hover {
  background: #db502e;
}
.nav li li li a {
  background: #ed6a4a;
  z-index: 200;
  border-top: 1px solid #ef7a5d;
}

@media screen and (max-width: 768px) {
  .nav > li {
    float: none;
  }
  .nav > li > .parent {
    background-position: 95% 50%;
  }
  .nav li li .parent {
    background-image: url("images/downArrow.png");
    background-repeat: no-repeat;
    background-position: 95% 50%;
  }
  .nav ul {
    display: block;
    width: 100%;
  }
  .nav > li.hover > ul,
  .nav li li.hover ul {
    position: static;
  }
  .nav > li {
    background-image: url("../images/nav-arrow.png");
    background-position: 96% 55%;
  }
  .nav > li > .parent {
    background-position: 96% 55%;
  }
}
.header_bottom {
  padding: 6% 0 2%;
}
.slider-text {
  float: left;
  width: 50%;
}
.slider-text h2 {
  color: #e44f2b;
  font-size: 40px;
}
.slider-text p {
  color: #8fa7ae;
  font-size: 20px;
  margin: 20px 0;
}
.slider-text a {
  background: #8fa7ae;
  display: inline-block;
  padding: 8px 25px;
  font-size: 20px;
  color: #23272a;
  position: relative;
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
.slider-text a:hover {
  color: #fff;
  background: #6c9ba9;
}
.slider-text a:after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  border-width: 22px 0px 18px 8px;
  border-style: solid;
  border-color: rgba(255, 0, 0, 0) rgba(0, 0, 255, 0) rgba(0, 128, 0, 0) #23272a;
}
.slider-text a:before {
  content: "";
  position: absolute;
  right: 0;
  top: 0;
  border-width: 21px 8px 18px 0px;
  border-style: solid;
  border-color: rgba(239, 0, 0, 0) #23272a rgba(0, 128, 0, 0)
    rgba(35, 39, 42, 0);
}
.slider-img {
  float: right;
  width: 42%;
}
.slider-img img {
  margin-top: 60px;
}

.content_bottom {
  padding-top: 2em;
}
.content-bottom-left {
  float: left;
  width: 20%;
  padding-right: 2%;
}
.content-bottom-right {
  float: left;
  width: 75.8%;
  padding-left: 2%;
  border-left: 1px solid #d7d7d7;
}

.buters-guide h3,
.content-bottom-right h3,
.preview-page h3 {
  font-size: 1.1em;
  color: #fff;
  padding: 10px;
  padding-left: 25px;
  background: #e44f2b;
  position: relative;
  margin-bottom: 5px;
}
.buters-guide h3:after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  border-width: 22px 0px 20px 15px;
  border-style: solid;
  border-color: rgba(255, 0, 0, 0) rgba(0, 0, 255, 0) rgba(0, 128, 0, 0) #ebebeb;
}
.content-bottom-right h3,
.preview-page h3 {
  background: #23272a !important;
  margin-bottom: 10px !important;
  padding-left: 10px !important;
}
.content-bottom-right h3:before,
.preview-page h3:before {
  content: "";
  position: absolute;
  right: 0;
  top: 0;
  border-width: 22px 15px 20px 0px;
  border-style: solid;
  border-color: rgba(255, 0, 0, 0) #ebebeb rgba(0, 0, 255, 0) rgba(0, 128, 0, 0);
}
.buters-guide {
  margin-top: 2em;
}
.buters-guide p {
  font-size: 14px;
  color: #969696;
  line-height: 1.4em;
  padding: 8px 0;
}
.buters-guide p span {
  color: #e44f2b;
  font-size: 16px;
}

.section {
  clear: both;
  padding: 0px;
  margin: 0px;
}
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  zoom: 1;
}
.grid_1_of_4 {
  display: block;
  float: left;
}
.grid_1_of_4:first-child {
  margin-left: 0;
}
.images_1_of_4 {
  width: 20%;
  padding: 1.5%;
  text-align: center;
  position: relative;
  background: #fff;
}
.price-details {
  border-top: 1px solid #eee;
}
.price-details p span.rupees {
  font-size: 22px;
  color: #23272a;
}
.add-cart {
  display: inline-block;
}
.add-cart h4 a,
.add-cart h4 a:after {
  bottom: 0;
  left: 0;
  border-width: 14px 0px 12px 5px;
  border-style: solid;
  border-color: rgba(255, 0, 0, 0) rgba(0, 0, 255, 0) rgba(0, 128, 0, 0) #fff;
}
.add-cart h4 a:before {
  content: "";
  top: 0;
  right: 0;
  border-width: 14px 5px 12px 0px;
  border-style: solid;
  border-color: rgba(239, 0, 0, 0) #fff rgba(0, 128, 0, 0) rgba(35, 39, 42, 0);
}
.add-cart h4 a:hover {
  text-shadow: 0px 0px 1px #000;
  background: #292929;
}
.product-articles {
  padding: 20px 0;
  padding-top: 30px;
}
.product-articles p {
  font-size: 15px;
  color: #a1a1a1;
  line-height: 1.6em;
  padding: 5px 0;
}
.product-articles p span {
  color: #23272a;
  font-size: 18px;
}
.product-articles p a {
  color: #e44f2b;
  font-size: 14px;
}
.product-articles p a:hover {
  text-decoration: underline;
  color: #23272a;
}
.product-articles li {
  padding: 2% 0 2%;
  border-top: 1px solid #dfdfdf;
}
.product-articles li:first-child {
  border-top: none !important;
  padding-top: 0;
}
.footer {
  background: #e44f2b;
  padding: 3% 0;
}
.footer-nav {
  float: right;
}
.footer-nav li {
  display: inline-block;
  color: #fff;
  font-size: 14px;
}
.footer-nav li a {
  color: #fff;
  margin: 0 10px;
}
.footer-nav li a:hover {
  text-decoration: underline;
}
.copy_right {
  float: left;
}
.copy_right p {
  font-size: 14px;
  color: #fff;
}
.copy_right p a {
  color: #fff;
  text-decoration: underline;
}
.copy_right p a:hover {
  color: #222;
  text-decoration: none;
}

#toTop {
  display: none;
  text-decoration: none;
  position: fixed;
  bottom: 10px;
  right: 10px;
  overflow: hidden;
  width: 55px;
  height: 50px;
  border: none;
  text-indent: 100%;
  background: url(../images/arrow_up.png) no-repeat right top;
}

.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  zoom: 1;
}
.cont-desc {
  display: block;
  float: left;
  clear: both;
}
.cont-desc:first-child {
  margin-left: 0;
}
.desc {
  display: block;
  float: left;
  margin: 0% 0 0% 2.6%;
}
.span_1_of_2 {
  width: 76.6%;
  padding: 1.5% 0;
}
.span_3_of_2 {
  width: 61.2%;
}
.span_3_of_2 h2 {
  font-size: 1.2em;
  color: #e44f2b;
  font-weight: normal;
  margin-top: 0px;
}
.span_3_of_2 p {
  font-size: 13px;
  padding: 5px 0;
  color: #8b8b8b;
  line-height: 1.6em;
  font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;
}
.price p {
  font-size: 0.85em;
  padding-top: 20px;
  color: #666;
  vertical-align: top;
}
.price p span {
  font-size: 2em;
  color: #e44f2b;
  font-family: "Ubuntu Condensed", sans-serif;
}
.available {
  padding: 10px 0;
  border-top: 1px solid #ebebeb;
}
.available li span {
  font-size: 13px;
  color: #8b8b8b;
  font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;
}
.available li {
  display: block;
  color: #000;
  font-size: 20px;
  padding: 5px 0;
}
.share-desc {
  margin-bottom: 15px;
}
.share {
  float: left;
}
.share p {
  padding-top: 10px;
  font-size: 13px;
  color: #333;
  display: inline;
}

.product_desc h2 {
  font-size: 1.2em;
  color: #333;
}
.product_desc p {
  font-size: 0.8em;
  padding: 5px 0;
  color: #8b8b8b;
  line-height: 1.8em;
  font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;
}
.span_3_of_2 .button {
  float: right;
}
.span_3_of_2 .button a {
  font-size: 0.85em;
  display: block;
  padding: 8px 10px;
  background: #e44f2b;
  color: #fff;
  text-decoration: none;
  outline: 0;
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  -o-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
}
.span_3_of_2 .button a:hover {
  text-shadow: 0px 0px 1px #000;
  background: #292929;
}

.popular-products li .price-number {
  margin: 5px 0;
}
.popular-products li .price-number p span.line-through {
  text-decoration: line-through;
  color: #e44f2b;
}
.preview-page {
  padding: 2% 0;
}

.product-tags h4 {
  padding: 10px 0;
  font-size: 0.95em;
  color: #333;
}

.product-tags .button {
  margin-top: 15px;
  line-height: 3em;
}
.span_3_of_2 .button {
  float: right;
  margin-top: 1%;
}
.product-tags .button a {
  font-size: 1em;
  padding: 10px 15px;
  background: #e4292f;
  color: #fff;
  text-decoration: none;
  outline: 0;
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  -o-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
}
.span_3_of_2 .button a:hover,
.product-tags .button a:hover {
  text-shadow: 0px 0px 1px #000;
  background: #292929;
}
.product-tags p {
  font-size: 13px;
  padding: 5px 0;
  color: #969696;
  line-height: 1.8em;
}

@media only screen and (max-width: 1366px) {
  .wrap {
    width: 90%;
  }
}
@media only screen and (max-width: 1280px) {
}
@media only screen and (max-width: 1024px) {
  .wrap {
    width: 95%;
  }
  .nav a {
    padding: 16px 20px;
  }
  .navigation {
    margin: 0 30px;
  }
  .nav li li a {
    font-size: 14px;
  }
  .nav ul {
    width: 9em;
  }
  .nav > li > a {
    font-size: 14px;
  }
  .slider-img img {
    margin-top: -50px;
  }
  .slider-img {
    width: 50%;
  }
  .span_1_of_2 {
    width: 100%;
  }
  @media only screen and (max-width: 800px) {
    .nav {
      border-bottom: none;
      border-top: none;
    }
    .nav ul {
      width: 100%;
    }
    .header_bottom {
      padding: 6% 0 0% 0;
    }
    .slider-text h2 {
      font-size: 25px;
    }
    .slider-text p {
      font-size: 15px;
    }
    .slider-img img {
      margin-top: -20px;
    }
    .header_top {
      padding-bottom: 10px;
    }
    .nav > li > a {
      padding: 10px;
    }
    .content-bottom-left,
    .content-bottom-right {
      float: none;
      width: 100%;
      padding-right: 0;
    }
    .content-bottom-right {
      padding-left: 0;
      border-left: none;
      margin-top: 15px;
    }
    .span_3_of_2 {
      width: 54.2%;
    }
  }

  @media only screen and (max-width: 640px) {
    .logo {
      width: 32%;
    }
    .header_top_right {
      padding-top: 0;
    }
    .header {
      padding: 8px 0;
    }
    .toggleMenu {
      width: 94%;
    }
    .slider-text h2 {
      font-size: 22px;
    }
    .header_bottom {
      padding: 3% 0 0 0;
    }
    .slider-text p {
      margin: 15px 0;
    }
    .navigation {
      margin: 0 7%;
    }
    .slider-text a {
      font-size: 15px;
    }
    .slider-text a:before {
      border-width: 17px 8px 18px 0px;
    }
    .slider-text a:after {
      border-width: 17px 0px 18px 8px;
    }
    .ocarousel,
    .content_bottom {
      padding-top: 10px;
    }
    .buters-guide {
      margin-top: 10px;
    }
    .span_3_of_2 {
      width: 100%;
    }
    .desc {
      margin: 0;
    }
  }
  @media only screen and (max-width: 480px) {
    .logo {
      width: 35%;
      margin-top: 2px;
    }
    .toggleMenu {
      width: 92%;
      padding: 8px 15px;
    }
    .slider-text h2 {
      font-size: 20px;
    }
    .slider-text p {
      margin: 8px 0;
      font-size: 14px;
    }
    .navigation span.left-ribbon {
      background-size: 70%;
      left: -28px;
    }
    .navigation span.right-ribbon {
      background-size: 70%;
    }
    .slider-text {
      width: 70%;
    }
    .slider-img {
      width: 30%;
    }
    .slider-img img {
      margin-top: 0;
    }
    .header_bottom {
      padding: 3% 0;
    }
    .images_1_of_4 {
      width: 45%;
    }
    .copy_right,
    .footer-nav {
      float: none;
      text-align: center;
    }
    .footer-nav {
      margin-top: 20px;
    }
  }
}
@media only screen and (max-width: 320px) {
  .logo {
    float: none;
    margin: 0 auto;
    text-align: center;
    width: 50%;
  }
  .header_top_right {
    float: none;
    text-align: center;
    margin-top: 5px;
  }
  .navigation {
    margin: 0 10%;
  }
  .toggleMenu {
    width: 88%;
  }
  .footer-nav li a {
    margin: 0 4px;
  }
  .footer-nav {
    margin-top: 10px;
  }
  .slider-text,
  .slider-img {
    width: 100%;
    text-align: center;
  }
}
</style>
