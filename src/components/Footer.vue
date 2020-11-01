<template>
  <footer id="footer">
    <div class="flex between">
      <h1 class="footer-logo">estra inc.</h1>
      <nav class="footer-nav">
        <ul>
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">service</a></li>
          <li><a href="#">works</a></li>
          <li><a href="#">price</a></li>
          <li><a href="#">contact</a></li>
        </ul>
      </nav>
      </div>
    <small>Copyright 2019 estra inc. All Rights Reserved.</small>
  </footer>
</template>

<style scoped>
footer {
  height: auto;
  background: #000;
}

.footer-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #f2f2f2;
  line-height: 70px;
}

.footer-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.footer-nav a:hover{
  text-decoration: none;
}

.footer-nav a {
  color: #f2f2f2;
}

#footer {
  height: 160px;
  text-align: center;
  line-height: 80px;
  color: #fff;
}

@media screen and (max-width: 480px) {
  .footer-logo {
  position: relative;
  left: 32%;
  padding-top: 30px;
  line-height: 0;
}

.footer-nav {
  display: none;
}

#footer {
  height: 110px;
}
}
</style>