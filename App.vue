<template>
  <Layout>
  </Layout>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"
import Layout from "./Layout"


class App extends Vue {
  onClick() {
    this.message = "Goodbye"
  }
}

/*
  Codesandbox does not support decorators. This is the alternate
  "non-decorator" version (which kinda stinks 😅)
*/
Prop({ default: "Hello from Prop decorator" })(App, "message")

export default Component({
  components: {
    Layout
  }
})(App)
</script>