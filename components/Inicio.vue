<template>
  <div
    class="
      bg-white
      text-gray-600
      work-sans
      leading-normal
      text-base
      tracking-normal
    "
  >
    <!--Nav-->
    <Nav :ruta="ruta" />

    <Carusel/>
    <section class="bg-white py-8" >
      <div class="container mx-auto flex items-center flex-wrap pt-4 pb-12">
        <nav id="store" class="w-full z-30 top-0 px-6 py-1">
          <div
            class="
              w-full
              container
              mx-auto
              flex flex-wrap
              items-center
              justify-between
              mt-0
              px-2
              py-3
            "
          >
            <div
              class="
                uppercase
                tracking-wide
                no-underline
                hover:no-underline
                font-bold
                text-gray-800 text-xl
              "
            
            >
              nuestros productos
            </div>

          </div>
        </nav>
<!-- prueba  -->
<style>
  
</style>
<div class="container p-4">
        <div class="row">
            <div class="card-columns">

                

                <div class="card animated fadeInDown  "  v-for="image in productos" :key="image._id">
                    <img :src="image.path" class="card-img-top" :alt="image.filename">
                    <div class="card-body">
                        <h5 class="card-title">{{image.title}}</h5>
                        <p class="card-text">{{image.description}}</p>
                        
                       
                    </div>
                </div>
                
            </div>
        </div>
    </div>
<!-- prueba  -->


       <div class="container p-5 hidden">
          <div 
        class="grid gap-x-8 gap-y-4 md:grid-cols-3 sm:grid-cols-1 grid-cols-1 xl:grid-cols-4 auto-cols-max "
        >
          <Producto
          v-for="item in productos"
          :producto="item"
          :key="item._id"
        />
        </div>
       </div>
      </div>
    </section>

   
<Footer/>
    
  </div>
</template>
<script>
import { mapState } from "vuex";
import axios from "axios"
export default {
  data() {
    return {
      ruta: { url: "/servicioTecnico", nombre: "Servicio Técnico" },
productos: [],
      store: false,
      
    };
  },
  created(){
    this.getProducts()
  },
  methods: {
  async  getProducts (){
const {data} = await axios.get("/api/image")
this.productos = data
  },
   
  },
  computed: {
    ...mapState(["menu"]),
  },
};

</script>
 <style scoped>
 @import "../static/static/style.css";
 
 @media  (min-width: 900px) {
    .card-columns {
    column-count: 4;
      
  }
  }
 </style>