
<script>
import Nav from './components/Nav.vue'
export default {
components: { Nav },

data()
{
  return {
    plants:
    [
      {id: 1, name: "Snake Plant", type:"Indoor", instock:true},
      {id: 1, name: "Sun Flower", type:"Outdoor", instock:false}
    ],
    filterType: 'All'
  }
},
methods: {
  handleFilter(type){
  this.filterType = type;
  console.log(this.filterType);
  }
}

}

</script>
<template>
  <div>
    <Nav @filter-plants="handleFilter"/>
  <h1>Plant Store App</h1>
  <router-view :plants="plants" :filterType="filterType"/>
  </div>
</template>



