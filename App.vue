<template>
  <div>
    <slot name="header"></slot>
    <h1 @click="onClick">
      {{message}}
    </h1>
    <slot name="footer"></slot>
  </div>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"


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

export default Component({})(App)

</script>