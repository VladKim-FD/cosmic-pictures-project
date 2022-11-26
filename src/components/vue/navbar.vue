<template>
<nav>
    <div class="container nav-content">
     <div class="nav-logo">
      <img :src="img" alt="">
      <p>Профессиональная космическая помощь</p>
     </div>
     <div class="nav-menu">
       <ul class="nav-list">
        <li v-for="link in list">
        <a href="#!">{{link.text}}</a>
        </li>
      </ul>
      <div class="nav-phone">
        <p>+7 (495) 745 59 57</p>
        <div class="phone-circle">
           <img :src="icon" alt="">
        </div>
     </div>
      
        

      </div>
      <input 
      type="checkbox" 
      class="input" 
      id="check-menu" 
      v-on:click="burgerMenu"
      >
      <div class="btn">
          <div class="hamburger-lines" >
        <!-- <span class="hamburger-line line1"></span>
        <span class="hamburger-line line2"></span>
        <span class="hamburger-line line3"></span> -->
        <span></span>
      </div>
      </div>
      
    </div>
</nav>
</template>

<script>
export default{
    data() {
        return {
          img: '/src/assets/images/nav-logo.png',
          icon: '/src/assets/images/icons/phone.svg',
          list: [
            {text: 'Применение'},
            {text: 'Примеры'},
            {text: 'Тарифы'},
            {text: 'Контакты'},
          ]
        }
       
    },
    methods: {
      burgerMenu(){
      const navLinks = document.querySelector('.nav-menu');
      const navbarBtn = document.querySelector('.input');
      const burgerBtn = document.querySelector('.hamburger-lines');

      if(navbarBtn.classList.contains('active')){
        navLinks.style = 'left: -100%; transition : left 0.5s; ';
        navbarBtn.classList.remove('active');
        burgerBtn.classList.remove('active');
      }
      else{
        navbarBtn.classList.add('active');
        burgerBtn.classList.add('active');
        navLinks.style = `left: 0; transition : left 0.5s; `
      }
    }
    }
}
</script>

<style >
  @import '../scss/components/navbar';
</style>