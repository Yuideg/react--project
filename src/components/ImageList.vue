  // eslint-disable-next-line vue/valid-template-root
<template>
<v-card width="300" max-width="300">
  <v-container class= "image_repeat" v-for = "image in Photo" :key="image">
    <v-container v-for="i in 2" :key="i">
      <v-img class="image" max-height="300" max-width="300" :src="image">
      </v-img>
    <v-card-title>Gast Cinema</v-card-title>
    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          v-model="startValue"
          color="amber"
          dense
          half-increments
          size="14"
        ></v-rating>
        <div class="grey--text ml-4">
          {{ startValue }} ({{ 413 }} reviewers)
        </div>
      </v-row>

      <div class="my-4 subtitle-1">
        $ 40
      </div>
      <div>
        Small plates, salads & sandwiches - an intimate setting with 12 indoor
        seats plus patio seating.
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Tonight's availability</v-card-title>

    <v-card-text>
      <v-chip-group active-class="deep-purple accent-4 white--text" column>
        <v-chip>5:30PM</v-chip>

        <v-chip>7:30PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>9:00PM</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <button color="purple" text>
        watch
      </button>
    </v-card-actions>
  </v-container>
  </v-container>
  </v-card>
</template>
<script>
export default {
  name: 'ImageList',
  data() {
    return {
      Photo: {
        image1:
          'https://etmdb.com/static/images/CACHE/images/movie/Addisu-Sew/e7f2324b84a41d1574ceb5a98948c339.png',
        image2: 'https://i.ytimg.com/vi/XK_my27eTGM/maxresdefault.jpg',
        image3: 'https://i.ytimg.com/vi/uxFK3XseYqA/maxresdefault.jpg',
        image4:
          'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_si1CuyhluHHRtdFC7lSqXBEr0JcqinMtZA&usqp=CAU',
        image5:
          'https://i.pinimg.com/564x/45/3d/d6/453dd61e03dcd7957397a9e13024c564.jpg',
        image6: 'https://i.ytimg.com/vi/gYUqRGQGLvY/maxresdefault.jpg',
      },
      startValue: 3.5,
      imagevalue: '',
    };
  },
  methods: {},
  components: {},
  computed: {},
  props: {},
};
</script>
<style scoped>
.image_repeat {
  width: 100%;
  margin: 20px auto;
  border: 1px solid grey;
  text-transform: lowercase;
  color: black;
}
.image {
  margin-left: 130px;
}
</style>
