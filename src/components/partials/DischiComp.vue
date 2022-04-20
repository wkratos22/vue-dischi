<template>
  <div>
      <img :src="poster" alt="">
      <h3 class="my-3">{{title}}</h3>
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
  }
}
</script>

<style scoped lang="scss">

</style>