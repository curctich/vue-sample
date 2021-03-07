<template>
  <div>

    <p>{{ message }}</p>
    <p>{{ message_1.value }}</p>
    <p>{{ message_1.value.length }}</p>
    <p>{{ list[2] }}</p>
    <p>{{ list[num] }}</p>

    <input type="text" v-bind:value="message">

    <div v-bind:text-content.prop="message_2"></div>

    <p>{{ count }}回クリックdone</p>
    <button v-on:click="increment">カウントを増やす</button>

    <p v-bind:class="{ child: idChild, 'is-active': isActive }">Text</p>
    <p v-bind:style="{ color: textColor,backgroundColor: bgColor }">Text</p>

    <p v-bind:class="classObject">Text</p>
    <p v-bind:style="styleObject">Text</p>

  </div>
</template>


<script>
export default {
  data() {
    return {
      message: 'Hello World',
      message_1: {
        value: 'Message1'
      },
      list: ['ぱんだ', 'くま', 'いるか'],
      num: 1,
      message_2: 'Message2',
      count: 0,
      isChild: true,
      isActive: true,
      textColor: 'red',
      bgColor: 'lightgray',
      classObject: {
        child: true,
        'is-active': false
      },
      styleObject: {
        color: 'blue',
        backgroundColor: 'lightblue'
      }
    }
  },
  methods: {
    increment: function () {
      this.count += 1
    }
  }
}
</script>


<style scoped>

</style>
