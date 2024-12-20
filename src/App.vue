<template>
  <div class="app">
{{name}} -{{ age }}  </div>
<button @click="changeName('Mama')" >

change name
</button>
<button @click="changeAge(49)">change age</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import {ref} from 'vue'
// import HelloWorld from './components/HelloWorld.vue';

// export default defineComponent({
//   name: 'App',
//   components: {

//   },
//   data (){
//     return {
//       name:'LInk',
//       age:30,

//     }
//   },
//   methods : {
//     changeName(name:string){
//       this.name=name
//     },
//     changeAge(age:number){
//       this.age=age
//     }

//   }
// });

export default defineComponent({
  name: 'App',
  setup(){
    const name = ref<string>('KEEE')
    const age = ref<number|string>(5)

    const changeName = (newName : string)=>{
      name.value=newName

    }
    const changeAge = (newAge : number)=>{
      age.value=newAge
    }
    return{
      changeName,changeAge,
      name,age,
    }

  }
})
</script>


