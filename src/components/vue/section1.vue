<template>
<div class="section1">
    <div class="container">
        <h2>В КАКИХ СЛУЧАЯХ ВЫ МОЖЕТЕ ИСПОЛЬЗОВАТЬ КОСМИЧЕСКИЕ СНИМКИ В СУДЕ</h2>
        <h3>Согласно статьям 64 и 89 АПК РФ и статье 55 ГПК РФ данные космической съемки могут рассматриваться как доказательства в судебной и досудебной практике при решении земельных, имущественных и хозяйственных споров</h3>
        <div class="items">
        <div class="item" v-for="item in items">
        <div class="top">
            <img :src="item.img" alt="">
            <p>{{item.title}}</p>
        </div>
        <p class="item-text">{{item.text}}</p>
        </div>
    </div>
    </div>
    
</div>
</template>


<script>
export default{
    data(){
       return {
         items: [
            {
            img: '/src/assets/images/circle.png',
            title: 'определение дат',
            text: 'Определение даты постройки зданий и сооружений'
        },
         {
            img: '/src/assets/images/circle.png',
            title: 'нарушение границ',
            text: 'Выявление нарушения границ участка и условий землепользования'
        },
         {
            img: '/src/assets/images/circle.png',
            title: 'незаконная деятельность',
            text: 'Фиксация незаконной деятельности на территории леса, ООПТ'
        },
        {
            img: '/src/assets/images/circle.png',
            title: 'подтверждение ущерба',
            text: 'Оценка достоверности страховых случаев и страховых премий'
        },
           {
            img: '/src/assets/images/circle.png',
            title: 'соблюдение сроков',
            text: 'Мониторинг сроков выполнения строительных и земельных работ'
        },
        {
            img: '/src/assets/images/circle.png',
            title: 'экомониторинг',
            text: 'Анализ экологической ситуации, выявление незаконных свалок'
        }
         ]
       }
    
    }
}
</script>

<style lang="scss">
@import '../scss/components/section1'
</style>