<template>
  <Settings>
    <Layout slot-scope="{header, footer}">
      <Header slot="header" :header="header"></Header>
      <div slot="content" class="flex-grow p-4">Amazing Content</div>
      <Footer slot="footer" :footer="footer"></Footer>
    </Layout>
  </Settings>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"
import Settings from "./Settings"
import Layout from "./Layout"
import { Header, Footer } from "./components"

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
    Layout,
    Header,
    Footer
  }
})(App)
</script>