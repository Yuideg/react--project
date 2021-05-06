<template>
  <v-bottom-navigation
    class="botton-nav"
    horizontal
    color="black"
  >
    <v-btn class='menubar'>
      <span>Recents</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>Favorites</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Nearby</span>

      <v-icon>mdi-map-marker </v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>
<script>
export default {
  name: 'BottomBar',
};
</script>
<style scoped>
.botton-nav{
  color: white;
  background-color: black;
}

</style>
