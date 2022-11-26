<template>
<div class="slider-block">
    <div class="container slider-content">
       <h3>ПРИМЕРЫ ПРИМЕНЕНИЯ СНИМКОВ В СУДЕБНОЙ ПРАКТИКЕ</h3>
       <div class="slider-wrapper" ref="sliderWrapper">
        <div class="slider__list" ref="sliderList">
        <div class="slider__item" v-for="slide in $store.state.slides" ref="sliderItems">
           <div class="slide-left">
            <h4>{{slide.title1}}</h4>
            <div class="slider-img">
              <img :src="require(`../assets/images/${slide.img}.png`)" alt="">
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
            <button class="icon-left prev" ref="prev" @click="prevSlide"></button>
            <button class="icon-right next" ref="next" @click="nextSlide"></button>
        </div>
       </div>
    </div>
    
</div>

</template>

<script>
import {ref, mounted} from 'vue';

export default{
    mounted() {
const sliderWrapper = this.$refs.sliderWrapper;
const sliderList = this.$refs.sliderList;
const sliderItems = this.$refs.sliderItems;
const btnPrev = this.$refs.prev;
const btnNext = this.$refs.next;
// const slider = document.querySelector('.slider');
// const sliderWrapper = document.querySelector('.slider-wrapper');
// const sliderList = document.querySelector('.slider__list');
// const sliderItems = document.querySelectorAll('.slider__item');
// const btnPrev = document.querySelector('.prev');
// const btnNext = document.querySelector('.next');

// console.log(sliderList.offsetWidth);

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

let position = 0;
let timeMove = 500;
let dotIndex = 0;

let width = sliderList.offsetWidth;

let end = width * 3;
// console.log(end);

// slider work code

const nextSlide = () => {

    if(position < end){
        position += sliderList.offsetWidth;
        // console.log(position);
        sliderList.style.left = -position + 'px';
        // sliderList.style.transition = `left ${timeMove}s`
    }
    else if(position == end){
        event.target.disabled;
    }
    // else{
    //     position = 0;
    // }

    thisSlide(dotIndex)
    
}

const prevSlide = () => {

    if(position > 0){
        position -= sliderList.offsetWidth;

        sliderList.style.left = -position + 'px';
        // console.log(position);
        // sliderList.style.transition = `left ${timeMove}s`
    }
    // else if(position == 0){
    //     event.target.disabled;
    // }
    // else{
    //     position = 0;
    // }

    thisSlide(dotIndex)
    
}

btnNext.addEventListener('click', nextSlide);
btnPrev.addEventListener('click', prevSlide);


// generating dots

const ul = document.createElement('ul');
ul.classList.add('slider__dots');
sliderItems.forEach(() => {
    const li = document.createElement('li');
    ul.appendChild(li);
})

sliderWrapper.appendChild(ul);

const dots = document.querySelectorAll('.slider__dots li');
// dots[dotIndex].classList.add('active');

const thisSlide = (index) => {
    for(let dot of dots){
        dot.classList.remove('active')
    }

    dots[index].classList.add('active')
}

dots.forEach((dot, index) => {
    dot.addEventListener('click', () => {
       position = width * index;

       sliderList.style.left = -position + 'px';
       console.log(index);
       dotIndex = index;
       thisSlide(dotIndex)
    })
})

// console.log(sliderList);
    }
}
</script>


<style lang="scss">
@import '../scss/components/slider';
</style>