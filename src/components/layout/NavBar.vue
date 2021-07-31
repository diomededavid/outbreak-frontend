<template>
    <v-navigation-drawer app v-model="drawer">
        <v-list-item>
        <v-list-item-content>
            <v-list-item-title class="text-h6">
            The Covid Online Board Game
            </v-list-item-title>
            <v-list-item-subtitle>
            subtext
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
            :to="item.to"
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
</template>

<script>
  export default {
    name: 'NavBar',
    props: {
        drawer: Boolean
    },
    data () {
      return {
        items: [
          { title: 'Game', icon: 'mdi-virus', to: '/game' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        right: null,
      }
    },
  }
</script>
