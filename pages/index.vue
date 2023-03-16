<template>
  <div class="container">
  <AboutMe />
  <div class="content">
      <ArticleCard 
        v-for="article in articles"
        :key="article.slug"
      />
  </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      articles: [1, 2, 3, 4, 5, 6]
    }
  }
}
</script>

<style scoped>
  .container{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-width: 100vh;
  }

  .content{
    display: flex;
    align-items: flex-start;
    justify-content: space-around ;
    width: 100%;
  }
</style>