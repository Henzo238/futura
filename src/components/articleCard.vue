<script setup>
// eslint-disable-next-line no-unused-vars
const props = defineProps({
  article: Object
})
</script>

<template>
  <div class="articleCard">
    <img :src="article.image" :alt="article.title" />

    <p>
      <!-- Utilisation de la méthode JavaScript '.toUpperCase()' pour mettre ces textes en majuscule -->
      <span>{{ article.category.toUpperCase() }}</span>
      <span>{{ article.subCategory.toUpperCase() }}</span>
    </p>

    <h2>{{ article.title }}</h2>

    <p class="date">{{ article.date }}</p>
  </div>
</template>

<style scoped>
.articleCard {
  /* Calcul : la largeur disponible du parent ('100%') moins les espaces qu'il y aura entre chaque carte (3 x 30px => 90px). Le résultat de cette soustraction est divisé par 4 car on veut 4 cartes par ligne */
  width: calc((100% - 90px) / 4);
  height: 480px;
}
img {
  width: 100%;
  height: 350px;
  object-fit: cover;
  margin-bottom: 15px;
}
span {
  font-size: 12px;
}
span:first-child {
  margin-right: 10px;
  font-weight: bold;
  letter-spacing: 0.7px;
  /* Texte avec des couleurs dégradées */
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
  /* Pour la compatibilité de la couleur dégradée entre les différents navigateurs */
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
span:last-child {
  font-weight: 300;
  letter-spacing: 0.3px;
}
h2 {
  margin: 10px 0;
  font-family: var(--font-title);
  font-size: 17px;
  font-weight: bolder;
  line-height: 20px;
}
.date {
  letter-spacing: 0.3px;
  font-weight: 300;
  font-size: 12px;
  color: var(--grey);
}
</style>
