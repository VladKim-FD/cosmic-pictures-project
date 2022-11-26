<template>
<header>
<navbar></navbar>
<div class="header-content container">
    <div class="header-info">
       <h1>КОСМИЧЕСКИЕ СНИМКИ ДЛЯ СУДЕБНЫХ СПОРОВ </h1>
       <p>Обеспечиваем космическими снимками, аналитикой и экспертными заключениями 
       в качестве доказательной базы при отстаивании ваших прав в суде </p>
       <a href="#!">Заказать</a>
    </div>
    <img :src="img" alt="">
</div>
</header>
  
</template>

<script>



import navbar from './navbar.vue';
export default{
    components: {
     navbar
    },
    data(){
        return{
            img: '/src/assets/images/planet.png',
        }
        
    }
}
</script>

<style>
@import '../scss/components/header';
</style>