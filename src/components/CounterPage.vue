<template>
  <div class="container">
    <h3> how many claps for 'Her'?</h3>
    <span class="defaultCount"> {{ count }} </span>
    <div class="buttons">
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
      <button @click="setValue(25)">Set to 25</button>
      <button @click="setValue(50)">Set to 50</button>
    </div>
    <button class="reset" @click="reset">Reset</button>
  </div>
</template>
  
<script>
import useCounter from '@/composables/useCounter'

export default {
  setup() {
    const { count, increment, decrement, reset, setValue } = useCounter()

    return {
      count,
      increment,
      decrement,
      reset,
      setValue
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Mulish:wght@200&family=Stardos+Stencil:wght@700&display=swap');

.defaultCount {
  font-size: 50px;
  color: #eedada;
}

.container {
  background: linear-gradient(120deg, #272626 37%, #673736, #db5a56);
  /* background-color: #d9df7e;  */

  padding-top: 40px;
  padding-bottom: 60px;
  border-radius: 20px;
  z-index: 1;
}

.buttons {
  display: grid;
  grid-template-columns: auto auto;
  justify-content: center;
  grid-gap: 10px;
  margin-bottom: 15px;
  grid-gap: 13px;
  margin-bottom: 15px;
  margin-top: 20px;
}

button {
  width: 8rem;
  background-color: #774140;
  /* background-color: #dfb27e; */
  height: 27px;
  /* border-color: #2c3e50; */
  cursor: pointer;
  color: #eedada;
  border-radius: 5px;
}

button:hover {
  color: #d81616;
}

.reset {
  width: 20em;
}

span {
  font-family: 'Mulish', sans-serif;
  font-family: 'Stardos Stencil', cursive;
  color: white;
  font-size: 20px;
}

h3,
h5 {
  margin: 5px 0 15px 0;
  font-family: 'Righteous', cursive;
}

@media screen and (max-width: 768px) {
  .container {
    width: 90%;
    margin: auto;
  }
}
</style>