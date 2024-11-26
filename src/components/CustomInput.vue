<template>
  <div class="block">
    <input :value='text' @input="event => text = event.target.value" type="text">
    <span>Значение из инпута: "{{text}}"</span>
  </div>
</template>


<script>
export default {
  name: 'CustomInput',

  data() {
    return {
      text: ''
    }
  }
}
</script>


<style scoped>
  .block {
    margin-top: 50px;
    padding: 30px;
  }

  input {
    widows: 100px;
    height: 32px;
  }

  span {
    margin-left: 30px;
  }

</style>