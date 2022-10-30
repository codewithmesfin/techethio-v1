<template>
  <v-container fluid>
    <div class="my-5 py-5">
      <h1 class="display-2 text-center b">Our Works</h1>
      <p class="body-1 text-center">
        At TechEthio we are creating solutions for different industries.
      </p>
      <v-layout row wrap justify-center pa-2>
        <v-flex xs12 sm6 md3 lg3 pa-2>
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card class="mx-auto" max-width="344" height="100%">
                <v-img
                  height="100%"
                  width="100%"
                  max-height="700px"
                  alt="etyop"
                  src="/images/etyop.PNG"
                  lazy-src="https://picsum.photos/id/11/10/6"
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
                    </v-row>
                  </template>
                </v-img>

                <v-card-text>
                  <h2 class="text-h6 primary--text">Etyop Mobile App</h2>
                  A beautifully designed Marketplace and Joblisting IOS and
                  Android mobile app.
                </v-card-text>

                <v-fade-transition>
                  <v-overlay v-if="hover" absolute color="#036358">
                    <v-btn href="https://etyop.com" target="_blank"
                      >Downoload the app</v-btn
                    >
                  </v-overlay>
                </v-fade-transition>
              </v-card>
            </template>
          </v-hover>
        </v-flex>
        <v-flex xs12 sm6 md3 lg3 pa-2>
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card class="mx-auto" max-width="344" height="100%">
                <v-img
                  height="100%"
                  width="100%"
                  max-height="700px"
                  alt="etyop"
                  src="/images/sharegebeya.PNG"
                  lazy-src="https://picsum.photos/id/11/10/6"
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
                    </v-row>
                  </template>
                </v-img>

                <v-card-text>
                  <h2 class="text-h6 primary--text">Share Gebeya Mobile App</h2>
                  A beautifully designed IOS and Android app for listing Banks,
                  Insurances, and other companies shares.
                </v-card-text>

                <v-fade-transition>
                  <v-overlay v-if="hover" absolute color="#036358">
                    <v-btn href="https://etyop.com" target="_blank"
                      >Downoload the app</v-btn
                    >
                  </v-overlay>
                </v-fade-transition>
              </v-card>
            </template>
          </v-hover>
        </v-flex>
      </v-layout>
    </div>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    overlay: false,
  }),
};
</script>