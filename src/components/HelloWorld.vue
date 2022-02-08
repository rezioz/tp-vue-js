

<template>


  <input v-model="nombre">
  {{cm}}
  {{mm}}

  <form v-if="seen" id="hide">
    nom:<input v-model="nom">
    <br>
    prenom<input v-model="prenom">
    <br>
    date de naissance<input type="date" v-model="date">
    <br>
    adresse<input v-model="addr">
  </form>

  <div id="app" v-on:click="seen = !seen" class="control">
      <p>click app</p>
  </div>


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
      seen: true,

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
