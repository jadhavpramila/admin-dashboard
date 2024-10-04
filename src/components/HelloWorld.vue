<template>
  <div>
    <!-- <h1>{{ msg }}</h1> -->
    <div class="min-h-screen bg-gray-100 flex items-center justify-center">
      <h1 class="text-3xl font-bold text-blue-600">
        Hello, Tailwind CSS with Vue!
      </h1>
    </div>
    <!-- <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p> -->
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
a {
  color: #42b983;
}
</style>
