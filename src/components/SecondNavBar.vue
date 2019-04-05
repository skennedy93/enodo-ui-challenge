<template>
  <div>
    <div>
      Property Analysis
    </div>
    <div>
      {{property.name ? property.name : property.address}}
    </div>
    <button type="button">Share</button>
    <button type="button">Export</button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class SecondNavBar extends Vue {
    @Prop()
    private property!: object
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>