<template>
  <div class = "expenses-table">
      <div class = "title">
      Historical Operating Expenses
      </div>
      <hr/>
    <table>
      <tr>
        <th></th>
        <th v-for="header in headers" :key="header">{{header}}</th> 
      </tr>
      <tr v-for="(row, i) in items" :key="i">
        <td>{{row.name}}</td>
        <td class = "amount" v-for="(value, x) in row.values" :key="x">{{value}}</td> 
      </tr>
      <br/>
    </table>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavBar extends Vue {
    @Prop()
    private headers!: string[]

    @Prop()
    private items!: object[]

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.expenses-table{display:flex;
    width: 94%;
    background-color: white;
    border: 1px solid #ccc;
    flex-direction: column;
    margin-left: 3%;
    margin-top: 35px;
    margin-bottom: 75px;
}
.title{
    margin-top: 15px;
    margin-right: 827px;
  
}
hr {
    display: block;
    height: 1px;
    border: 0;
    border-top: 1px solid #ccc;
    margin: 1em 0;
    padding: 0;
}
.list-container{
    margin-top: 15px;
}
td {
    border-bottom: 1px solid #ddd;
    padding: 10px;
    text-align: left;
}
th{
    border-bottom: 1px solid #ddd;
    padding: 10px;
    text-align: right;
}
.amount{
    text-align: right;
}
table{
    width: 65%;
    margin-left: 15px;
}
</style>