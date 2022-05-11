<template>
  <div>
    <h1>Produits</h1>
    <ul>
      <li>{{ nom }}</li>
      <li>{{ prenom }}</li>
      <li>{{ mot }}</li>
    </ul>
    <!--    Code qui, quand on click sur le bouton, renvoi vers @click et écrir un msg au mot-->
    <BoutonMagique @coucou="mot = 'Bienvenue'" couleur="red"
      >Bonjour</BoutonMagique
    >
    <BoutonMagique @coucou="mot = 'Au-revoir'">Adieu</BoutonMagique>
    <BoutonMagique @coucou="mot = 'Ciao fréfo'" couleur="blue" couleur-txt="red"
      >Tcho</BoutonMagique
    >
    <BoutonMagique @coucou="MotAurevoir" couleur="purple" couleur-txt="black"
      >Adieu</BoutonMagique
    >
  </div>
</template>

<script>
/* @ représente le dossier src/ de l'app */

import BoutonMagique from "@/components/BoutonMagique";
export default {
  name: "ProduitsView",
  components: { BoutonMagique },
  data() {
    return {
      nom: "Willemin",
      prenom: "Xavier",
      mot: "Bonjour",
    };
  },
  // Création d'une méthode MotAurevoir qui affiche une pop-up quand elle est appelée'
  methods: {
    MotAurevoir() {
      alert("Ce fut un plaisir " + this.prenom + " !");
    },
  },
};
</script>

<style lang="sass" scoped>
h1
  color: green
</style>
