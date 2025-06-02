<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>Спеціальність: 121</p>
    <p>Курс: 3</p>
    <p>Група: 3ПР1</p>
    <p>ПІБ: Сілецький Антон Олегович</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.hello {
  text-align: center;
  margin-top: 2rem;
}
</style>
