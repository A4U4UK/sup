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
          <a class="toggleMenu" href="#">Menu</a>
          <ul class="nav">
            <li>
              <a href="index.html">Home</a>
            </li>
            <li class="test , q-pa-md q-gutter-sm">
              <a href="#" onclick="alert('Функция пока не работает')"
                >Computers</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Health & Beauty</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Home & Garden</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Office Supplies</a
              >
            </li>
            <li>
              <a href="#" onclick="alert('Функция пока не работает')"
                >Sports Equipment</a
              >
            </li>
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
            <a href="#">Наш оффициальный сайт</a>
          </div>
          <div class="slider-img">
            <img src="./images/slider-img.png" alt="" />
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
                  <span>We want you to be happy with your purchase.</span>
                </p>
                <p>
                  So we're committed to giving you all the tools to make the
                  right decision with minimum fuss.
                </p>
              </div>
            </div>

            <div class="content-bottom-right">
              <h3>Browse All Categories</h3>
              <div class="section group">
                <div class="grid_1_of_4 images_1_of_4">
                  <h4>
                    <a>{{ products.name }}</a>
                  </h4>
                  <a href="./components\preview.vue">
                    <img src="./images/product-img1.jpg" alt="" />
                  </a>
                  <div class="price-details">
                    <div class="price-number">
                      <p>
                        <span class="rupees">{{ products.price }}</span>
                      </p>
                    </div>
                    <div class="add-cart">
                      <h4>
                        <router-link to="./components/preview.vue"
                          >More Info</router-link
                        >
                      </h4>
                    </div>
                    <div class="clear"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="product-articles">
              <ul>
                <li>
                  <div class="article">
                    <p>
                      Cras aliquam, odio ac consectetur tincidunt, eros nunc
                      fermentum augue, quis rutrum ante lectus ac lectus. Fusce
                      sed tellus orci, et feugiat urna. Integer et dictum leo.
                      Nulla consectetur tempus orci sed consequat. Mauris cursus
                      est a sapien venenatis faucibus. Etiam sagittis convallis
                      volutpat.
                    </p>
                    <p><a href="#">+ Read Full article</a></p>
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
            <li><a href="#">Terms of Use</a> :</li>
            <li><a href="#">Privacy Policy</a> :</li>
            <li><a href="#">Contact Us</a> :</li>
            <li><a href="#">Sitemap</a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "@nuxt/composition-api";
import { supabase } from "supabase-nuxt";
const { data, error } = await supabase.from("products").select();
</script>

<style>
div,
span,
applet,
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
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
dl,
dt,
dd,
ol,
nav ul,
nav li,
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
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
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
ol,
ul {
  list-style: none;
  margin: 0;
  padding: 0;
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
table {
  border-collapse: collapse;
  border-spacing: 0;
}
.nav {
  padding-left: 50px;
}
.sait {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  background-color: #f6f6f6;
}
a {
  text-decoration: none;
}
.clear {
  clear: both;
}
img {
  max-width: 100%;
}

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
  padding: 20px 0;
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
  background: url(./images/left-fold.png) no-repeat;
}
.navigation span.right-ribbon {
  position: absolute;
  right: -40px;
  top: 8px;
  width: 40px;
  height: 60px;
  background: url(./images/right-fold.png) no-repeat;
}
.toggleMenu {
  display: none;
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
  .nav > li {
    background-position: 95% 50%;
  }
  .nav li li {
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
  margin-top: -60px;
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
/** categories **/

.buters-guide h3 {
  font-size: 1.1em;
  color: #fff;
  padding: 10px;
  padding-left: 25px;
  background: #e44f2b;
  position: relative;
  margin-bottom: 5px;
}
.content-bottom-right h3 {
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
.content-bottom-right h3:before,
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
  margin: 1% 0 1% 1.6%;
}
.grid_1_of_4:first-child {
  margin-left: 0;
}
.images_1_of_4 {
  width: 20.72%;
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
.add-cart h4 a {
  font-size: 0.85em;
  display: block;
  padding: 6px 20px;
  background: #8fa7ae;
  color: #fff;
  text-decoration: none;
  outline: 0;
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  -o-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  position: relative;
}
.add-cart h4 a:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  border-width: 14px 0px 12px 5px;
  border-style: solid;
  border-color: rgba(255, 0, 0, 0) rgba(0, 0, 255, 0) rgba(0, 128, 0, 0) #fff;
}
.add-cart h4 a:before {
  content: "";
  position: absolute;
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
/*** Footer ***/
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
.price-number {
  margin: 5px 0;
}
li .price-number {
  text-decoration: line-through;
  color: #e44f2b;
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
    width: 44.72%;
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
