<template>
   <div class="info">
    <div class="container info-contact">
        <h2>Почему выбирают нас</h2>
   <h3>«Терра Тех» обладает внушительным опытом поиска и анализа любой доступной пространственной информации на территории земного шара за любой период времени</h3>
   <div class="advantages">
       <div class="advantage" v-for="advantage in advantages">
         <div class="top">
            <div class="item-icon">
                <img :src="advantage.img" alt="">  
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
            advantages: [
                {
                    img: '/src/assets/images/icons/reliability.svg',
                    title: 'Надежный поставщик данных',
                    text: 'У нас Вы можете оперативно приобрести данные съемки со всех мировых коммерчески доступных спутников за последние 20 лет, что позволяет уверенно определить историю использования и изменений на конкретном участке. '
                }, 
                {
                    img: '/src/assets/images/icons/quality.svg',
                    title: 'Гарантированное качество',
                    text: 'Дешифрование космических снимков и подготовка экспертных заключений проводится ведущими экспертами отрасли, кандидатами географических и технических наук, имеющими многолетний опыт работы с геопространственными данными.'
                },
                {
                    img: '/src/assets/images/icons/choice.svg',
                    title: 'Большой выбор снимков',
                    text: 'Доступ к базе разновременных космических снимков с российских и зарубежных космических аппаратов за последние 20 лет позволяет уверенно определить историю использования и изменений на конкретном участке.'
                }, 
                {
                    img: '/src/assets/images/icons/confidence.svg',
                    title: 'Конфиденциальность',
                    text: 'Абсолютная конфиденциальность является одним из главных принципов нашей работы. Доверяя нашим специалистам свой заказ, Вы можете быть полностью уверены, что Ваши данные будут надежно защищены.'
                },
            ],
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

<style >
@import '../scss/components/info';
</style>