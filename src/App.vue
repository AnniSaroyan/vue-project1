<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref } from 'vue';

let count = ref (0)
let countTen = ref (0)

function increment(){
  count.value++
}

function decrement(){
  count.value--
}

function incrementTen(){
  countTen.value +=10
}

function decrementTen(){
  countTen.value -=10
}

function reset(){
  count.value = 0
  countTen.value = 0
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />

    <div>
      <button @click="decrement()">-</button>
    <span>{{ count }}</span>
    <button @click="increment()">+</button>
      </div>

      <div>
        <button @click="decrementTen()">-10</button>
    <span>{{ countTen }}</span>
    <button @click="incrementTen()">+10</button>
      </div>  
    

    <button @click="reset()">reset</button>
    
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
