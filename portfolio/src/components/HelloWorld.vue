<script>
import FruitItem from './FruitItem.vue'; 


export default{
  name:'Hello World',
  components:{
    FruitItem
  },
  
 
  data(){
    return {
      message:'Hello World From Vite',
      fruits:['Apple','Banana','Orange'],
      fr:''
    }
  },
methods: {
    addFruit(){
      this.fruits.push(this.fr)
    },
    RemoveFruit(fruitName) {
      this.fruits = this.fruits.filter(fruit => fruit !== fruitName)
    }
}
}
</script>

<template>
 <div>
  <h1>{{ message }}</h1>
  <input v-model = "message">
  <p v-if="message.length > 5">That's a long Message</p>
  <br>

  <input type="text" v-model ="fr" placeholder = 'Input a Fruit'>
  <button @click="addFruit">Add Fruit</button>
  <ul>
  <FruitItem v-for="(fruit, index) in fruits" :key="index" 
  :fruitName="fruit"
  @remove ="RemoveFruit" />
</ul>
 </div>
</template>

<style>
h1 {
  color:'blue'
}
</style>