<template>
<div class="form-block">
    <div class="container form-content">
        <h3>оставьте вашу заявку</h3>
        <form action="">
          <div class="user-info">
            <input type="text" placeholder="Ваше имя" @click="textDissapear" required>
            <input type="text" placeholder="Номер телефона" required>
            <input type="email" placeholder="E-mail" required>
          </div>
          <input type="text" placeholder="Ваш вопрос" required >
          <input type="text" class="last-input" placeholder="Кадастровый номер или адрес интересующего вас объекта">
          <button type="submit">Отправить</button>
        </form>
         <p>Нажимая «Отправить», я даю согласие на обработку персональных данных в соответствии с Федеральным законом № 152-ФЗ «О персональных данных» от 27.07.2006. и соглашаюсь с Политикой конфиденциальности</p>
    </div>
</div>
</template>

<script>
export default{
  methods: {
 
  }
}
</script>

<style >
@import '../scss/components/form';
</style>