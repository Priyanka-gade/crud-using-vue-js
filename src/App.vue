<template>
  <div>
    <AddToDo v-on:add-todo="addtododata"></AddToDo>
    <ToDos v-bind:Todata="Todata" v-on:delete-todo="deletetododata"></ToDos>
  </div>
</template>

<script>
import AddToDo from './components/AddToDo.vue'
import ToDos from './components/ToDos.vue'


export default {
  name:'App',
    components: { AddToDo, ToDos },
    data(){
  return{
    Todata :[
      {
        id:'1',
        title:'Todo 1',
        completed:false
      },
      {
        id:'2',
        title:'Todo 2',
        completed:true
      },
      {
        id:'3',
        title:'Todo 3',
        completed:false
      },
      {
        id:'4',
        title:'Todo 4',
        completed:true
      },
      {
        id:'5',
        title:'Todo 5',
        completed:true
      }
    ]
  }
},
methods:{
  addtododata(newtodo){     //v-on: add-todo ="addtododata" used
    //adding the dodata to the Todata array
    this.Todata=[...this.Todata,newtodo ]
  },
  deletetododata(id){
    this.Todata= this.Todata.filter((items)=>items.id !== id)
  }
}  
}

</script>

<style>

</style>
