<template>
  <button :style="'background-color:' + couleur">
    <!-- IL s'agit des paramètres du bouton-->
    <slot>Magique</slot>
  </button>
</template>

<script>
export default {
  name: "BoutonMagique",
  props: {
    couleur: {
      type: String,
      // default: "green",
    },
  },
};
</script>

<style scoped>
button {
  background-color: green;
  color: white;
  font-weight: bold;
  border-radius: 10px;
  padding: 2px 4px;
}
</style>
