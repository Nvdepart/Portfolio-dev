<template>
  <v-app-bar app color="#124578" dark flat class="px-12">
    <v-btn>
      <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>
      Atlas-Expo
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-yellow btn">
      <span>Home</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div
    ></v-btn>
    <v-btn text @click="scroll('about')" class="btn">
      <span>About</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
    </v-btn>
    <v-btn text @click="scroll('portfolio')" class="btn">
      <span>Portfolio</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
    </v-btn>
    <v-btn text @click="scroll('services')" class="btn">
      <span>Services</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
    </v-btn>
    <v-btn text @click="scroll('page')" class="btn">
      <span>Page</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
    </v-btn>
    <v-btn text @click="scroll('blog')" class="btn">
      <span>Bio</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
    </v-btn>
    <v-btn text @click="scroll('contact')" class="btn">
      <span>Contact Us</span>
      <div class="top"></div>
      <div class="left"></div>
      <div class="bottom"></div>
      <div class="right"></div>
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

<style scoped>
.btn {
  padding: 10px;
  background-color: #124578;
  border: none;
  font-size: 12px;
  position: relative;
  /*overflow: hidden;*/
  transition: 500ms;
}

.btn span {
  color: rgb(8, 3, 33);
  position: relative;
  transition: 500ms;
  transition-delay: 500ms;
  font-size: 16px;
  text-transform: uppercase;

  font-weight: 600;
}

.btn:before {
  content: "";
  position: absolute;
  width: 0%;
  height: 0%;
  left: 50%;
  right: 50%;
  top: 50%;
  bottom: 50%;
  transition: 500ms;
  transition-delay: 500ms;
  background-color: rgb(220, 236, 5);
  box-shadow: 0 0 10px rgb(0, 4, 255), 0 0 30px rgb(13, 5, 245), 0 0 50px red;
}

.btn div {
  transition: 500ms;
  position: absolute;
  background-color: rgb(4, 93, 236);
  box-shadow: 0 0 15px rgb(5, 5, 248), 0 0 30px rgb(56, 6, 222), 0 0 50px red;
}

.btn .top {
  width: 2px;
  height: 2px;
  top: 0;
  left: 0;
}

.btn .bottom {
  width: 2px;
  height: 2px;
  bottom: 0;
  right: 0;
}

.btn .left {
  width: 2px;
  height: 2px;
  top: 0;
  left: 0;
}

.btn .right {
  width: 2px;
  height: 2px;
  bottom: 0;
  right: 0;
}

.btn:hover {
  color: #000;
}

.btn:hover span {
  color: #000;
}

.btn:hover:before {
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.btn:hover .top,
.btn:hover .bottom {
  width: 100%;
}

.btn:hover .left,
.btn:hover .right {
  height: 100%;
}
</style>
