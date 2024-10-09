<template>
  <div>
    <!-- <h1>{{ msg }}</h1> -->
    <div
      class="min-h-screen container m-auto flex items-center justify-center w-full">
      <div class="grid grid-cols-1 gap-4 w-1/2">
        <div class="border border-1 p-4 bg-gray-100 w-full">
          <h1 class="text-3xl font-bold text-black">Signup</h1>
          <div class="mt-4 flex flex-col w-full">
            <div class="grid grid-cols-2 gap-4">
              <div class="flex flex-col justify-start items-start">
                <label for="username">First Name</label>
                <input
                  v-model="form_data.first_name"
                  type="text"
                  name="fname"
                  id="fname"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
              </div>
              <div class="flex flex-col justify-start items-start">
                <label for="password">Last Name</label>
                <input
                  v-model="form_data.last_name"
                  type="text"
                  name="lname"
                  id="lname"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
              </div>
            </div>
            <div class="mt-2 grid grid-cols-2 gap-4">
              <div class="flex flex-col justify-start items-start">
                <label for="email">Email</label>
                <input
                  v-model="form_data.email"
                  type="email"
                  name="email"
                  id="email"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
              </div>
              <div class="flex flex-col justify-start items-start">
                <label for="contact">Mobile</label>
                <input
                  v-model="form_data.mobile"
                  type="number"
                  name="mobile"
                  id="mobile"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
              </div>
            </div>
            <div class="mt-2 grid grid-cols-2 gap-4">
              <div class="flex flex-col justify-start items-start">
                <label for="password">Password</label>
                <input
                  v-model="form_data.password1"
                  type="password"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
              </div>
              <div class="flex flex-col justify-start items-start">
                <label for="confirm-password">Confirm Password</label>
                <input
                  v-model="form_data.password2"
                  type="password"
                  class="block w-full flex-1 border py-1.5 pl-1 text-gray-900 placeholder:text-gray-400 focus:ring-0 sm:text-sm sm:leading-6" />
                <div v-if="validatePassword">
                  <small class="text-[#ff0000] mt-1"
                    >Password is incorrect</small
                  >
                </div>
              </div>
            </div>

            <div class="mt-4">
              <button
                type="button"
                @click="saveDetails()"
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
  data() {
    return {
      form_data: {
        email: "",
        mobile: "",
        first_name: "",
        last_name: "",
        password1: "",
        password2: "",
      },
      validatePassword: false,
    };
  },
  methods: {
    saveDetails() {
      if (this.form_data.password1 == this.form_data.password2) {
        this.validatePassword = false;
      } else {
        this.validatePassword = true;
        this.form_data.password2 = "";
        this.form_data.password2.focus();
      }
    },
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
