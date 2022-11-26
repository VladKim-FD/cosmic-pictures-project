<template>
<div class="slider-block">
    <div class="container slider-content">
       <h3>ПРИМЕРЫ ПРИМЕНЕНИЯ СНИМКОВ В СУДЕБНОЙ ПРАКТИКЕ</h3>
       <div class="slider-wrapper">
        <div class="slider__list">
        <div class="slider__item" v-for="slide in slides">
           <div class="slide-left">
            <h4>{{slide.title1}}</h4>
            <div class="slider-img">
              <img :src="slide.img" alt="">
            </div>
           </div>
           <div class="slide-right">
            <div class="text1">
                <h5>{{slide.title2}}</h5>
                <p>{{slide.text1}}</p>
            </div>
            <div class="text2">
                <h5>{{slide.title3}}</h5>
                <p>{{slide.text2}}</p>
            </div>
           </div>
        </div>
        
       </div>
       <div class="slider__controls">
            <button class="icon-left prev"></button>
            <button class="icon-right next" @click="nextSlide"></button>
        </div>
       </div>
    </div>
    
</div>

</template>

<script>

export default{
  data(){
    return {
        slides: [
            {
                title1: 'Кейс — Нарушение условий аренды земельного участка',
                img: '/src/assets/images/slide1.png',
                title2: 'Задача',
                text1: 'Определить факт нарушения условий аренды земельного участка и его использования не по назначению.',
                title3: 'Решение',
                text2: 'Архивные космические снимки за даты, предшествующие заключению договора аренды, подтвердили отсутствие рубок и нарушений в лесном покрове. На снимках за даты нахождения участка в долговременной аренде зафиксировано возведение капитальных строений и вырубка леса. В отчёте также подсчитан ущерб, нанесенный неправомерной деятельностью.'
            },
            {
                title1: 'Кейс — Раздел имущества супругов',
                img: '/src/assets/images/slide2.png',
                title2: 'Задача',
                text1: 'Определить имущество, принадлежавшее одному из супругов до вступления в брак, на конкретной территории для предъявления в судебном споре при разделе земельного участка и имущества в рамках бракоразводного процесса.',
                title3: 'Решение',
                text2: 'Архивные космические снимки за даты, предшествующие заключению брака, подтвердили наличие спорного имущества на указанной территории. В подготовленных для заказчика материалах указана дата съемки, координаты объекта, являющегося предметом имущественного спора, дана привязка к кадастру.'
            },
            {
                title1: 'Кейс — Подтверждение ущерба имуществу в результате ЧС',
                img: '/src/assets/images/slide3.png',
                title2: 'Задача',
                text1: 'Подтвердить нахождение имущества в зоне чрезвычайной ситуации, факт нанесения ему ущерба для дальнейшего обращения в страховую компанию или суд.',
                title3: 'Решение',
                text2: 'Сравнительный анализ двух разновременных снимков до и после наступления чрезвычайной ситуации подтвердил нахождение имущества в зоне стихийного бедствия, а также нанесение ему ущерба. Данная информация в дальнейшем может использоваться страховой компанией или участниками судебного процесса для расчета компенсации за повреждение имущества. '
            }, 
            {
                title1: 'Кейс — Несанкционированная свалка вблизи заповедника',
                img: '/src/assets/images/slide4.png',
                title2: 'Задача',
                text1: 'Зафиксировать факт наличия и увеличения объемов незаконной мусорной свалки на самовольно занятом земельном участке вблизи особо охраняемой природной территории (заповедника).',
                title3: 'Решение',
                text2: 'Анализ космических снимков подтвердил факт наличия свалки вблизи заповедника, которая увеличивалась за период 2017-2019 гг. Оценен предварительный экологический ущерб. Установлен факт нарушения природоохранного законодательства и норм землепользования в конкретный период времени, с указанием кадастровых границ и координат.'
            },
        ]
    }
  },
}

// const slider = document.querySelector('.slider');
// const sliderWrapper = document.querySelector('.slider-wrapper');
// const sliderList = document.querySelector('.slider__list');
// const sliderItems = document.querySelectorAll('.slider__item');
// const btnPrev = document.querySelector('.prev');
// const btnNext = document.querySelector('.next');

// // console.log(sliderList.offsetWidth);
// console.log(sliderList);

// let activeSlide = 0;
// let moveSlide = sliderList.offsetWidth;

// let dir = 'X';

// sliderItems.forEach((slide, num) => {
//     if(num != activeSlide){
//         slide.style.transform = `translate${dir}(${moveSlide}px)`;
//     }
//     if(num == sliderItems.length - 1){
//         slide.style.transform = `translate${dir}(${-moveSlide}px)`;
//     }
// })

// console.log(sliderItems.length);


// console.log(btnNext);
// console.log(btnPrev);

// if(btnNext){
// btnNext.addEventListener('click', function(){move(btnNext)})
// }
// if(btnPrev){
// btnPrev.addEventListener('click', function(){move(btnPrev)})
// }


// function move(btn){

//     console.log(moveSlide);
    
//     let btnPrevOrNext = btn == btnNext ? -moveSlide : moveSlide ;

//     sliderItems[activeSlide].style.transform = `translate${dir}(${btnPrevOrNext}px)`;
//     sliderItems[activeSlide].style.transition = `${timeMove}ms`;

//     if(btn == btnNext){
//         activeSlide++;
//         // console.log(activeSlide);
//         if(activeSlide >= sliderItems.length){
//             activeSlide = 0;
//         }
//     }
//     else if(btn == btnPrev){
//         activeSlide--;
//         if(activeSlide < 0){
//             activeSlide = sliderItems.length - 1;
//         }
//     }

//     sliderItems[activeSlide].style.transform = `translate${dir}(${0}px)`;
//     sliderItems[activeSlide].style.transition = `${timeMove}ms`;
// }

// let position = 0;
// let timeMove = 500;
// let dotIndex = 0;

// let width = sliderList.offsetWidth;

// let end = width * 3;
// console.log(end);

// // slider work code

// const nextSlide = () => {

//     if(position < end){
//         position += sliderList.offsetWidth;
//         console.log(position);
//         sliderList.style.left = -position + 'px';
//         // sliderList.style.transition = `left ${timeMove}s`
//     }
//     else if(position == end){
//         event.target.disabled;
//     }
//     // else{
//     //     position = 0;
//     // }

//     thisSlide(dotIndex)
    
// }

// const prevSlide = () => {

//     if(position > 0){
//         position -= sliderList.offsetWidth;

//         sliderList.style.left = -position + 'px';
//         console.log(position);
//         // sliderList.style.transition = `left ${timeMove}s`
//     }
//     // else if(position == 0){
//     //     event.target.disabled;
//     // }
//     // else{
//     //     position = 0;
//     // }

//     thisSlide(dotIndex)
    
// }

// btnNext.addEventListener('click', nextSlide);
// btnPrev.addEventListener('click', prevSlide);


// // generating dots

// const ul = document.createElement('ul');
// ul.classList.add('slider__dots');
// sliderItems.forEach(() => {
//     const li = document.createElement('li');
//     ul.appendChild(li);
// })

// sliderWrapper.appendChild(ul);

// const dots = document.querySelectorAll('.slider__dots li');
// // dots[dotIndex].classList.add('active');

// const thisSlide = (index) => {
//     for(let dot of dots){
//         dot.classList.remove('active')
//     }

//     dots[index].classList.add('active')
// }

// dots.forEach((dot, index) => {
//     dot.addEventListener('click', () => {
//        position = width * index;

//        sliderList.style.left = -position + 'px';

//        dotIndex = index;
//        thisSlide(dotIndex)
//     })
// })





</script>


<style  lang="scss">
@import '../scss/components/_slider.scss';
</style>