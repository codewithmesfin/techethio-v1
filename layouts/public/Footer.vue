
<template>
  <v-card tile class="primary">
    <v-container fluid>
      <v-layout wrap row justify-center pa-2>
        <v-flex xs12 md10 pa-2>
          <v-layout row wrap justify-space-around class="my-5">
            <v-flex md3 pa-2>
              <h4 class="white--text title">TechEthio</h4>
              <a class="link white--text pr-3" href="mailto:contact@etyop.com">
                <v-icon small color="white">mdi-email</v-icon>
                contact@etyop.com </a
              ><br />
              <a class="link white--text pr-3" href="tel:+251 91 143 0924">
                <v-icon small color="white">mdi-phone</v-icon>
                +251 91 143 0924
              </a>
            </v-flex>
            <v-flex md3 pa-2>
              <h4 class="white--text title">Quick Links</h4>
              <template
                v-for="companyLinkItem in companyLinkItems"
                class="text-center"
              >
                <router-link
                  :key="companyLinkItem.title"
                  class="link white--text pr-3"
                  :to="`/${companyLinkItem.route}`"
                >
                  {{ companyLinkItem.title }}</router-link
                >
              </template>
            </v-flex>

            <v-flex md3 pa-2>
              <h4 class="white--text title">Social</h4>
              <template
                v-for="socialLinkItem in socialLinkItems"
                class="text-center"
              >
                <router-link
                  :key="socialLinkItem.title"
                  class="link white--text pr-3"
                  :to="`/${socialLinkItem.route}`"
                >
                  {{ socialLinkItem.title }}</router-link
                >
              </template>
            </v-flex>

            <v-flex md3 pa-2>
              <h4 class="title white--text">Misc</h4>
              <template
                v-for="miscLinkItem in miscLinkItems"
                class="text-center"
              >
                <router-link
                  :key="miscLinkItem.title"
                  class="link white--text pr-3"
                  :to="`/${miscLinkItem.route}`"
                >
                  {{ miscLinkItem.title }}</router-link
                >
              </template>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
    <v-divider color="white" />
    <div class="pt-3 mt-3">
      <p class="text-center body-1 white--text">
        All rights reserved! {{ new Date().getFullYear() }} —
        <router-link class="link white--text" to="https://techethio.com"
          >techethio.com</router-link
        >
      </p>
    </div>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    companyLinkItems: [
      { title: "About us", route: "about" },
      { title: "Services", route: "service" },
      { title: "Careers", route: "career" },
      { title: "Contact us", route: "contact" },
    ],

    socialLinkItems: [
      { title: "Facebook", route: "home" },
      { title: "Linkedin", route: "home" },
      { title: "Twitter", route: "home" },
    ],

    miscLinkItems: [
      { title: "Privacy Policy", route: "home" },
      { title: "Terms and Conditions", route: "home" },
    ],
  }),
};
</script>

<style lang="css" scoped>
.social.underline.after.first {
  text-decoration: none;
  position: relative;
}
</style>
