<template>
  <div>
    <slot :header="header" :footer="footer"></slot>
  </div>
</template>
<script>
import Vue from "vue"
import Component from "vue-class-component"

class Settings extends Vue {
  header = "Awesome Site"
  footer = "Incredible Footer"
}

/*
  Codesandbox does not support decorators. This is the alternate
  "non-decorator" version (which kinda stinks 😅)
*/

export default Component({})(Settings)

</script>