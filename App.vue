<template>
  <h1 @click="onClick">
    {{message}}
  </h1>
</template>

<script>
import Vue from "vue"
import { Component, Prop } from "vue-property-decorator"

export default Component({
  props: {
    message: {
      default: "Hello from default prop"
    }
  }
})(
class App extends Vue {
  // Decorators not currently supportted in codesandbox
  // @Prop({ default: "Hello from Prop decorator" })
  // message

  onClick() {
    this.message = "Goodbye"
  }
})
</script>