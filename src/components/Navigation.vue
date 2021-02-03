<template>
  <div
      class="w-full bg-gray-50 dark:bg-gray-800"
  >
    <div
        class="flex flex-col w-full md:w-5/6 mx-auto md:items-center md:justify-between md:flex-row lg:px-8"
    >
      <div class="p-4 flex flex-row items-center justify-between">
        <router-link
            class="text-lg font-semibold tracking-widest bg-gray-50 text-gray-800 uppercase rounded-lg dark:text-gray-200 focus:outline-none focus:shadow-outline"
            to="/"
        >
          HV Development
        </router-link>
        <button
            class="md:hidden rounded-lg focus:outline-none focus:shadow-outline"
            @click="menuOpen = !menuOpen"
        >
          <svg
              fill="black"
              viewBox="0 0 20 20"
              class="w-6 h-6"
          >
            <path
                :class="menuOpen ? 'hidden' : ''"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
            ></path>
            <path
                :class="menuOpen ? '' : 'hidden'"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
            ></path>
          </svg>
        </button>
      </div>
      <nav
          :class="menuOpen ? '' : 'hidden'"
          class="flex flex-col flex-grow pb-4 mx-4 md:mx-0 md:pb-0 md:flex md:justify-end md:flex-row"
      >
        <Button class="mr-2" title="About" path="/about" />
        <Button class="mr-2" title="Case Studies" path="/case-studies" />
        <Button class="mr-2" title="Contact" path="/contact" />
        <div class="relative">
          <button
              @click="dropdownOpen = !dropdownOpen"
              class="flex flex-column items-center justify-center md:w-full px-4 py-2 mt-2 mx-4 md:mx-0 text-sm font-semibold text-left bg-transparent rounded-lg dark:bg-transparent dark:hover:bg-gray-600 md:w-auto md:inline md:mt-0 hover:bg-gray-200 focus:outline-none focus:shadow-outline"
          >
            <svg
                fill="black"
                viewBox="0 0 20 20"
                :class="dropdownOpen ? 'rotate-180' : 'rotate-0'"
                class="inline w-4 h-4 mt-1 transition-transform duration-200 transform md:-mt-1"
            >
              <path
                  d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
              ></path>
            </svg>
          </button>
          <div
              class="absolute bg-gray-50 right-0 w-full mt-2 origin-top-right rounded-md shadow-md md:w-48"
          >
            <div
                @click="dropdownOpen = !dropdownOpen"
                class="p-2 rounded-md shadow dark:bg-gray-800"
                :class="dropdownOpen ? '' : 'hidden'"
            >
              <Button title="User" path="#" icon="user" />
              <Button title="Settings" path="#" icon="cog" />
              <Button title="Logout" path="#" icon="sign-out-alt" highlight="bg-red-400" />
            </div>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Button from '@/components/Button.vue'

export default defineComponent({
  name: 'Navigation',
  components: {
    Button
  },
  setup() {
    const dropdownOpen = ref(false)
    const menuOpen = ref(false)

    return {
      dropdownOpen,
      menuOpen
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav {
  margin-bottom: 20px;
  padding: 30px 10%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.links {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

@media only screen and (max-width: 600px) {
  .links {
    flex-direction: column !important;
  }
}

.links a {
  padding: 6px 12px;
}

.links div:not(:last-of-type) {
  margin-right: 30px;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a, p {
  text-decoration: none;
  color: black;
}

a:visited {
  color: black;
}
</style>
