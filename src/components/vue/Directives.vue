<script setup>
import { ref } from "vue";
const ischecked = ref (true)


const users = ["pepe","ana","juana","lola"]

</script>
<template>
    <ul>
        <li v-for=" ( user, index) in users" :key="index"> {{ index}} {{ user }}</li>
    </ul>


    <input type="checkbox" id="check" v-model="ischecked"/>
    <label for=" check">pinchame </label>
    <div class="bg-blue-400 text-white rounded py-1 px-2"
    :class="{ 'bg-orange-500': ischecked}"

    >

        Este es un mensaje 
    </div>
    <div v-show="ischecked">
        este es un mensaje que podria ocultar 
    </div>
    <div v-if="ischecked">
        este es un mensaje que podria ocultar 
    </div>
    <div v-else>
        esto se ve porque no cumplio la condicion del if  
    </div>
</template>
