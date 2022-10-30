<template>
  <div>
    <div style="height: 100px"></div>
    <section>
      <v-container fluid>
        <v-layout row wrap justify-center pa-2>
          <v-flex xs11 md10 pa-2>
            <div>
              <v-layout justify-center wrap row pa-1>
                <v-flex xs12 md6 pa-2>
                  <h1 class="display-3 b text-center py-3 primary--text">
                    {{ title }}
                  </h1>
                  <p class="body-1 text-center">
                    We are working hard to make your life easier! The following
                    are a few areas among what we are focusing to innovate the
                    right solution!
                  </p>
                </v-flex>
                <v-flex xs12></v-flex>
                <v-flex
                  xs12
                  sm12
                  md4
                  lg4
                  pa-2
                  v-for="(item, i) in items"
                  :key="i"
                >
                  <v-card height="100%" flat>
                    <v-card-text>
                      <v-img
                        lazy-src="https://picsum.photos/id/11/10/6"
                        height="100%"
                        width="100%"
                        max-height="200px"
                        :src="item.img"
                        alt="biz"
                        contain
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
                      <div class="display-1 b pt-3 text-center primary--text">
                        {{ item.title }}
                      </div>
                      <p class="title text-center primary--text">
                        {{ item.subtitle }}
                      </p>
                      <p class="body-1 text-center">
                        {{ item.desc }}
                        <router-link class="link" to> Read more</router-link>
                      </p>
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </div>
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
      title: "Our Services",
      items: [
        {
          title: "ERP",
          subtitle: "Enterprise resource planing",
          desc: `Enterprise resource planning (ERP) refers to a type of software that organizations use to manage day-to-day business activities such as accounting, procurement, project management, risk management and compliance, and supply chain operations`,
          img: `https://magenest.com/wp-content/uploads/2021/07/erp-software-1.jpg`,
          route: "erp",
        },
        {
          title: "CRM",
          subtitle: "Customer relation management",
          desc: `
CRM stands for “Customer Relationship Management” and is a software system that helps business owners easily track all communications and nurture relationships with their leads and clients . A CRM replaces the multitude of spreadsheets, databases and apps that many businesses patch together to track client data.`,
          img: "https://www.computerhope.com/jargon/c/crm.jpg",
        },
        {
          title: "LMS",
          subtitle: "Learning management System",
          desc: `LMS means learning management system . A learning management system is a digital learning environment that manages all aspects of a company's various training efforts. It also manages user information for personalized delivery including their user profile, job functions and preferences.`,
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-qmT_7eOfjvOnu_rInnznzaP2u6JYcRtDcuX6x_pbeCgMLH-1UMwHKtS5BV0DRuRF1ns&usqp=CAU",
        },
        {
          title: "Hosting",
          subtitle: "Website hosting services",
          desc: `
Web hosting is the place where all the files of your website live . It is like the home of your website where it actually lives. A good way to think about this is if the domain name was the address of your house, then web hosting is the actual house that address points to. All websites on the internet, need web hosting.`,
          img: "https://previews.123rf.com/images/doomu/doomu1310/doomu131000087/23302658-conecte-al-concepto-world-wide-web-los-ordenadores-port%C3%A1tiles-con-el-globo-terrestre-sobre-un-fondo-.jpg",
        },
        {
          title: "Digital marketing",
          desc: `Digital marketing, also called online marketing, is the promotion of brands to connect with potential customers using the internet and other forms of digital communication . This includes not only email, social media, and web-based advertising, but also text and multimedia messages as a marketing channel.`,
          img: "https://misd.in/wp-content/uploads/2020/04/digital-marketing-course.png",
        },
        {
          title: "Consultancy",
          desc: `
Consulting Services means the provision of expertise or strategic advice that is presented for consideration and decision-making . A Non-consulting Service Provider is an individual or a company who contracts to provide services, other than consulting services to another individual or business.`,
          img: "https://www.itoutcomes.com/wp-content/uploads/2016/10/IT-consultancy.jpg",
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
          content: "Learn more about TechEthio services ",
        },
      ],
    };
  },
};
</script>


<style>
.link {
  text-decoration: none !important;
}
</style>