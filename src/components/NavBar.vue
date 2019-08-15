<template>
  <div class = "navbar">
    <div class = "options">
     <img src = "https://cdn2.hubspot.net/hubfs/3426680/logo_white-1.png"/>
      <a class = "nav-links">
      <font-awesome-icon icon="search" class = "icon"/><div>SEARCH</div>
      <font-awesome-icon icon="tools" class = "icon"/><div>TOOLS</div>
      <font-awesome-icon icon="home" class = "icon"/><div>MY PROPERTIES</div>
      </a>
    </div>  
  <div class = "user-display">
    <div class = "properties">
      <a class = "properties-amount">Remaining Properties:</a>
      <span>2</span>
    </div>
    <div class="vertical-line"/>
    <div class = "user-box">
    <font-awesome-icon icon="question-circle" class = "question"/>
     <img
     class = "profile-pic"
     src = "https://images.pexels.com/photos/1043471/pexels-photo-1043471.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
     >
    </div>
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
.navbar { 
  border: 1px solid #424657; 
  background-color: #424657;
  color: white;
  display: flex;
  flex-direction: row;
  font-family: 'Comfortaa', cursive;
}
.options{display:flex;
  width:75%;
  margin-left: 3%;
}
.user-display{display:flex;
  margin-left: auto;
  width: 23%;
}
.nav-links{
  margin-top: 18px;
  cursor:pointer;
  display: flex;
  justify-content: space-between;
  width: 54%;
  margin-left: 2%;
}
.properties{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  width: 210px;
  margin-right: 10px;
}
.properties-amount{
  font-style: italic;
  margin-top: 15px;
}
span{
  font-weight: bold;
  margin-top: 15px;
}
.vertical-line{
    width: 1px;
    background-color: white;
    height: 60%;
    margin-top: 10px;
}
.profile-pic{
    display: flex;
    height: 38px;
    width: 36px;
    border-radius: 50px;
    margin-left: 15px;
    margin-top: 8px;
}
.icon{
    margin-left: 13%;
}
.user-box{
  display:flex
}
.question{
  margin-top: 18px;
    margin-left: 8px;
}
</style>