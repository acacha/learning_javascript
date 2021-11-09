<template>
  <div>
    <p>{{ counter }}</p>
    <button @click="increment">+</button>
    <button @click="decrement()">-</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increment() {
      this.counter++
    },
    decrement() {
      this.counter--
    }
  }
}

</script>

<styles>

</styles>