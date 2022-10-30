<template>
  <div>
    <div style="height: 100px"></div>
    <v-container fluid>
      <v-layout row wrap justify-center>
        <v-flex xs12 sm12 md5 lg5 pa-2>
          <div>
            <v-img
              lazy-src="https://picsum.photos/id/11/10/6"
              contain
              height="100%"
              width="100%"
              max-height="500px"
              src="https://www.techjaadu.com/images/contact-us.png"
              alt="biz"
            >
              <template v-slot:placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row> </template
            ></v-img>
          </div>
          <p class="display-2 b pt-3 mt-3 text-center primary--text">
            Contact us !
          </p>
          <p class="body-1 text-center">Reach us by placing your messages.</p>
        </v-flex>
        <v-flex xs12 sm12 md5 pa-2>
          <iframe
            src="https://docs.google.com/forms/d/e/1FAIpQLSdJoUHsEuWVShuIbKuNLdj6awOGgUk-9deIIfc5dHogJ9hd4w/viewform?embedded=true"
            width="100%"
            height="100%"
            frameborder="0"
            marginheight="0"
            marginwidth="0"
            style="min-height: 100vh"
            @loadstart="console.log('loading')"
            >Loading…</iframe
          >
        </v-flex>
      </v-layout>
    </v-container>
    <section>
      <iframe
        width="100%"
        height="700px"
        id="gmap_canvas"
        src="https://maps.google.com/maps?q=2880%20Broadway,%20New%20York&t=&z=13&ie=UTF8&iwloc=&output=embed"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
      ></iframe>
    </section>
  </div>
</template>

<script>
export default {
  layout: "career",
  data() {
    return {
      title: "Contact us",
    };
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Reach TechEthio by placing your messages",
        },
      ],
    };
  },
};
</script>