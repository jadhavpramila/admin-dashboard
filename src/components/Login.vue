<template>
  <div>
    <!-- <h1>{{ msg }}</h1> -->
    <div
      class="min-h-screen container m-auto flex items-center justify-center w-full">
      <div class="grid grid-cols-1 gap-4 w-1/3">
        <div class="border border-1 p-4 bg-gray-100 w-full">
          <h1 class="text-3xl font-bold text-black">Login</h1>
          <div class="mt-4 flex flex-col w-full">
            <div class="flex flex-col justify-start items-start">
              <label for="username">Username</label>
              <input
                type="text"
                name="username"
                id="username"
                class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
            </div>
            <div class="mt-2 flex flex-col justify-start items-start">
              <label for="password">Password</label>
              <input
                type="password"
                name="password"
                id="password"
                class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
            </div>
            <div class="mt-4">
              <button
                type="button"
                class="rounded-md bg-white px-2.5 py-1.5 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50">
                Submit
              </button>
            </div>
          </div>
        </div>
      </div>
      <!-- <h1 class="text-3xl font-bold text-blue-600">
        Hello, Tailwind CSS with Vue!
      </h1> -->
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
