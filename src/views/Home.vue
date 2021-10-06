<template>
    <div>
        <Nav />
        <MainHeader />
        <Presentation v-for="presentation in presentations" :key="presentation" :content="presentation" class="mb-16"/>
        <Stats />
    </div>
</template>

<script>
import {Nav, MainHeader,Presentation,Stats} from '../components';
import {reactive, toRefs} from 'vue';
import PorscheCockpit from '../assets/porsche-cockpit.png';
import PorscheMotorsG5 from '../assets/g-motor5.jpeg';

export default {
    components:{
     Nav, 
     MainHeader,
     Presentation,
     Stats
    },
    setup(){
        let data= reactive({
            presentations:[
                {
                left:false,
                columns:[{
                    backgroundColor:'customBlue',
                    title:'Future is now',
                    subtitle:'Taycan concept',
                    description:'The soul has namy aspects. It is variable and constantly changing. When viewing the Porsche Taycan, it reveals itself by a smile that express total delight. Or by the urge for freedom at the wheel of the new Taycan Cross Turismo that holds its ground, even away from everyday life.'
                },{
                imgSrc:PorscheCockpit,
                }
                ],

            },
            {
                left:true,
                columns:[{
                    backgroundColor:'white',
                    button:{
                        backgroundColor:'customBlue',
                        text: 'Book a test'
                    },
                    title:'our first electric sportcar',
                    subtitle:'Taycan concept',
                    description:'The soul has namy aspects. It is variable and constantly changing. When viewing the Porsche Taycan, it reveals itself by a smile that express total delight. Or by the urge for freedom at the wheel of the new Taycan Cross Turismo that holds its ground, even away from everyday life.'
                },{
                imgSrc:PorscheMotorsG5,
                contain:true
                }
                ],

            }
            ]
        })
            return{
        ...toRefs(data)
    }
    },

}

</script>