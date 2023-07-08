<template>
<div> 
  <div>
    <select v-model="$i18n.locale">
      <option v-for="locale in $i18n.availableLocales" :key="`locale-${locale}`" :value="locale">{{ locale }}</option>
    </select>
  </div>
  <h1>{{ $t("message.hello", {name: username, surname: surname}) }}</h1>
  <p>{{ $t("message.content") }}</p>
  <p> {{ $t("message.products", {count: 5}) }}</p>
  <p> {{ $t("message.comments", 5) }}</p>
</div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const username = ref('Zenen')
const surname = ref('Peraza')
   
</script>

<style scoped>

</style>
