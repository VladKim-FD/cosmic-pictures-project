<template>
<div class="section3">
    <div class="container section3-content">
        <div class="section3-info">
            <h3>КАК СДЕЛАТЬ ЗАКАЗ</h3>
            <p>Заказ можно оформить круглосуточно на нашем сайте или в рабочее время по телефону  
            +7 (495) 745-59-57. Обработка заказов, поступивших в нерабочее время, производится в ближайший к ним рабочий день.</p>
           <a href="#!">Оставить заявку</a>
        </div>
        <div class="section3-stepper">
           <ul class="stepper-list">
            <li v-for="step in $store.state.steps" :class="step.class">
            <div class="circle" @click="updateProgressBar"></div>
                <div class="step">
                 <h4>{{step.title}}</h4>
                 <p>{{step.text}}</p>
                </div>
            </li>
            
           </ul>
        </div>
    </div>
</div>
</template>

<script>
export default{
    data(){
        return {
            
        }
    },
    methods: {
        updateProgressBar(){
          let circle = event.target;
          const line = document.querySelector('.line');
          const circles = document.querySelectorAll('.circle');
          const CirclesActive = document.querySelectorAll('.circle-active');
 
        //   line.style.width = ((CirclesActive.length - 1) / (circles.length - 1)) * 100 + 'px'
   

        circles.forEach((el, index) => {
            if(circles[index] == event.currentTarget && event.currentTarget.classList.contains('active') == false){
                circles[index].classList.add('active');
                
            }

            else if(circles[index] == event.currentTarget && event.currentTarget.classList.contains('active') ){
               circles[index].classList.remove('active') 
            }
        })

        //  if(circle.classList.contains('circle-active')){
        //     circle.classList.remove('circle-active')
        //  }else{
        //     circle.classList.add('circle-active')
        //  }

    //    const circles = document.querySelectorAll('.circle');

    //    circles.forEach((el, idx) => {
    //     if(idx < )
    //    })

        }
    }
}
</script>

<style lang="scss">
@import '../scss/components/section3';
</style>