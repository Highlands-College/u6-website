<template>
  <router-link
      class="flex flex-row justify-start items-center px-4 py-2 text-sm hover:bg-gray-200 dark:hover:bg-gray-600 font-semibold bg-transparent text-gray-800 dark:text-gray-200 md:mt-0 rounded-lg dark:bg-transparent focus:outline-none focus:shadow-outline"
      :to="path"
  >
    {{ title }}
  </router-link>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Button',
  props: {
    title: {
      type: String,
      required: true
    },
    path: {
      type: String,
      required: true
    }
  }
})
</script>

<style>
.button {
  display: flex;
  justify-content: start;
  align-items: center;
  padding: 2rem 4rem;
}

.button:focus {
  outline: none;
}

.button:hover {
  cursor: pointer;
}
</style>