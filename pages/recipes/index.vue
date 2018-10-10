<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :id="recipe.id"
      :title="recipe.title"
      :thumbnail="recipe.thumbnail"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script>
  import Recipe from '@/components/Recipe.vue';

  export default {
    name: 'index',
    components: {
      Recipe
    },
    asyncData() {
      return new Promise((( resolve, reject ) => {
        setTimeout(() => {
          resolve({
            recipes: [
              {
                id: '1',
                title: 'Delicious biscuits',
                previewText: 'Awesome cookie!!',
                thumbnail: 'https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg'
              },
              {
                id: '2',
                title: 'Delicious Pizza',
                previewText: 'Awesome Pizza!!',
                thumbnail: 'https://www.rd.com/wp-content/uploads/2018/04/9-Foods-You-Should-Never-Eat-Before-Bed-760x506.jpg'
              }
            ]
          })
        }, 1500)
      }))
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
