<template>
    <div class="Stats bg-cover bg-no-repeat bg-bottom relative lg:pt-32 py-8" :style="`background-image:url(${Porsche2020});min-height: 300px; margin-bottom: 300px; background-position: center bottom -6rem;`">
        <div class="w-full h-full bg-customBlue opacity-75 absolute z-0 top-0 left-0"  />
        <div class="Stats-Components flex flex-col lg:flex-row items-center justify-between z-50 gap-y-5 lg:gap-y-0 relative lg:absolute w-full p-8">
         <StatsCard v-for="card,index in cards" :key="index" :content="card" />
        </div>     
    </div>
</template>

<script>
import {reactive, toRefs} from 'vue'
import StatsCard from '../components/elements/stats/StatsCard.vue';
import Porsche2020 from '../assets/2020-porsche.jpeg';
import Speed from '../assets/speed.png';
import Weight from '../assets/weight.png';
import Plug from '../assets/rounded-plug.png';
import Size from '../assets/dimensions.png';

export default {
    components: {
        StatsCard
    },

  setup(){
    const data = reactive({
        Porsche2020,
        cards:[
            {
    imgSrc:Plug,
    title:'Range',
    description:'301 miles<br>(25.4 - 24.4 kwh/100 miles)',
    animated:'fade-right'
},
{
    imgSrc:Speed,
    title:'Speed',
    description:'5.4s<br>0 - 100km',
    animated:'fade-up',
},
{
    imgSrc:Size,
    title:'Size',
    description:'L: 4.963 mm<br>W: 1,966 mm<br>H: 1,395 mm',
    animated:'fade-down'
},
{
    imgSrc:Weight,
    title:'Weight',
    description:'2,050 kg',
    animated:'fade-left'
}
        ]
    })

    return {
    ...toRefs(data),
}

  }

}

</script>

<style>
.Stats{

}
</style>

