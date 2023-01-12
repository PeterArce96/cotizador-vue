<script setup>
  import {ref,reactive} from 'vue'
  import Header from './components/Header.vue'

  const cantidad = ref(0); //declarar con ref
  //declarar con reactive
  const state = reactive({ 
    cantidad:0
  })

  function handleChange(e){
    console.log(e.target.value);
  }

  // mostrar con ref
  console.log(cantidad.value);

  // mostrar con reactive
  console.log(state.cantidad);
</script>

<template>
  <div class="my-20 max-w-lg mx-auto bg-white shadow p-10">
    <Header />

    <div class="my-5">
      <input 
        type="range"
        class="w-full bg-gray-200 accent-lime-500 hover:accent-lime-600"
        @input="handleChange"
      />
    </div>
  </div>
</template>


