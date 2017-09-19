<template>
  <v-app id="navbar" dark toolbar>
    <v-navigation-drawer
      :mini-variant.sync="mini"
      v-model="drawer"
      enable-resize-watcher
      persistent
      clipped
      floating
    >
      <v-card class="ma-3 mt-5 " light>
        <v-list dense class="py-0">
          <v-list-tile class="red darken-4" dark v-for="item in items" :key="item.title" @click="">
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-card>
    </v-navigation-drawer>
    <v-toolbar class="red darken-4" dark>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>{{title}}</v-toolbar-title>
    </v-toolbar>
    <main>
      <v-container fluid>
        <!--v-router-->
      </v-container>
    </main>
  </v-app>
</template>

<script>
  export default {
    name: 'navbar',
    data() {
      return {
        drawer: true,
        items: [
          {
            title: 'Resistor Characteristics',
            icon: 'flash on',
          },
        ],
        title: 'WebSim',
      };
    },
  };
</script>

<style scoped>
</style>
