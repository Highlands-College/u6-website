<template>
  <div class="footer">
    <div class="links">
      <a class="mr-3" href="#">Twitter</a>
      <a href="#">LinkedIn</a>
    </div>
    <p>Copyright © 2021</p>
  </div>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
.footer {
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border-top: 1px solid #222222;
}
</style>