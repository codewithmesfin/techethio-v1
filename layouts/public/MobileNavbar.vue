<template>
  <div>
    <v-app-bar
      flat
      class="d-block d-md-none"
      app
      clipped-left
      clipped-right
      fixed
      style="border-bottom: 1px solid #e6e6e6; background-color: white"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <!-- <v-avatar class="mr-1" size="40">
        <img src="/images/logo.png" alt="logo" />
      </v-avatar> -->

      <v-text-field
        append-icon="mdi-magnify"
        solo
        rounded
        flat
        dense
        hide-details
        :label="$t('search')"
        background-color="#edf2f7"
      />
      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn text v-bind="attrs" v-on="on">
            <v-icon>mdi-translate</v-icon>
            <v-icon small>mdi-chevron-down</v-icon>
          </v-btn>
        </template>
        <v-list dense>
          <template v-for="(locale, i) in $i18n.locales">
            <v-list-item :key="i" :to="switchLocalePath(locale.code)">
              <v-list-item-title> {{ locale.name }}</v-list-item-title>
            </v-list-item>
          </template>
        </v-list>
      </v-menu>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <v-toolbar
        flat
        dense
        style="border-bottom: 2px solid #f6f7f9; background-color: white"
      >
        <!-- <img src="/images/logo.png" alt="logo" height="35px" class="mr-1" /> -->
        <v-toolbar-title class="primary--text title">TechEthio</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon @click="drawer = !drawer">
          <v-icon>mdi-close-circle</v-icon>
        </v-btn>
      </v-toolbar>

      <v-list dense>
        <template v-for="menu in menus">
          <v-list-item
            v-if="!menu.children"
            :key="menu.title"
            to=""
            @click.native="$router.push(`${menu.route}`)"
          >
            <v-list-item-title
              >{{ $t(menu.title) }}
            </v-list-item-title></v-list-item
          >
        </template>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      drawer: false,
      menus: [
        { title: "home", route: "home" },
        { title: "about", route: "about" },
        { title: "service", route: "service" },
        { title: "portfolio", route: "portfolio" },
        { title: "career", route: "career" },
        { title: "contactUs", route: "contact" },
      ],
    };
  },
};
</script>
