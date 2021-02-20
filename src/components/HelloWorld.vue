<template>
  <h1>{{ msg }}</h1>

  <button @click="() => (count ++)">count is: {{ count }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>

    <p>{{ message }}</p>
    <button @click="reverseMessage">反转 Message</button>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "HelloWord",
  props: {
    msg: String
  },
  data() {
    return {
      count: 0,
      message: "Hello World!"
    }
  },
  methods: {
    reverseMessage() {
      console.log(this)
      this.message = this.message.split("").reverse().join("")
    }
  }
})
</script>

<!--<script setup>-->
<!--import { defineProps, reactive, ref } from 'vue'-->

<!--defineProps({-->
<!--  msg: String-->
<!--})-->

<!--const state = reactive({ count: 0 })-->
<!--console.log(state);-->

<!--const message = ref(0);-->
<!--message.value = "hello world!"-->

<!--const reverseMessage = () => {-->
<!--  message.value = message.value-->
<!--      .split('')-->
<!--      .reverse()-->
<!--      .join('')-->
<!--}-->
<!--console.log(message);-->
<!--</script>-->

<style scoped>
a {
  color: #42b983;
}
</style>