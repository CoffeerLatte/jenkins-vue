<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";


const firebaseConfig = {
  apiKey: "AIzaSyAkPjTZGmnUDfdyp8ie_lQiDsFy23yVaC0",
  authDomain: "jenkins-vue-7680f.firebaseapp.com",
  projectId: "jenkins-vue-7680f",
  storageBucket: "jenkins-vue-7680f.appspot.com",
  messagingSenderId: "166064333460",
  appId: "1:166064333460:web:232fe33d7d57587f6f0a81",
  measurementId: "G-3EQH67WGNB"
};

const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
