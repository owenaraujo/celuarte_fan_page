<template>

    <div>
        {{hola}}
        <input type="text" v-model="hola">
        <button @click="send">send</button>
    </div>
</template>
<script>
export default {
    setup() {
        let hola= ref(2)
        function send() {
            hola.value= "mama mia"
        }
        return{hola ,send}

    }
}
</script>