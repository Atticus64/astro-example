
<template>
  <h1>Hola Vuejs</h1>

  <div class="container">
    <h2 class="count">{{ count }}</h2>
  </div>
  <br>
  <button @click="increase" class="btn-custom" >+1</button>
  <button @click="decrease" class="btn-custom" >-1</button>
  <div class="container">
    <a href="/">Home</a>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {

    const count = ref(1)


    return {
      count,
      increase: () => count.value++,
      decrease: () => count.value--
    }
  }
}
</script>

<style>

html {
  font-family: system-ui, sans-serif;
  display: flex;
  justify-content: center;
  align-content: center;
}

.container {
  display: flex;
  align-content: center;
  justify-content: center;
}

 a {
        padding: 10px;
        color: #000;
        text-decoration: none;
        border: 1px solid #000;
        transition: all 0.3s;
    }

    a:hover {
        background-color: cornflowerblue;
        border: 1px solid #0000;
    }

.count {
  align-self: center;
  justify-self: center;
  margin: auto;
}

.btn-custom {
  padding: 10px;
  color: #000;
  text-decoration: none;
  border: 1px solid #000;
  transition: all 0.3s;
  margin: 20px;
}

.btn-custom:hover {
  background-color: aquamarine;
  border: 1px solid #0000;
}

</style>

