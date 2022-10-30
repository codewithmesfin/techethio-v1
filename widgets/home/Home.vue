<template>
  <div>
    <section>
      <v-card tile flat light>
        <custom-carousel />
      </v-card>
    </section>
    <section>
      <v-card tile flat color="primary" dark>
        <v-card-text>
          <v-layout row wrap justify-end align-center>
            <v-flex xs12 sm12 md5 lg5 pa-2>
              <div class="text-left">
                <p class="display-1 b1 text-left white--text">
                  {{ $t("intro") }}
                </p>
                <p class="subtitle-1 px-1 black--text">
                  <router-link to="/service" class="link white--text">
                    {{ $t("seeHow") }}
                  </router-link>
                </p>
              </div>
              <v-layout row wrap justify-start px-2 pt-3>
                <v-flex xs6 sm6 md4 lg4 pa-2>
                  <v-btn
                    color="white primary--text"
                    class="text-capitalize"
                    @click="$router.push(`/contact`)"
                  >
                    <v-icon class="mr-2 d-none d-md-flex">mdi-forum</v-icon>
                    {{ $t("contactUsNow") }}
                  </v-btn>
                </v-flex>
                <v-flex xs6 sm6 md4 lg4 pa-2>
                  <v-btn
                    outlined
                    class="text-capitalize"
                    @click="$router.push(`/about`)"
                  >
                    <v-icon class="mr-2 d-none d-md-flex"
                      >mdi-information</v-icon
                    >
                    {{ $t("learnMore") }}
                  </v-btn>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-flex xs12 sm12 md6 lg6>
              <v-img
                lazy-src="https://picsum.photos/id/11/10/6"
                contain
                height="100%"
                width="100%"
                max-height="400px"
                src="https://crestechnology.com/wp-content/uploads/2020/06/infra02.png"
                alt="biz"
              >
                <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                    <v-progress-circular
                      indeterminate
                      color="grey lighten-5"
                    ></v-progress-circular>
                  </v-row> </template
              ></v-img>
            </v-flex>
          </v-layout>
        </v-card-text>
      </v-card>
    </section>
    <section>
      <services />
    </section>
    <section>
      <tech-ethio-intro />
    </section>
    <section>
      <partners />
    </section>
  </div>
</template>
<script>
import Services from "./Services.vue";
import Partners from "./Partners.vue";
import TechEthioIntro from "./TechEthioIntro.vue";
import CustomCarousel from "../../components/CustomCarousel.vue";
export default {
  components: {
    Services,
    Partners,
    TechEthioIntro,
    CustomCarousel,
  },
};
</script>
