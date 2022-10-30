<template>
  <div class="my-3 py-3">
    <v-container>
      <v-layout row wrap justify-start>
        <v-flex xs12 pa-2>
          <p class="display-2 py-3 b1 text-center">
            {{ $t("notToMissServices") }}
          </p>
          <p class="body-1 text-center">{{ $t("serviceDesc") }}</p>
        </v-flex>
        <v-flex xs12 md12 md4 lg4 pa-2 v-for="item in items" :key="item.title">
          <v-card flat height="100%">
            <v-img
              lazy-src="https://picsum.photos/id/11/10/6"
              contain
              height="100%"
              width="100%"
              max-height="200px"
              :src="item.img"
              :alt="item.title"
            >
              <template v-slot:placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
            <v-card-text>
              <p class="display-1 b1">
                {{ item.title }}
              </p>
              <p class="body-1 text-justify">
                {{ item.desc }}
                <router-link :to="item.route" class="ndec">
                  Read More</router-link
                >
              </p>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>

    <v-container>
      <v-layout row wrap justify-center align-center my-3 py-3>
        <v-flex xs12 pa-2>
          <p class="display-1 b1">{{ $t("thirdPartyInt") }}</p>
          <p class="body-1">
            {{ $t("thirdPartyIntDesc") }}
          </p>
        </v-flex>
        <v-flex
          xs12
          sm12
          md3
          lg3
          pa-2
          v-for="item in integrations"
          :key="item.title"
        >
          <v-card height="100%" flat>
            <v-card-text>
              <v-layout row wrap justify-center align-center>
                <v-flex xs3 pa-2>
                  <div style="height: 40px; width: 40px; margin: auto">
                    <img
                      :src="item.img"
                      :alt="item.title"
                      height="100%"
                      width="100%"
                    />
                  </div>
                </v-flex>
                <v-flex xs9 pa-2>
                  <h1 class="body-1 b1">{{ item.title }}</h1>
                  <p class="body-2">{{ item.desc }}</p>
                </v-flex>
              </v-layout>
            </v-card-text>
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
      integrations: [
        {
          title: this.$t("googleAds"),
          route: "google-ads",
          desc: this.$t("googleAdsDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqPeQkTwonFMJEOvRJQovTPNXwF4TiEbnFbqquD6k4FtLetXrR5xAhtOdb0xXHJTtBmb0&usqp=CAU",
        },
        {
          title: this.$t("googleBiz"),
          route: "gmb",
          desc: this.$t("googleBizDesc"),
          img: "https://www.cityplacesurgery.com/wp-content/uploads/2019/10/google-my-business-icon.png",
        },
        {
          title: this.$t("googleCal"),
          route: "g-cal",
          desc: this.$t("googleCalDesc"),
          img: "https://i.pinimg.com/originals/6e/09/90/6e099088b3deb805b68d83676af6f067.png",
        },
        {
          title: this.$t("googleDrive"),
          route: "g-drive",
          desc: this.$t("googleDriveDesc"),
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/1/12/Google_Drive_icon_%282020%29.svg/2295px-Google_Drive_icon_%282020%29.svg.png",
        },
        {
          title: this.$t("googleContact"),
          route: "g-contact",
          desc: this.$t("googleContactDesc"),
          img: "https://icons.iconarchive.com/icons/dtafalonso/android-lollipop/512/Contacts-icon.png",
        },
        {
          title: this.$t("googleAnalytics"),
          route: "g-analytics",
          desc: this.$t("googleAnalyticsDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSBeYSZxnu-iLTqA4qXvgyo54w2-ex9_uz7BpOujIKHTvFcvTbZcR3Ok7L1a9WFdcDfHGc&usqp=CAU",
        },
        {
          title: this.$t("mailChimp"),
          route: "mail-chimp",
          desc: this.$t("mailChimpDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxsDtnwF2e1XgOe_yGQuN5jNAkCabeg_x39TMCf1RO8ASzBZGSv15rxDijDsIBYxeN760&usqp=CAU",
        },
        {
          title: this.$t("salesforce"),
          route: "salesforce",
          desc: this.$t("salesforceDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1iVYUTXl21mWpdI6CFk6yfjZlNGorUYdtz5-03kOTa7JauwI-TwhdLOEDogr1sW5lMmg&usqp=CAU",
        },
        {
          title: this.$t("fbAds"),
          route: "fb-ads",
          desc: this.$t("fbAdsDesc"),
          img: "https://icon-library.com/images/1-512_22089.png",
        },
        {
          title: this.$t("instagram"),
          route: "instagram",
          desc: this.$t("instagramDesc"),
          img: "https://i.pinimg.com/736x/5e/ff/6c/5eff6c25d920f6a78fda288e6589bf8b.jpg",
        },
        {
          title: this.$t("whatsapp"),
          route: "whatsapp",
          desc: this.$t("whatsappDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSSv4vSJK5HR8co51Om7c1z-1NNVXFqE9O4w6Q1tGLOb9DjOAr-9RTfp9Pe2SVaaTUluog&usqp=CAU",
        },
        {
          title: this.$t("twilio"),
          route: "twilio",
          desc: this.$t("twilioDesc"),
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSc_qbbESmCKefPbTTb7HYgWK_QXiSS862IiHAcSUEFnIWTCpWrsmIJPIaTYnNp3Fe15Xs&usqp=CAU",
        },
      ],
      items: [
        {
          img: require("../../static/images/report.jpg"),
          title: this.$t("appWebsite"),
          route: "about",
          desc: this.$t("appWebsiteDesc"),
        },
        {
          img: require("../../static/images/call-center.jpg"),
          title: this.$t("simpleHosting"),
          route: "about",
          desc: this.$t("simpleHostingDesc"),
        },
        {
          img: require("../../static/images/emailm.png"),
          title: this.$t("simpleAdvert"),
          route: "about",
          desc: this.$t("simpleAdvertDesc"),
        },
      ],
      crms: [
        {
          img: "https://www.salesforce.com/content/dam/web/en_us/www/images/home/php-rc-card-2.png",
          title: "REPORT",
          subtitle: "State of Sales Report",
          desc: `Research shows nearly 6,000 sales pros are selling in a global crisis.`,
        },
        {
          img: "https://www.salesforce.com/content/dam/web/en_us/www/images/home/php-rc-smb-navigating-through-change.jpg",
          title: "Video",
          subtitle: "Navigate through Change",
          desc: "Small businesses evolve to meet customer needs.",
        },
        {
          img: "https://www.salesforce.com/content/dam/web/en_us/www/images/home/php-rc-card-4.png",
          title: "Webinar",
          subtitle: "Lead Management",
          desc: "Get expert advice on lead management.",
        },
      ],
    };
  },
};
</script>
