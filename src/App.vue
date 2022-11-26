<template>
  <headerVue></headerVue>
  <section1></section1>
  <slider></slider>
  <section2></section2>
  <section3></section3>
  <section4></section4>
  <section5></section5>
  <info></info>
  <formVue></formVue>
  <footerVue></footerVue>
  <!-- <router-view/> -->
</template>

<script>

  import headerVue from './components/header.vue';
  import section1 from './components/section1.vue';
  import slider from './components/slider.vue';
  import section2 from './components/section2.vue';
  import section3 from './components/section3.vue';
  import section4 from './components/section4.vue';
  import section5 from './components/section5.vue';
  import info from './components/info.vue';
  import formVue from './components/form.vue';
  import footerVue from './components/footer.vue'
  export default{
    components: {
      headerVue,
      section1,
      slider,
      section2,
      section3,
      section4,
      section5,
      info,
      formVue,
      footerVue
    }
  }
</script>

<!-- <style lang="scss">

</style> -->
