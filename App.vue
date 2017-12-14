<template>
  <h1 @click="onClick">
    {{message}}
  </h1>
</template>

<script>
import Vue from "vue"
import Component from "vue-class-component"

class App extends Vue {
  message = "Hello from class"

  onClick() {
    this.message = "Goodbye"
  }
}

/*
  Codesandbox does not support decorators. This is the alternate
  "non-decorator" version (which kinda stinks 😅)
*/

export default Component({})(App)

</script>