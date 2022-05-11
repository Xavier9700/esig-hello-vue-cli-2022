<template>
  <!-- Association et création de la class "actif" au boutons-->
  <!-- Association des propriétés couleur et couleur de texte au bouton-->
  <button
    :style="'background-color:' + couleur + '; color:' + couleurTxt"
    :class="{ actif }"
    @click="$emit('coucou')"
  >
    <slot>Magique</slot>
    <!-- propriété du texte du bouton-->
  </button>
</template>

<script>
export default {
  name: "BoutonMagique",
  props: ["couleur", "couleurTxt"],
  // default: "green",
  data() {
    return {
      actif: false, // Défini si actif est actif ou non
    };
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
/*Style apporté au bouton s'il a la class actif active*/
button.actif {
  border: 4px solid black;
}
</style>
