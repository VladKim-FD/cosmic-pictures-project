<template>
<div class="section2">
    <div class="container section2-content">
   <h2>КОМУ МОГУТ ПОМОЧЬ КОСМИЧЕСКИЕ СНИМКИ</h2>
    <p class="text">Сервис «Докажи.рф» открывает доступ к данным космической съемки со спутников дистанционного зондирования Земли для самых разных пользователей</p>
    <div class="blocks">
        <div class="block" v-for="item in items">
        <img :src="item.img" alt="">
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
           items: [
                {
                    img: '/src/assets/images/man.png',
                    text: 'Физические лица'
                },
                {
                    img: '/src/assets/images/umbrella.png',
                    text: 'Страховые компании'
                },
                {
                   img: '/src/assets/images/organisation.png',
                    text: 'Некоммерческие организации'
                },
                {
                    img: '/src/assets/images/signal.png',
                    text: 'Правоохранительные органы'
                },
                {
                    img: '/src/assets/images/court.png',
                    text: 'Правозащитные организации'
                },
                {
                    img: '/src/assets/images/ecology.png',
                    text: 'Экологические правозащитники'
                },
            ]
        }
    }
  }
</script>

<style lang="scss">
 @import '../scss/components/section2';
</style>