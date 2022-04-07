<template>
  <v-app dark>
    <Nav></Nav>
    <!-- <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      app
    >
      <v-toolbar-title v-text="title" />
    </v-app-bar> -->
    <v-main>
      <v-container fluid class="appStyling px-0">
        <Nuxt/>
      </v-container>
    </v-main>
    <v-footer
      app
    >
      <span>&copy; WUULF {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      drawer: true,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Calendar',
          to: '/calendar'
        }
      ],
      title: 'The Unitarian Universalist Life Festival'
    }
  }
}
</script>

<style lang="scss" scoped>
.appStyling {
  background: linear-gradient(to bottom, #111111, #a31b0c, #b98412)
}
</style>