<template>

  
  <div id="app">
    <section class="section has-background-warning" style="min-height:100vh">
      <div class="container" id="calculadora">
        <div class="columns is-multiline is-mobile">
          <div class="column is-9">
            <input type="text" class="input is-fullwidth" v-model="operacion">
          </div>
          <div class="column is-3">
            <button class="button is-danger is-fullwidth" @click="clear()">Clear</button>
          </div>
          <div class="column is-10">
            <div class="columns is-multiline is-mobile">
              <tecla v-for="tecla in numeros" :texto="tecla" clases-columna="is-one-third" clases-tecla="is-dark"></tecla>
            </div>
          </div>
          <div class="column is-2">
            <div class="columns is-multiline">
              <tecla v-for="tecla in signos" :texto="tecla" clases-columna="is-full" clases-tecla="is-link"></tecla>
            </div>
          </div>
          <div class="column is-full">
            <button class="button is-success is-medium is-fullwidth" @click="calcular()">=</button>
          </div>
        </div>
      </div>
    </section>
  </div>
  
  
  </template>

<script setup>


</script>


<style >
#calculadora {
			max-width:500px;
			background-color: #ddd;
			border-radius: 10px;
			padding: 25px;
		}
</style>