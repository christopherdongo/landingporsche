<template>
    <div class="Nav container mx-auto my-8 grid grid-flow-col grid-cols-1 md:grid-cols-auto gap-4">
        <div>
           <img :src="PorscheLogo" alt="Porsche logo in colors" class="w-16 mx-auto md:mx-0"/>
        </div>
        <div class="hidden md:block">
            <div class="grid-flow-col grid grid-cols-7 gap-4 items-center">
            <p v-for="(option,index) in menu" :key="index" @click="openLink(option.link)" class="cursor-pointer text-xs font-bold ">{{option.title}}</p>
        </div>
        </div>
        <div class="block md:hidden fixed right-8 top-8 cursor-pointer">
            <img :src="MenuLogo" alt="Display menu" class="w-8"/>
        </div>
    </div>
</template>

<script setup>
//import logo
import PorscheLogo from '../assets/porsche_logo.png';
import MenuLogo from '../assets/menu.png';

const menu = [{
    title:'Brank',
    link:'',
},
{title:'718',
link:''
},
{
    title:'911',
    link:'',
},
{
    title:'Taycan',
    link:'',
},
{
    title:'Macan',
    link:'',
},
{
    title:'Panamera',
    link:'',
},
{
    title:'Cayanne',
    link:'',
}]

const openLink=(link)=>{
      window.open(link)
}

</script>