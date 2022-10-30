<template>
  <div>
    <v-app-bar
      flat
      class="d-none d-md-block"
      app
      clipped-left
      clipped-right
      style="border-bottom: 1px solid #e6e6e6; background-color: white"
    >
      <v-spacer></v-spacer>
      <div
        class="d-flex align-center"
        style="cursor: pointer"
        @click="$router.push('/')"
      >
        <v-toolbar-title class="display-1 b">
          <span class="primaryBright--text">T</span>ech<span
            class="primaryBright--text"
            >E</span
          >thio
        </v-toolbar-title>
      </div>
      <v-spacer></v-spacer>
      <v-text-field
        prepend-inner-icon="mdi-magnify"
        solo
        rounded
        flat
        dense
        hide-details
        color="primary"
        background-color="#edf2f7"
        :label="$t('search')"
      />
      <v-spacer></v-spacer>
      <template v-for="(menu, i) in menus">
        <v-btn
          :key="i"
          text
          class="text-capitalize"
          @click="$router.push(`${menu.route}`)"
        >
          {{ $t(menu.title) }}
        </v-btn>
      </template>

      <div id="google_translate_element"></div>

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
      <v-spacer></v-spacer>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data: () => ({
    menus: [
      { title: "home", route: "home" },
      { title: "about", route: "about" },
      { title: "service", route: "service" },
      { title: "portfolio", route: "portfolio" },
      { title: "career", route: "career" },
      { title: "contactUs", route: "contact" },
    ],
  }),
};
</script>
