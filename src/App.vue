<script setup>
  import {ref,reactive} from 'vue'
  import Header from './components/Header.vue'

  const cantidad = ref(10000);
  const MIN = 0;
  const MAX = 20000;
  const step = 100;
  

  function handleChange(e){
    cantidad.value = Number(e.target.value);
  }

</script>

<template>
  <div class="my-20 max-w-lg mx-auto bg-white shadow p-10">
    <Header />

    <div class="my-5">
      <input 
        type="range"
        class="w-full bg-gray-200 accent-lime-500 hover:accent-lime-600"
        min="0"
        max="20000"
        step="100"
        value="10000"
        @input="handleChange"
      />
      <p>$ {{ cantidad }}</p>
      <!-- Equivalente con directiva de VUE, v-text o v-html-->
      <!-- <p v-text="`$ ${cantidad}`"></p> -->
    </div>
  </div>
</template>


