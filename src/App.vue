<template>
  <Navigation />
  <router-view />
  <Footer />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Navigation from "@/components/Navigation.vue";
import Footer from '@/components/Footer.vue'

export default defineComponent({
  name: "App",
  components: {
    Navigation,
    Footer
  }
});
</script>

<style>
@font-face {
  font-family: 'Luam';
  src: url('assets/fonts/Luam-Regular.ttf') format('truetype');
}

* {
  padding: 0;
  margin: 0;
  font-family: "Luam", Helvetica, 'sans-serif';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 20px;
}

body {
  background-color: #eeeeee;
}
</style>
