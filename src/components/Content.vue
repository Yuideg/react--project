/* eslint-disable vue/valid-v-bind */
/* eslint-disable max-len */
<template >
  <v-card class="mx-auto my-18" height="auto" max-width="900"  width="900" :elevation="29" >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>
      <ImageList/>
  </v-card>
</template>
<script>
import ImageList from './ImageList.vue';

export default {
  name: 'Content',
  components: {
    ImageList,
  },
};
</script>
