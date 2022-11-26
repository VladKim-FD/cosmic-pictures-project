++<template>
<div class="section2">
    <div class="container section2-content">
   <h2>КОМУ МОГУТ ПОМОЧЬ КОСМИЧЕСКИЕ СНИМКИ</h2>
    <p class="text">Сервис «Докажи.рф» открывает доступ к данным космической съемки со спутников дистанционного зондирования Земли для самых разных пользователей</p>
    <div class="blocks">
        <div class="block" v-for="item in $store.state.items2">
        <img :src="require(`../assets/images/${item.img}.png`)" alt="">
        <p>{{item.text}}</p>
        </div>
    </div>
    </div>
</div>
</template>


<script>
  export default{
    data(){
        return{
          
        }
    }
  }
</script>

<style lang="scss">
 @import '../scss/components/section2';
</style>