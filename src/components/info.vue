<template>
   <div class="info">
    <div class="container info-contact">
        <h2>Почему выбирают нас</h2>
   <h3>«Терра Тех» обладает внушительным опытом поиска и анализа любой доступной пространственной информации на территории земного шара за любой период времени</h3>
   <div class="advantages">
       <div class="advantage" v-for="advantage in $store.state.advantages">
         <div class="top">
            <div class="item-icon">
                <img :src="require(`../assets/images/icons/${advantage.img}.svg`)" alt="">  
            </div>
             <h4>{{advantage.title}}</h4> 
         </div>
         <p>{{advantage.text}}</p>
       </div>
   </div>
   <h5>часто задаваемые Вопросы </h5>
   <div class="accordion">
      <div class="accordion-item" v-for="item in accordion">
         <div class="item-btn" @click="clickAcc">
            <p>{{item.title}}</p>
            <span></span>
         </div>
         <div class="item-content">
           <p>{{item.text1}}</p>
           <p>{{item.text2}}</p>
           <div class="item-paragraphs">
            <p>{{item.text3}}</p>
            <p>{{item.text4}}</p>
           </div>
         </div>
      </div>
   </div>
    </div>
   </div>
</template>

<script>
export default{
    data(){
        return {
            
            accordion: [
                {
                    title: 'Какая информация требуется для начала работы?',
                    text1: 'Для наиболее точного определения подходящего снимка специалисту потребуется уточнить следующие данные:',
                    text2 : '•	территория интереса (по возможности, сообщите координаты места и площадь);',
                    text3: '• дату или временной интервал;',
                    text4: '• решаемая при помощи космических снимков задача.'
                },
                 {
                    title: 'Сколько времени занимает подготовка необходимых материалов?',
                    text1: 'Для наиболее точного определения подходящего снимка специалисту потребуется уточнить следующие данные:',
                    text2 : '•	территория интереса (по возможности, сообщите координаты места и площадь);',
                    text3: '• дату или временной интервал;',
                    text4: '• решаемая при помощи космических снимков задача.'
                }, 
                {
                    title: 'Как осуществляется оплата?',
                    text1: 'Для наиболее точного определения подходящего снимка специалисту потребуется уточнить следующие данные:',
                    text2 : '•	территория интереса (по возможности, сообщите координаты места и площадь);',
                    text3: '• дату или временной интервал;',
                    text4: '• решаемая при помощи космических снимков задача.'
                }, 
                {
                    title: 'Как будут выглядеть снимки, отчет и экспертное заключение?',
                    text1: 'Для наиболее точного определения подходящего снимка специалисту потребуется уточнить следующие данные:',
                    text2 : '•	территория интереса (по возможности, сообщите координаты места и площадь);',
                    text3: '• дату или временной интервал;',
                    text4: '• решаемая при помощи космических снимков задача.'
                },
            ]
        }
    },
    methods: {
        clickAcc(){
        const accBtns = document.querySelectorAll('.item-btn');
        accBtns.forEach((el) => {
         el.addEventListener('click', () => {
           let accContent = el.nextElementSibling;
           let icon = el.lastChild;
           if(accContent.style.maxHeight){
             document.querySelectorAll('.content').forEach((el) => el.style.maxHeight = null);
             accContent.style.maxHeight = null;
             icon.classList.remove('active')
           }
           else{
            document.querySelectorAll('.content').forEach((el) => el.style.maxHeight = null)
            accContent.style.maxHeight = accContent.scrollHeight + 'px';
            icon.classList.add('active')
          }
         })
       })

    },
    }
}
</script>

<style lang="scss">
@import '../scss/components/info';
</style>