<template>
  <HeaderPage v-if="!this.$route.meta.hideHeader" />
  <router-view />
  <FooterPage v-if="!this.$route.meta.hideFooter" />
</template>
<script>
import HeaderPage from "@/components/global/HeaderPage.vue";
import FooterPage from "@/components/global/FooterPage.vue";
export default {
  name: "App",
  computed: {
    currentUser() {
      return this.$store.state.auth.user;
    },
  },
  components: {
    HeaderPage,
    FooterPage,
  },
};
</script>
<style>
@import "@/assets/style/common.css";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
