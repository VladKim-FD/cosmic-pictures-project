<template>
<div class="section1">
    <div class="container">
        <h2>В КАКИХ СЛУЧАЯХ ВЫ МОЖЕТЕ ИСПОЛЬЗОВАТЬ КОСМИЧЕСКИЕ СНИМКИ В СУДЕ</h2>
        <h3>Согласно статьям 64 и 89 АПК РФ и статье 55 ГПК РФ данные космической съемки могут рассматриваться как доказательства в судебной и досудебной практике при решении земельных, имущественных и хозяйственных споров</h3>
        <div class="items">
        <div class="item" v-for="item in $store.state.items">
        <div class="top">
            <img :src="require(`../assets/images/${item.img}.png`)" alt="">
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
         
       }
    
    }
}
</script>

<style lang="scss">
@import '../scss/components/section1';
</style>