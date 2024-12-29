<script setup>
import data from './assets/data/articles.json'
import Header from './components/headerF.vue'
import FrontPage from './components/frontPage.vue'
import ArticleCard from './components/articleCard.vue'
import Footer from './components/footerF.vue'
</script>

<template>
  <Header />
  <main>
    <FrontPage :frontPage="data.frontPage" />

    <div class="container articlesList">
      <ArticleCard v-for="article in data.articlesList" :key="article.id" :article="article" />
    </div>
  </main>
  <Footer />
</template>

<style scoped>
main {
  padding: 70px 0;
}
.articlesList {
  margin-top: 100px;
  padding: 0 20px;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
}
</style>
