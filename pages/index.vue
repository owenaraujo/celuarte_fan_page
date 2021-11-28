<template>
  <div>
  <Inicio/>

  </div>
</template>

<script>
import {  mapState} from 'vuex'
export default {

   data() {
       return {
           
       }
   },
  methods: {
      cambiar(){
          this.usuario= "hola"
      }
  },
  computed: {
...mapState(["menu"])
    
  }
  
  
}
</script>
 