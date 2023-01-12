<script setup>
  import {ref,reactive} from 'vue'
  import Header from './components/Header.vue'

  const cantidad = ref(10000);
  const MIN = 0;
  const MAX = 20000;
  const STEP = 100;


</script>

<template>
  <div class="my-20 max-w-lg mx-auto bg-white shadow p-10">
    <Header />

    <div class="my-5">
      <input 
        type="range"
        class="w-full bg-gray-200 accent-lime-500 hover:accent-lime-600"
        :min="MIN"
        :max="MAX"
        :step="STEP"
        v-model.number="cantidad" 
      />
      <p>$ {{ cantidad }}</p>
      <!-- Equivalente con directiva de VUE, v-text o v-html-->
      <!-- <p v-text="`$ ${cantidad}`"></p> -->
      <!-- v-model reemplaza la lineas eliminadas de
      :value="cantidad, @input='handleChange y la función de handleChange en script'-->
    </div>
  </div>
</template>


