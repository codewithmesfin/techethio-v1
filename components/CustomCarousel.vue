<template>
  <v-carousel
    cycle
    height="100%"
    hide-delimiter-background
    hide-delimiter
    show-arrows-on-hover
    delimiter-icon="mdi-minus"
  >
    <v-carousel-item>
      <v-card flat tile light>
        <v-card-text>
          <v-layout row wrap justify-center align-center>
            <v-flex xs12 sm12 md4 lg4 pa-2>
              <h1 class="display-1 primary--text b">
                <v-icon color="orange" x-large>mdi-format-quote-open</v-icon
                ><br />
                {{ $t("intro1") }}
                <p class="text-right">
                  <v-icon x-large color="orange">mdi-format-quote-close</v-icon>
                </p>
              </h1>
            </v-flex>
            <v-flex xs12 sm12 md6 lg6 pa-2>
              <v-img
                lazy-src="https://picsum.photos/id/11/10/6"
                contain
                height="100%"
                width="100%"
                max-height="400px"
                src="https://i.pinimg.com/736x/a7/ce/3c/a7ce3cc7c795e5e6a82cb8a6a93e35b5.jpg"
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
    </v-carousel-item>
    <v-carousel-item>
      <v-card flat tile light>
        <v-card-text>
          <v-layout row wrap justify-center align-center>
            <v-flex xs12 sm12 md6 lg6 pa-2>
              <v-img
                lazy-src="https://picsum.photos/id/11/10/6"
                contain
                height="100%"
                width="100%"
                max-height="400px"
                src="https://www.workforcehub.com/wp-content/uploads/2019/04/swipeclock-HR-techniques-improve-communication.jpg"
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
            <v-flex xs12 sm12 md4 lg4 pa-2>
              <h1 class="title b">
                {{ $t("intro2") }}
              </h1>
            </v-flex>
          </v-layout>
        </v-card-text>
      </v-card>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>