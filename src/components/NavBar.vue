<template>
  <div>
    <div>
      <a v-for="item in menuItems" :key="item.name" :class="item.active ? 'active' : ''">{{item.name}}</a>
    </div>
    <div>
      <a>Go To Platform</a>
    </div>
    <div>
      <a>{{userInitials}}</a>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavBar extends Vue {
    @Prop()
    private userInitials!: string

    @Prop()
    private menuItems!: object[]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>