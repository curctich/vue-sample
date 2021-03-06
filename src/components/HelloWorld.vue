<template>
  <div>
    <p>{{ message }}</p>
    <p>{{ message_1.value }}</p>
    <p>{{ message_1.value.length }}</p>
    <p>{{ list[2] }}</p>
    <p>{{ list[num] }}</p>

    <input type="text" v-bind:value="message">
  </div>
</template>


<script>
export default {
  //name: 'HelloWorld',
  data() {
    return {
      message: 'Hello World',
      message_1: {
        value: 'Message1'
      },
      list: ['ぱんだ', 'くま', 'いるか'],
      num: 1
    }
  }
}
</script>


<style scoped>

</style>
