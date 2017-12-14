<template>
  <Settings>
    <Layout slot-scope="{header,footer}">
      <h1 slot="header" class="bg-blue text-white p-2">{{header}}</h1>
      <div slot="content" class="flex-grow p-3">Amazing content</div>
      <h2 slot="footer" class="bg-grey-light text-blue p-2 text-center">{{footer}}</h2>
    </Layout>
  </Settings>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"
import Settings from "./Settings"
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
    Settings,
    Layout
  }
})(App)
</script>