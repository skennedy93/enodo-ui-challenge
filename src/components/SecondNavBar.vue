<template>
  <div class = "second-nav">
  <div class = "description">
  <div class = "property-name">   
   <div>
      Property Analysis
    </div>
    <a class = "property-address" href="">
      {{property.name ? property.name : property.address}}
    </a>
    </div>
  <div class = "nav-buttons">
    <div class = "button-share">Share</div>
    <div class = "button-export">Export</div>
    </div>
   </div>
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
.second-nav{
  border: 1px solid #ccc;
  display: flex;
  flex-direction: row;
  background-color:white
}
.description{
  display:flex;
  width:100%;
  padding:1%
}
.nav-buttons{
  display:flex;
  margin-left:69%;
  width: 12%;
  justify-content: space-around
}
.button-share{
  border: 1px solid #82b32e;
  color: #82b32e;
  background-color: inherit;
  padding:7px;
  height:20px;
  border-radius:2px;
  cursor:pointer;
  width:60px;
}
.button-export{ 
  border: 1px solid #82b32e;
  color: white;
  background-color: #82b32e;
  padding:7px;
  height:20px;
  border-radius:2px;
  cursor:pointer;
  width:60px;
}
.property-name{
  display:flex;
  width: 275px;
  justify-content: space-between;
  padding: 7px;
}
.property-address{
color: #aeafb5
}
</style>