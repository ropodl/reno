<template>
  <v-app-bar absolute color="transparent" height="70" elevation="0">
    <v-container>
      <v-row class="d-flex align-center mt-10">
        <span class="font-weight-bold text-h4 white--text mr-2">Reno</span>
        <v-dialog v-model="dialog" width="500">
          <template v-slot:activator="{ on, attrs }">
            <v-btn icon small v-bind="attrs" v-on="on">
              <v-icon>info</v-icon>
            </v-btn>
          </template>
          <v-card>
            <v-card-title
              >The work done here is based on following link</v-card-title
            >
            <v-card-text>
              <ul>
                <li>
                  <a
                    href="https://www.behance.net/gallery/109349885/Reno-Landing-page?tracking_source=search_projects_recommended%7Cweb%20design%20website"
                    target="_blank"
                    rel="noopener noreferrer"
                    >Design Link
                  </a>
                </li>
                <li>
                  <a
                    href="https://www.behance.net/mianwaseemabbas"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                    Designer's Profile
                  </a>
                </li>
              </ul>
            </v-card-text>
            <v-card-subtitle>
              P.S.: Alteration/Modification have been done.
            </v-card-subtitle>
          </v-card>
        </v-dialog>
        <v-spacer></v-spacer>
        <ul class="navbar-items">
          <li v-for="i in nav" :key="i">
            <a href="#">{{ i.title }}</a>
          </li>
        </ul>
        <v-btn outlined class="rounded-lg" color="white">Let's Talk</v-btn>
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      nav: [
        {
          id: "1",
          title: "Home"
        },
        {
          id: "2",
          title: "Buying"
        },
        {
          id: "3",
          title: "Selling"
        },
        {
          id: "4",
          title: "Neighbourhoods"
        },
        {
          id: "5",
          title: "Contact"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
ul.navbar-items {
  display: flex;
  flex-wrap: wrap;
  li {
    list-style: none;
    margin-right: 20px;
    a {
      font-family: "Varela Round", sans-serif;
      font-size: 18px;
      color: white;
      font-weight: normal;
      text-decoration: none;
    }
  }
}
</style>
