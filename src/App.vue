<template>
  <div id="app">
    <Kanban :data="data"/>
    
  </div>
</template>

<script>
import Kanban from "./components/Kanban"

export default {
  name: 'App',
  components: {
    Kanban
  },
  data(){
    return{
      data:[
        {
          name:"Todo",
          color:"#F9ACC0",
          tasks:[]
        },
        {
          name:"Doing",
          color:"#86A5C4",
          tasks:[]
        },
        {
          name:"Done",
          color:"#C4B3C3",
          tasks:[]
        }
      ]
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
}
</style>
