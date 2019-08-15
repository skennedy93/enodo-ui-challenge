<template>
  <div class = "summary">
    <div class="image">
      <img src="https://maps.googleapis.com/maps/api/streetview?size=400x200&pitch=10&fov=180&location=320%20N%20Canal%20St,%20Chicago,%20IL%2060606&key=AIzaSyApsGVNO-Ms2sIJM4PtmwC5VfeutsZSExo">
        <!-- Name: {{property.name}} -->
        <div class = "property">
        <div class = "address">{{property.address}}</div>
        <div class = "city">{{property.city}}</div>
        <div class = "property-info">
        {{property.numberUnits ? property.numberUnits : '--'}} /
        {{property.propetyType ? property.propetyType : '--'}} /
        {{property.yearBuild ? property.yearBuild : '--'}}
        </div>
        <div class = "avm">{{property.avm ? property.avm : '--'}} AVM</div>  
      </div> 
    </div>

    <LateralNav class = "section" />

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import LateralNav from './LateralNav.vue'


@Component({
  components: {
    LateralNav
  }
})
export default class NavBar extends Vue {
    @Prop()
    private property!: object

    private propertySections: object[] = [

    ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .summary{
    display:flex;
    border: 1px solid #ccc;
    background-color:white;
    flex-direction: column;
    width: 18%;
    height: 540px;
    margin-top: 60px;
    margin-left:50px;
}
  .image{
    display:flex;
    flex-direction: column
}
  .property-info{
    flex-direction: row;
    color: #858585
}
  .avm{
    color:#82b32e;
}
  .address{
    font-size: 25px;
    font-weight: bold;
  }
  .city{
    color: #858585
  }
  .property{
    text-align: left;
    margin-left: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    height: 138px;
  }
  .section{
    text-align: left;
    display: flex;
    height: 170px;
    justify-content: space-evenly;
    margin-top: 15px;
  }

</style>