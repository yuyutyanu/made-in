<template>
  <div>
      <div class="about">
        <div class="container">
          <div class="title-logo">
            <nuxt-link to="/">
             <img src="/logo.svg" alt="">
            </nuxt-link>
          </div>
          <div>
            <p>made in. とは</p>
            <p>デザイン性に優れたプロダクトサイト(製品サイト)を集めたギャラリーサイトです。<br>
              「 ものづくり」の発展の貢献を目指して合同会社ピクセルグラムが運営しています。<br>
              掲載に関してご意見ご要望がございましたら下記のメールアドレスからご連絡ください。</p>
            <p>info@pixelgram.jp</p>
          </div>
          <div class="contact">
            <p>運営会社</p>
            <p>合同会社ピクセルグラム</p>
            <p>〒552-0003 大阪府大阪市港区磯路2-2-22 カーサアトレ201</p>
            <a href="https://pixelgram.jp">https://pixelgram.jp</a>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
  export default{
    transition:'fade'
  }
</script>
<style scoped>
  .container {
    padding: 30px 35px;
  }

  .about{
    width: 100%;
    height: 100vh;
    background-color: #fafafa;
  }
  .title-logo {
    margin-bottom: 100px;
  }
</style>