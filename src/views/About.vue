<template>
  <div class="about">
    <p>This is an about page</p>
    <img
        class="image"
        src="https://pbs.twimg.com/profile_images/1308420818926436352/qDMjsU1T_400x400.jpg"
        alt="Programming Image"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "About"
});
</script>

<style scoped>
.image {
  width: 50%;
}
</style>