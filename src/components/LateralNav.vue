<template>
  <div class = "list">

      <div class = "property-bottom-container">
      <div class = "option-name">
      <font-awesome-icon icon="list-alt" />
      Comparables
      </div>
      </div>
      <div class = "property-bottom-container">
      <div class = "option-name">
      <font-awesome-icon icon="money-bill" />
      Operating Expenses
      </div>
      </div> 
      <div class = "property-bottom-container">
      <div class = "option-name">
      <font-awesome-icon icon="newspaper" />
      Rent roll / Unit Mix'
      </div>
      </div> 
      <div class = "property-bottom-container">
      <div class = "option-name">
      <font-awesome-icon icon="star" />
      Amenities
      </div>
      </div> 
      <div class = "property-bottom-container">
      <div class = "option-name">
      <font-awesome-icon icon="map-marker-alt" />
      Market
      </div>
      </div> 

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavBar extends Vue {
    @Prop()
    private options!: object[]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.list{
display:flex;
flex-direction: column;
}
.property-bottom-container { 
  height: 50px;
  
}
.property-bottom-container:hover { 
  background-color: #424657;
  color:white;
  cursor:pointer;
  height: 50px;
  
}
.option-box { 
  margin-top: 9px;
}
.option-name{
  margin-left:10px;
  margin-top: 5px;
}
.search{
    height: 20px;
}
</style>