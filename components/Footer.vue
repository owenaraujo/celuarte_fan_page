<template>
    <footer class="container mx-auto bg-white py-8 border-t border-gray-400">
      <h5 class="text-center">comunicate con nosotros</h5>
      <div class="container flex px-3 py-8">
        <div class="w-full mx-auto justify-center flex flex-wrap">
          <a @click="toWs">
            <img class="p-5" src="/static/ws.png" alt="" />
          </a>
          <a @click="toIg">
            <img src="/static/ig.png" class="p-5" alt="" />
          </a>
          <a @click="toFb">
            <img src="/static/fb.png" class="p-5" alt="" />
          </a>
        </div>
      </div>
    </footer>
</template>
<script>
export default {
    methods:{
         toWs() {
      window.open(this.ws, "_blanck");
    },
    toIg() {
      window.open(this.ig, "_blanck");
    },
    toFb() {
      window.open(this.fb, "_blanck");
    },
    },
    data(){
        return{
            ws: "https://wa.me/message/QN44EMB2UVLKG1",
      ig: "https://www.instagram.com/celuarte/?hl=es-la",
      fb: "https://www.facebook.com/Celuarte-207328293281630/",
        }
    }
}
</script>