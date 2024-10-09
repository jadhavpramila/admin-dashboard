<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <!-- <Login></Login> -->
    <Signup></Signup>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
// import Login from "@/components/Login.vue";
import Signup from "@/components/Signup.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld,
    //Login,
    Signup,
  },
};
</script>
