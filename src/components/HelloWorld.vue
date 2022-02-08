

<template>


  <input v-model="nombre">
  {{cm}}
  {{mm}}

  <form>
    <input v-model="nom">
    <input v-model="prenom">
    <input v-model="date">
    <input v-model="addr">
  </form>>


</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({

  data:()=>{
    return {
      nombre:'',
      nom:'',
      prenom:'',
      date:'',
      addr:'',

    }
  },

  computed: {
    // un accesseur (getter) calculé
    m() {
      // `this` pointe sur l'instance vm
      return this.nombre+"m";
    },
    cm() {
      // `this` pointe sur l'instance vm
      return this.nombre*100+"cm";
    },

    mm() {
      // `this` pointe sur l'instance vm
      return this.nombre*1000+"mm";
    }
  }

})
</script>



<style scoped>
a {
  color: #42b983;
}
</style>
