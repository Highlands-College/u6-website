<template>
  <div class="home">
    <p>This is a home page</p>
    <img
      class="image"
      src="https://images.pexels.com/photos/4164418/pexels-photo-4164418.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
      alt="Programming Image"
    />
  </div>
  <Footer />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Footer from '@/components/Footer.vue'

export default defineComponent({
  name: "Home",
  components: {
    Footer
  }
});
</script>

<style scoped>
.image {
  width: 50%;
}
</style>
