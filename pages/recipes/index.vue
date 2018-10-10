<template>
  <section class="recipes">
    <Recipe
      id="1"
      thumbnail="https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg"
      title="Delicious biscuits"
      previewText="Awesome cookie"
    />

    <Recipe
      id="2"
      thumbnail="https://www.rd.com/wp-content/uploads/2018/04/9-Foods-You-Should-Never-Eat-Before-Bed-760x506.jpg"
      title="Delicious Pizza"
      previewText="Awesome Pizza!!"
    />
  </section>
</template>

<script>
  import Recipe from '@/components/Recipe.vue';

  export default {
    name: 'index',
    components: {
      Recipe
    }
  }
</script>

<style scoped>
  .recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
  }




</style>
