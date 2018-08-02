<template>
  <div :class="{'is-menu-open': isOpen}">
    <div class="menu">
      <div class="container">
        <div class="menu-head">
          <img src="/logo-white.svg" alt="">
        </div>
        <div class="menu-side">

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
            <img src="https://dummyimage.com/350x250/000000/fff" alt="">
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
    background-color: #000;
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
    transform: translate3d(-250px, 150px, 0);
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
  }

</style>

