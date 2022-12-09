<template>
  <div class="border border-red-400 ">
    <button @click="api">fdfsdfsdf</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

let access= ref(null)
let api = () =>{
  let headers = new Headers();

  headers.append("Authorization", "Bearer cFJZcjZ6anEwaThMMXp6d1FETUxwWkIzeVBDa2hNc2M6UmYyMkJmWm9nMHFRR2xWOQ==");

  fetch("https://sandbox.safaricom.co.ke/oauth/v1/generate?grant_type=client_credentials", { headers })

    .then(response => response.text())

    .then(result => console.log(result))

    .catch(error => console.log(error));
}
</script>

<style lang="scss" scoped>

</style>