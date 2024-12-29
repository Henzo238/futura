<script setup>
// eslint-disable-next-line no-unused-vars
const props = defineProps({
  frontPage: Object
})
</script>

<template>
  <div class="container" :style="{ backgroundImage: `url(${frontPage.image})` }">
    <div class="verticalLine"></div>
    <div>
      <h3>
        <span>{{ frontPage.category.toUpperCase() }}</span>
        <span>{{ frontPage.subCategory.toUpperCase() }}</span>
      </h3>

      <h1>
        <span>{{ frontPage.title }}</span>
      </h1>
    </div>
    <p>{{ frontPage.teaser }}</p>
  </div>
</template>

<style scoped>
.container {
  height: 400px;
  border: 1px solid black;
  /* background-repeat: no-repeat; */
  background-position: bottom;
  padding: 90px;
}
/* -- Pour la ligne verticale colorée à gauche du titre */
.container > div {
  position: relative;
}
.container > div::before {
  content: '';
  position: absolute;
  top: 0px;
  width: 5px;
  height: 100%;
  left: -5px;
  background: linear-gradient(var(--light-purple), var(--dark-purple));
}
/* ------------------------- */
h1 {
  font-size: 32px;
  line-height: 46px;
  color: white;
  width: 750px;
  font-family: var(--font-title);
  font-weight: bold;
}
h3 {
  font-size: 12px;
  line-height: 24px;
  color: white;
  background-color: black;
  padding: 5px 0;
  display: inline;
}
h3 span:first-child {
  letter-spacing: 0.7px;
  /* Texte avec des couleurs dégradées */
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
  background-clip: text;
  /* Pour la compatibilité de la couleur dégradée entre les différents navigateurs */
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
h3 span:last-child {
  padding: 0 10px;
  font-weight: 300;
  letter-spacing: 0.3px;
}
span {
  padding: 5px;
  background-color: black;
  white-space: pre-wrap;
}
.container > p {
  margin-top: 40px;
  padding: 25px;
  /* Arrière plan noir transparent */
  background-color: rgba(0, 0, 0, 0.487);
  color: white;
  font-weight: 300;
  line-height: 22px;
  letter-spacing: 0.7px;
  font-size: 14px;
  width: 800px;
}
</style>
