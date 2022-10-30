<template>
  <div>
    <section>
      <div style="height: 60px"></div>
      <v-container fluid>
        <v-layout row wrap justify-center align-center ma-3>
          <v-flex xs12 sm12 md5 lg5 pa-1>
            <v-card height="100%" flat>
              <v-card-text>
                <p class="display-3 b primary--text">{{ title }}</p>
                <p class="title primary--text">
                  We are working hard to solves problems in Africa
                </p>
                <p class="body-1">
                  We are a team of experienced professionals. We are growing.
                  After several years of experienced in some of the high
                  techlogies we recognized that our technical skills,
                  experiences , and our African values ca be put togather to
                  create technologies that will transform lives in Africa.
                </p>
                <p class="body-1">
                  We believe that people are the secret to success. By
                  empowering them, we create value for our customers and
                  positively impact the world.
                </p>
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm12 md5 lg5 pa-2>
            <v-card height="100%" flat tile>
              <v-img
                lazy-src="https://picsum.photos/id/11/10/6"
                contain
                height="100%"
                width="100%"
                src="https://892728.smushcdn.com/1309077/wp-content/uploads/2021/01/it-security.png?lossy=1&strip=1&webp=0"
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
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
    <section>
      <div style="height: 100px"></div>
      <v-container fluid>
        <v-layout row wrap justify-center py-3>
          <v-flex xs12 sm12 md3 lg3 pa-2 v-for="(item, i) in items" :key="i">
            <p class="display-3 b text-center primary--text">
              {{ item.title }}
            </p>
            <p class="title text-center">{{ item.subtitle }}</p>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
    <section>
      <div style="height: 100px"></div>
      <v-container fluid>
        <v-layout row wrap justify-center>
          <v-flex xs12 md9 px-2>
            <v-layout row wrap justify-center>
              <v-flex xs11 px-2>
                <p class="display-2 b">Core values</p>
              </v-flex>
              <v-flex
                xs12
                sm12
                md4
                lg4
                px-2
                v-for="(item, i) in goals"
                :key="i"
              >
                <v-card height="100%" flat>
                  <v-img
                    lazy-src="https://picsum.photos/id/11/10/6"
                    :src="item.img"
                    height="100%"
                    width="100%"
                    min-height="100px"
                    max-height="200px"
                    aspect-ratio="1.7"
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
                    <div class="display-1 pt-3 b primary--text">
                      {{ item.title }}
                    </div>
                    <div class="body-1">{{ item.desc }}</div>
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
    <div style="height: 100px"></div>
  </div>
</template>




<script>
export default {
  layout: "service",
  data() {
    return {
      title: "Who we are ?",
      items: [
        { title: "200+", subtitle: "Apps and websites developed" },
        { title: "30+", subtitle: "Professionals globally" },
        { title: "5", subtitle: "Global Partners" },
      ],
      goals: [
        {
          title: "Innovations",
          desc: "We are here to invent a better solution to help you grow your business.",
          img: "https://sloanreview.mit.edu/wp-content/uploads/2021/04/GEN-Tippman-Connection-Remote-Innovation-2400x1260-1-1200x630.jpg",
        },
        {
          title: "Customer Value",
          desc: "We are working hard to make our customers happy. Customers are our valuable assets.",
          img: "https://cdni.iconscout.com/illustration/premium/thumb/global-communication-network-3611248-3126417.png",
        },
        {
          title: "Trust",
          desc: `Our team is looking to serve your long-term business goals. Unlike other consulting services, we maintain high retention rates, so that you’ll continue to work with engineers you trust for your business.`,
          img: "https://carpenterconsulting.pl/wp-content/uploads/2020/10/culture-pf-trust.jpg",
        },
      ],
    };
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Learn more about TechEthio",
        },
      ],
    };
  },
};
</script>