<template>
  <navbar />
  <div class="home">
    
    <router-view />
    <div class="block">
      <h1>The Archive:</h1>
      <h2>Web-based Research Compendium - TIP </h2>
    </div>
  </div>

  
<form @submit.prevent="handleSearch">
  <input type="text" v-model="search">

  <div class="search">
    <button>Search</button>
  </div>
</form>

<div class="Block1">
<div class="head">
  <h1>Recommendations:</h1>
</div>

<div class="articles">
  <div class="Article1">
    <router-link to="/article"><p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Reiciendis quaerat harum optio quis magnam odit qui ex expedita, necessitatibus vel provident, iure minima. Quis atque repellendus, unde consequuntur pariatur recusandae.</p></router-link>  
  </div>

  <div class="Article2">
    <router-link to="/article"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum in praesentium nobis expedita ratione natus pariatur beatae, rerum cupiditate et doloremque, labore fugiat iste provident vitae vel, incidunt explicabo enim.</p></router-link>
  </div>
  
  <div class="Article3">
    <router-link to="/article"><p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam numquam cumque unde saepe nihil voluptas fuga inventore blanditiis, recusandae necessitatibus quos veniam facere amet magnam, minima labore excepturi facilis esse.</p></router-link>
  </div>
</div>
</div>



</template>

<script>
import navbar from '@/views/navbar.vue';

export default {
  name: 'HomeView',
  components: { navbar },
  data() {
    return {
      search: '',
    }
  },
}
</script>

<style scoped>
div.block {
  margin: 150px auto 0;
  vertical-align: text-bottom;
  width: 550px;
  border-radius: 20px;
  background: #5d5d5d;
  color: #fff;
  padding: 10px;
  opacity: 0.7;
}
input {
  margin: 50px;
  border-radius: 20px;
  height: 35px;
  width: 500px;
  
}
button{
  margin: 0px 0px 200px ;
  height: 25px;
  width: 150px;
  border-radius: 10px;
  background-color: rgb(255, 255, 106);
}
.head h1 {
  text-decoration: underline;
  position: relative;
  z-index: 1;
}
.articles {
  height: 500px;
  width: 105%;
  display: flex;
  margin: 0 0 0;
  padding-top: 100px;
  position: relative;
  left: -10px;
}
.Article1 {
  height: 250px;
  width: 250px;
  background: #5d5d5d;
  border-radius: 25px;
  margin: 0 150px 0px 100px;
  color: #fff;
  text-align: left;
  padding: 30px;
  border: 2px solid;
  border-color: yellow;
}
.Article2 {
  height: 250px;
  width: 250px;
  background: #5d5d5d;
  border-radius: 25px;
  margin: 0 150px 0px 0;
  color: #fff;
  text-align: left;
  padding: 30px;
  border: 2px solid;
  border-color: yellow;
}
.Article3 {
  height: 250px;
  width: 250px;
  background: #5d5d5d;
  border-radius: 25px;
  margin: 0 0px 0px 0;
  color: #fff;
  text-align: left;
  padding: 30px;
  border: 2px solid;
  border-color: yellow;
}
</style>