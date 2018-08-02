<template>
  <div :class="{'is-menu-open': isOpen}">
    <div class="menu">
      <div class="container">
        <div class="menu-head">
          <img src="/logo-white.svg" alt="">
            <ul class="menu-head-lists">
              <li>line up</li>
              <li>about</li>
              <li></li>
              <li><img src="/twitter.svg" alt=""></li>
            </ul>
        </div>
        <div class="menu-side">
          <p class="menu-side-title">category</p>
          <div class="menu-side-category">
            <ul>
              <li v-for="n in 5" :key="n">インテリア・雑貨（２３３）</li>
            </ul>
          </div>
          <div class="menu-side-category">
            <ul>
              <li v-for="n in 5" :key="n">ホワイト系</li>
            </ul>
          </div>

        </div>
        <div class="menu-btn" @click="open">
          <span class="menu-border"></span>
          <span class="menu-border"></span>
          <span class="menu-border"></span>
        </div>
      </div>
    </div>

    <div class="main">
      <div class="container">
        <div class="title-logo">
          <img src="/logo.svg" alt="">
        </div>

        <div class="gallery">
          <div class="gallery-work" v-for="n in 9" :key="n">
            <img src="https://dummyimage.com/350x250/dedede/fff" alt="">
            <div class="gallery-work-name">
              <p>Dummy</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    data(){
      return {
        isOpen: false
      }
    },
    methods: {
      open(){
        this.isOpen = !this.isOpen
      }
    }
  }
</script>

<style>

  .container {
    padding: 30px 35px;
  }

  .menu {
    width: 100%;
    height: 100vh;
    background-color: #1E1E1E;
  }

  .menu-head-lists{
    display: flex;
    position: absolute;
    right:300px;
    top:110px;
  }
  .menu-head-lists li{
    color:#fff;
    list-style: none;
    margin-right:20px;
    font-weight:bold;
    font-size:24px;
  }
  .menu-head-lists li:hover{
    border-bottom:solid 1px #fff;
  }
  .menu-head-lists li:nth-child(3){
    height:30px;
    width:1px;
    background:#fff;
    border-bottom:none;
  }

  .menu-side {
    position: absolute;
    top:180px;
    right:60px;
  }
  .menu-side-title{
    color:#fff;
    font-weight:bold;
    font-size:24px;
    margin-bottom:20px;
  }
  .menu-side-category{
    color:#fff;
    font-size:14px;
    margin-left:20px;
    line-height: 2em;
    border-bottom:solid 1px #fff;
    padding-bottom:20px;
    margin-bottom:20px;
  }
  .menu-side-category ul {
    padding:0;
  }
  .menu-side-category ul li{
    list-style: none;
  }
  .menu-side-category ul li:hover{
    border-bottom:solid 1px #fff;
  }
  .menu-side-category:last-child{
    border:none;
  }

  .menu-btn {
    position: absolute;
    right: 50px;
    top: 30px;
    z-index: 1;
  }

  .menu-border {
    display: block;
    height: 4px;
    width: 30px;
    background-color: #000;
    margin-bottom: 8px;
    transition:all .5s ease-out;
  }
  .is-menu-open .menu-border:nth-child(1){
    background-color:#fff;
    transform: translateY(12px) rotate(-45deg);
  }
  .is-menu-open .menu-border:nth-child(2){
    opacity:0;
  }
  .is-menu-open .menu-border:nth-child(3){
    background-color: #fff;
    transform:translateY(-12px) rotate(45deg);
  }

  .main {
    background: #fafafa;
    position: absolute;
    top: 0;
    left: 0;
    transition: all .5s cubic-bezier(0.86, 0, 0.07, 1), box-shadow 0.3s ease-out 0.4s;
  }

  .is-menu-open .main {
    position: fixed;
    transform: translate3d(-300px, 160px, 0);
    transition: transform 0.5s cubic-bezier(0.86, 0, 0.07, 1), box-shadow 0.3s ease-out 0.4s, -webkit-transform 0.5s cubic-bezier(0.86, 0, 0.07, 1);
  }

  .title-logo {
    margin-bottom: 100px;
  }

  .gallery {
    padding: 0 120px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .gallery-work{
    margin-bottom:30px;
    position: relative;
  }
  .gallery-work-name{
    position: absolute;
    bottom:0;
    background: #000;
    width:100%;
  }
  .gallery-work-name p{
    font-size:16px;
    padding:10px 15px;
    color:#fff;
  }

</style>

