<template>
  <div>
    <div style="height: 100px"></div>
    <v-container fluid>
      <v-layout row wrap justify-center align-center pa-2>
        <v-flex xs12 sm12 md4 lg4 pa-2>
          <div>
            <v-img
              lazy-src="https://picsum.photos/id/11/10/6"
              contain
              height="100%"
              width="100%"
              max-height="500px"
              src="https://thumbs.dreamstime.com/b/career-opportunities-job-fair-re-hiring-recruitment-ads-human-resources-open-vacancy-job-seekers-come-applying-jobs-165707996.jpg"
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
            We are hiring !
          </p>
          <p class="body-1 text-center">
            TechEthio is hiring Software Engineers and Digital Marketing
            Experts. We are looking for a project manager experinced in Scrum
            and Agile Software Development Life Cycl; Software Developers in
            experinced in Vue js and Nuxt js, React and Next js, Flutter and
            Dart, Node js, PHP and Laravel, MySQL, MongoDB, Firebase, AWS;
            Certified Digital Marketing Experts experinced in Digital Marketing
            strategies, Marketing tools, and Customer Relation Management(CRM).
          </p>
        </v-flex>
        <v-flex xs12 sm12 md5 pa-2>
          <iframe
            src="https://docs.google.com/forms/d/e/1FAIpQLSdTRaWQQZv16XdT4T21E2A58gyLl84my7PQB_-jANPz0dP62Q/viewform?embedded=true"
            width="100%"
            height="100%"
            frameborder="0"
            marginheight="0"
            marginwidth="0"
            style="min-height: 100vh"
            >Loading…</iframe
          >
        </v-flex>
      </v-layout>
    </v-container>
    <div style="height: 100px"></div>
  </div>
</template>


<script>
export default {
  layout: "career",
  data() {
    return {
      title: "Job Opportunities",
    };
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Browse jobs and vacancies at TechEthio",
        },
      ],
    };
  },
};
</script>
