<template>

      
            <div class="  bg-white
                        rounded
                        w-100  p-6 flex flex-col
                        text-center
                        shadow-md
                        hover:shadow-lg
                        
                        smooth">
                <a >
                
                    <img  
                     
                    class="hover:grow hover:shadow-lg " style="width: 100%; height:70%" :src="producto.path" alt="image x">
                    <div class="pt-3 flex items-center justify-between">
                        <p class="text-gray-600 text-xs md:text-sm">
                          {{ producto.category }}
                        </p>
                        <p class="">{{producto.title}}</p>
                        
                    </div>
                    <p class="pt-1 text-gray-900">${{producto.price}}</p>
                </a>
            </div>
    
</template>
<script>
export default {
    props:["producto"]
}
</script>