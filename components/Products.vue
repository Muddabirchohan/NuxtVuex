<template lang="html"> 
<div>

    <div v-for="pro in products.data" class="flex-container" v-bind:key="pro.key">      
      <b-card>
      <div>
      <p>
     {{pro._id}}  
     <img :src="'https://greencommunitylaundry.herokuapp.com/api/Images/' + pro.image"  width="270px"/> 
     </p>
     <div class="moveLeft">
     <b-button v-on:click="addData(pro)"> Add </b-button>
     <b-button v-on:click="ShowDesc(pro)"> Description </b-button>
     </div>

</div>
</b-card>
 </div>
</div>

</template>


<script>

export default {

 created() {
    this.$store.dispatch("fetchProducts");
  },
  
  methods: {
  addData(obj){
         this.$store.dispatch("addToCart",obj);
  },

  ShowDesc(obj){
 this.$store.dispatch("showDesc",obj);
  }
},
 computed: {
    products() {
      return this.$store.getters.products;
      console.log(this.$store.getters.products);
    }
  }
};
</script>



<style>
.flex-container {
  display: flex;
  flex-flow: row;
  justify-content: space-around;
  /* align-content: center; */
  background-color: lightgrey;
}

.flex-container div {
  justify-content: center;
}

.flex-container > div {
  margin-top: 50px;
}

.moveLeft {
  margin-left: 50px;
}

</style>