<template>
  <Settings>
    <Layout slot-scope="{header, footer}">
      <Header slot="header" :header="header"></Header>
      <Content slot="content" :limit="4">
        <div><img src="https://robohash.org/mindy?set=set4" alt=""></div>
        <div><img src="https://robohash.org/john?set=set4" alt=""></div>
        <div><img src="https://robohash.org/kim?set=set4" alt=""></div>
        <div><img src="https://robohash.org/joel?set=set4" alt=""></div>
        <div><img src="https://robohash.org/maggie?set=set4" alt=""></div>
      </Content>
      <Footer slot="footer" :footer="footer"></Footer>
    </Layout>
  </Settings>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"
import Settings from "./Settings"
import Layout from "./Layout"
import { Header, Footer, Content } from "./components"

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
    Footer,
    Content
  }
})(App)
</script>