<template>
  <v-app-bar app color="#124578" dark flat class="px-12">
    <v-btn>
      <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>
      Atlas-Expo
      <v-spacer></v-spacer>
      <v-btn text @clcik="scroll('home')" class="text-yellow">Home</v-btn>
      <v-btn text @clcik="scroll('about')">About</v-btn>
      <v-btn text @clcik="scroll('portfolio')">Portfolio</v-btn>
      <v-btn text @clcik="scroll('services')">Services</v-btn>
      <v-btn text @clcik="scroll('page')">Page</v-btn>
      <v-btn text @clcik="scroll('blog')">Bio</v-btn>
      <v-btn text @clcik="scroll('contact')">Contact</v-btn>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style scoped></style>
