<template>
  <div class="about">
    <AboutPage msg="Welcome to About Page" />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutPage from "@/components/AboutPage.vue";

export default {
  name: "About",
  components: {
    AboutPage,
  },
};
</script>
