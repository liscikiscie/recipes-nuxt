<template>
  <section class="recipes">
    <article>
      <div>
        <h1>Title</h1>
        <p>Some nice preview text</p>
      </div>
    </article>
  </section>
</template>

<script>
  export default {
    name: 'index'
  }
</script>

<style scoped lang="scss">
  .recipes {

    .recipe {
      box-sizing: border-box;
      width: 280px;
      padding: 8px;
      border: 1px solid #ccc;
      box-shadow: 0 2px 2px #aaa;
    }
  }

</style>
