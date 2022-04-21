<template>
  <div class="col text-center my-5">
    <img :src="poster" alt="immagine">
    <h3 class="my-3">{{title}}</h3>
    <h3 class="my-3">{{author}}</h3>
    <h3 class="my-3">{{year}}</h3>
  </div>
</template>

<script>
export default {
  name: 'DischiComp',
  props: {
    author: String,
    poster: String,
    title: String,
    year: String,
    genre: String,
  }
}
</script>

<style scoped lang="scss">

</style>
