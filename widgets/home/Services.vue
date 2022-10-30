<template>
  <div>
    <section>
      <v-container>
        <v-layout row wrap justify-center pt-3 mt-3>
          <v-flex xs12 sm12 md8 lg8 pa-2>
            <p class="display-1 b1 text-center py-3 my-3">
              {{ $t("whatisNew") }}
            </p>
          </v-flex>
          <v-flex xs12></v-flex>
          <v-flex xs12 ms12 md4 lg4 pa-2 v-for="col in items" :key="col.title">
            <v-card style="cursor: pointer" height="100%" width="100%" flat>
              <v-card-text>
                <v-layout row wrap justify-start align-center>
                  <v-flex xs4 pa-2>
                    <v-img
                      lazy-src="https://picsum.photos/id/11/10/6"
                      :src="col.img"
                      height="100%"
                      width="100%"
                      min-height="90px"
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
                  </v-flex>
                  <v-flex xs8 pa-2>
                    <div class="subtitle-1 b">{{ col.title }}</div>
                    <p class="body-1 b1">{{ col.desc }}</p>
                  </v-flex>
                </v-layout>
              </v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>

    <v-container fluid>
      <div class="d-none d-md-block" style="height: 50px"></div>
      <div class="d-block d-md-none" style="height: 20px"></div>
      <v-layout row wrap justify-center>
        <v-flex xs12 sm12 md8 lg8 pa-2>
          <p class="display-1 b1 text-center">
            {{ $t("learnWhatHelp") }}
          </p>
          <p class="body-1 text-center">
            {{ $t("learnWhatHelpDesc") }}
          </p>
        </v-flex>
        <v-flex xs12></v-flex>
        <v-flex xs12 ms12 md2 lg2 pa-2 v-for="(col, i) in services" :key="i">
          <v-card
            elevation="5"
            class="contentCard white"
            height="100%"
            min-height="210px"
            width="100%"
          >
            <v-container fill-height fluid>
              <v-row align="center" justify="center">
                <v-col>
                  <v-layout column align-center justify-center>
                    <v-avatar style="background: #f0f2f5" size="100">
                      <v-img
                        lazy-src="https://picsum.photos/id/11/10/6"
                        contain
                        :src="col.img"
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
                    </v-avatar>
                    <v-card-text class="text-center subtitle-1">
                      <strong> {{ col.title }}</strong>
                      <p class="body-1">{{ col.subtitle }}</p>
                    </v-card-text>
                  </v-layout>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          title: this.$t("erpSystem"),
          subtitle: this.$t("erpDef"),
          route: "erp",
          img: "https://www.computerhope.com/jargon/e/erp.jpg",
        },
        {
          title: this.$t("crmPlatforms"),
          subtitle: this.$t("crmDef"),
          route: "crm",
          img: "https://www.computerhope.com/jargon/c/crm.jpg",
        },
        {
          title: this.$t("eLearning"),
          subtitle: this.$t("lmsDef"),
          route: "lms",
          img: "https://skillsacademy.tech/wp-content/uploads/2021/10/hero-lms-plug-and-play.png",
        },
        {
          title: this.$t("digitalMarketing"),
          subtitle: this.$t("dmDesc"),
          route: "digital-marketing",
          img: "https://www.smartinsights.com/wp-content/uploads/2011/05/RACE-planning-digital-marketing-plan-system-550x764.png",
        },
        {
          title: this.$t("consultancy"),
          subtitle: this.$t("consultancyDesc"),
          route: "consulatancy",
          img: "https://www.itoutcomes.com/wp-content/uploads/2016/10/IT-consultancy.jpg",
        },
      ],
      items: [
        {
          img: "https://www.salesforce.com/content/dam/blogs/ca/Blog%20Posts/market-your-firm-og.jpg",
          title: this.$t("caseStudies"),
          route: "case-study",
          desc: this.$t("tellUs"),
        },
        {
          img: "https://blog.trello.com/hs-fs/Illo_X_Characteristics_of_Problem_Solving__Solution_Oriented_Leaders.png",
          title: this.$t("solutions"),
          route: "solution",
          desc: this.$t("trySolution"),
        },
        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTUMkH_72l40CitoxAU3rZ2SphkKidaJ_ZhiS_dOO4DF1Zq44ti6TR9Qh9irCXFMi95y9A&usqp=CAU",
          title: this.$t("success"),
          route: "success",
          desc: this.$t("enjoyYourBusiness"),
        },
      ],
    };
  },
  created() {},
  methods: {},
};
</script>
<style lang="css" scoped>
.contentCard {
  cursor: pointer;
}
.contentCard:hover {
  background: #f0f2f5 !important;
}
</style>
