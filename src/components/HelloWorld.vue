<template>
  <h1>{{ msg }}</h1>

  <button @click="() => (count ++)">count is: {{ count }}</button>

<p>{{ message }}</p>
    <button @click="reverseMessage">反转 Message</button>
</template>

<script>
import {toRefs, ref} from "vue";

export default {
  name: "HelloWord",
  props: {
    msg: String
  },
  setup(props) {
    const { msg } = toRefs(props);
    const count = ref(0);
    const message = ref("Hello World!")

    const reverseMessage = () => {
      message.value = message.value.split("").reverse().join("")
    }

    return {
      msg,
      count,
      message,
      reverseMessage
    }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
