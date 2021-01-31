<template>
  <v-app-bar absolute color="transparent" height="70" elevation="0">
    <v-container>
      <v-row class="d-flex align-center mt-10">
        <span class="font-weight-bold text-h4 white--text">Reno</span>

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
