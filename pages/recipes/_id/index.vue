<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img
        class="recipe-img"
        :src="recipe.thumbnail"
        :alt="recipe.title"
      >
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
  export default {
    name: 'index',
    asyncData( context ) {
      return new Promise((( resolve, reject ) => {
        setTimeout(() => {
          resolve({
            recipe: [
              {
                id: '1',
                title: 'Delicious biscuits',
                previewText: 'Awesome cookie!!',
                descriptionText: 'fucking awesome',
                thumbnail: 'https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg'
              },
              {
                id: '2',
                title: 'Delicious Pizza',
                previewText: 'Awesome Pizza!!',
                descriptionText: 'fucking awesome',
                thumbnail: 'https://www.rd.com/wp-content/uploads/2018/04/9-Foods-You-Should-Never-Eat-Before-Bed-760x506.jpg'
              }
            ].find(el => el.id === context.params.id)
          })
        }, 1500)
      }))
    }
  }
</script>

<style scoped>
  .single-recipe {
    display: flex;
    flex-flow: column wrap;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px;
  }

  .recipe-img {
    width: 100%;
    height: 400px;
  }
</style>
