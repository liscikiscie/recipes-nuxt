<template>
  <section class="single-recipe">
    <h1>TITLE</h1>
    <div>
      <img src="" alt="">
    </div>
    <p>The recipe description</p>
  </section>
</template>

<script>
  export default {
    name: 'index'
  }
</script>

<style scoped>
  .single-recipe {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px;
  }
</style>
