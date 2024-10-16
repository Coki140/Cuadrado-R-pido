<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ counter }} <sup>2</sup> = {{ squareCounter }}</p>
    <button @click="decrease">Disminuir en -1</button>
    <button @click="increase">Aumentar en +1</button>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    start: {
      type: Number,
      default: 5,
      validator(value) {
        return (value) => 5;
      },
    },
  },
  data() {
    return {
      counter: this.start,
    };
  },
  methods: {
    increase() {
      this.counter++;
    },
    decrease() {
      this.counter--;
    },
  },
  computed: {
    squareCounter() {
      return this.counter * this.counter;
    },
  },
};
</script>

<style scoped>
div {
  text-align: center;
}
button {
  background-color: #64b687;
  border-radius: 5px;
  border: 1px solid #fff;
  color: #fff;
  cursor: pointer;
  margin: 10px 5px;
  padding: 5px 15px;
  transition: 0.3s ease-in-out;
}
button:hover {
  background-color: #2caa62;
  transition: 0.3s ease-in-out;
}
</style>
