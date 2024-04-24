<script setup>
  const name = "Vue dinamico";
  const styleColors = 'color: blue';
  const arrayColors = ["blue", "red", "peru"];
  const activo = true;

  //////////////////
  // array

  const arrayFrutas = [ "Manzana", "Pera", "Nanano", "Piña" ];


</script>

<template>
  <h1>hola {{ name.toUpperCase() }}</h1>
  <br>
  <h2 :style="styleColors">Soy azul</h2>
  <br>
  <h2 :style="`color: ${arrayColors[2]}`">{{ arrayColors }}</h2>
  <br>
  <h2>
    {{ activo ? "Estoy Activo" : "Estoy Inactivo" }}
  </h2>
  <br>
  <p v-if="activo">Estoy Activo</p>
  <p v-if="!activo">Estoy Inactivo</p>
  <br>
  <p v-if="activo === true">
    Estoy Activo!!!
  </p>
  <p v-else-if="activo === null">
    Otro Inactivo :( con  null
  </p>
  <p v-else>
    Estoy Inactivo!!!
  </p>
  <br>
  <h1 v-show="activo">v-show :()</h1>
  <h1 v-show="!activo">!v-show :()</h1>

  <br>
  <ul>
    <li v-for="(fruta, index) in arrayFrutas" :key="index">
      {{  index }} - {{ fruta }}
    </li>
  </ul>


</template>

<style>
  h1{
    color: red;
  }
</style>