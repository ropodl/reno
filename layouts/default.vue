<template>
  <v-app>
    <Navbar />
    <v-main>
      <nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>
<style lang="scss">
.v-application {
  font-family: "Varela Round", sans-serif !important;
}
</style>
