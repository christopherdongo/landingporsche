<template>
    <div class="Stats bg-cover bg-no-repeat bg-bottom relative" :style="`background-image:url(${Porsche2020}); height:450px;`">
        <div class="w-full h-full bg-customBlue opacity-75 absolute z-0"  />
        <div class="Stats-Components z-50 relative">
         <p class="text-white">{{cards}}</p>
         <StatsCard />
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
},
{
    imgSrc:Speed,
    title:'Speed',
    description:'5.4s<br>0 - 100km',
},
{
    imgSrc:Size,
    title:'Size',
    description:'L: 4.963 mm<br>W: 1,966 mm<br>H: 1,395 mm',
},
{
    imgSrc:Weight,
    title:'Weight',
    description:'2,050 kg',
}
        ]
    })

    return {
    ...toRefs(data),
}

  }

}



</script>


