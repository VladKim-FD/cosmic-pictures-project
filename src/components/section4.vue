<template>
<div class="section4">
    <div class="container section4-info">
       <h3>тарифы</h3>
       <p class="tarif">Выберите тариф с учетом необходимых параметров и  узнайте, сколько будет стоить заказ</p>
       <div class="cards">
          <div :class="'card ' + card.class" v-for="card in cards">
            <h4>{{card.title}}</h4>
            <p>{{card.text}}</p>
            <h5>{{card.price}}</h5>
            <a href="#!">Заказать</a>
          </div>
       </div>
       <p class="warning">Информация носит исключительно информационный характер и ни при каких условиях не является публичной офертой.</p>
       <div class="contract">
         <p>Мы работаем по договору</p>
         <img src="../assets/images/icons/contract.svg" alt="">
       </div>
    </div>
</div>
</template>

<script>
export default{
    data(){
        return {
            icon: '',
            cards: [
                {
                    title: 'Космические снимки',
                    text: 'Снимки подбираются специалистами на определенную территорию и даты по запросу заказчика',
                    price: 'от 8 000 руб.',
                    class: 'card1'
                }, 
                {
                    title: 'Экспертное заключение',
                    text: 'Отчет содержит аналитические заключения по результатам дешифрирования космических снимков',
                    price: 'от 50 000 руб.',
                    class: 'card2'
                },  
                {
                    title: 'Космоснимки с экспертным заключением ',
                    text: 'Снимки и подробное заключение специалиста на основе космосъемки и кадастровых данных',
                    price: 'от 58 000 руб.',
                    class: 'card3'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
   @import '../scss/components/section4';
</style> 