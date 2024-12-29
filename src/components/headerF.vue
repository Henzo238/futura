<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
</script>

<template>
  <header>
    <img src="C:\Users\henzo\OneDrive\Images\logo futura.svg" alt="logo Futura" />

    <nav>
      <p>SCIENCES <FontAwesomeIcon :icon="['fas', 'angle-down']" /></p>
      <p>SANTE <FontAwesomeIcon :icon="['fas', 'angle-down']" /></p>
      <p>TECH <FontAwesomeIcon :icon="['fas', 'angle-down']" /></p>
      <p>MAISON <FontAwesomeIcon :icon="['fas', 'angle-down']" /></p>
      <p>PLANETE <FontAwesomeIcon :icon="['fas', 'angle-down']" /></p>
    </nav>

    <a href="#">S'ABONNER</a>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
  color: white;
  height: 60px;
  padding: 0 55px;
}
nav {
  display: flex;
  gap: 25px;
}
svg {
  margin-left: 5px;
}
a {
  background-color: var(--yellow);
  padding: 10px 15px;
  font-size: 14px;
  border: none;
  /* Pour dire au bouton de prendre la couleur de texte, la police de caractère et la taille de caractère de son parent */
  color: inherit;
  font-family: inherit;
  font-size: inherit;
  text-decoration: none;
}
</style>
