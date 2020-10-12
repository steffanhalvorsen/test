<template>
  <div class="home">
    <img @click="action" alt="Vue logo" src="../assets/logo.png" />
    <Hello-World msg="Welcome to Your Vue.js App" :test="'yup'" @click="action" v-if="true"/>
    <HelloWorld2/>
    <HelloWorld3/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import HelloWorld2 from "../components/HelloWorld2.vue";
import HelloWorld3 from "./HelloWorld3.vue";
import ax from 'axios'

export default {
  name: "Home",
  components: {
    HelloWorld,
    HelloWorld2,
    HelloWorld3
  },
  methods: {
    action() {
      console.log('sososozu')
      ax('https://cors-anywhere.herokuapp.com/http://google.com').then(g => {
        console.log('google results', g)
      })
      axios('https://cors-anywhere.herokuapp.com/http://google.com').then(g => {
        console.log('google results 2', g)
      })
    }
  }
};
</script>
