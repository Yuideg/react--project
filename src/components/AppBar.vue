 <template>
  <nav>
    <v-app-bar flat app>
    <v-app-bar-nav-icon app  @click="drawer = !drawer">
    </v-app-bar-nav-icon>
    <v-spacer></v-spacer>
    <v-btn flat text class="menubar grey--text">
      Home
    </v-btn>
    <v-btn flat text class="menubar grey--text" >
      Contact
    </v-btn>
    <v-btn flat text class="menubar grey--text">
      Movie
    </v-btn>
    <v-btn flat text class="menubar grey--text">
      Help
    </v-btn>
    <v-btn icon flat text class="menubar grey--text">
      <v-icon>mdi-heart</v-icon>
    </v-btn>
    <v-btn icon flat text class="menubar grey--text">
      <v-icon>mdi-dots-vertical</v-icon>
    </v-btn>
    </v-app-bar>
    <v-navigation-drawer app  v-model="drawer" class="wheat white--text">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Cinema
          </v-list-item-title>
          <v-list-item-subtitle>
            cinema app
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>
<script>
export default {
  name: 'AppBar',
  data() {
    return {
      drawer: false,
      items: [
        { title: 'Admin', icon: 'mdi-view-dashboard' },
        { title: 'Photos', icon: 'mdi-image' },
        { title: 'Contact', icon: 'mdi-phone' },
        { title: 'About', icon: 'mdi-help-box' },
      ],
      right: null,
    };
  },
};
</script>
<style scoped>
.menubar {
  color: white;
  padding: 10px;
  margin: 10px;
}
</style>
