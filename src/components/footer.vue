<template>
  <div class="footer">
    <div class="container footer-info">
        <div class="footer-contacts">
            <div class="footer-phone">
                <p>+7 (495) 745 59 57</p>
                <a href="tel:+7(495)7455957">Перезвоните мне</a>
            </div>
            <div class="footer-email">
                <img src="../assets/images/icons/letter.svg" alt="">
                <p> info@terratech.ru</p>
            </div>
            <p class="address">г. Москва, Каширское шоссе, дом 3, корпус 2, строение 4 </p>
        </div>
        <div class="footer-extra">
            <div class="footer-logo">
                <img src="../assets/images/footer-logo.png" alt="">
                <p>Профессиональная космическая помощь</p>
            </div>
            <p>© АО "ТЕРРА ТЕХ", 2020</p>
            <p>Политика конфиденциальности</p>
        </div>
    </div>
  </div>
</template>

<script>
export default{
    data(){
        return {
            img: '',
            logo: ''
        }
    }
}
</script>

<style lang="scss">
@import '../scss/components/footer';
</style>