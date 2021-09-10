<template>
    <div>
        <Nav />
        <MainHeader />

    </div>
</template>

<script>
import {Nav, MainHeader,Presentation} from '../components';
import {reactive, toRefs} from 'vue'

export default {
    components:{
     Nav, 
     MainHeader,
     Presentation,
    },
    setup(){
        let data= reactive({
            presentations:[{
                left:true,
                col1:{
                    backgroundColor:'customBlue',
                    title:'Future is now',
                    subtitle:'Taycan concept',
                    description:'The soul has namy aspects. It is variable and constantly changing. When viewing the Porsche Taycan, it reveals itself by a smile that express total delight. Or by the urge for freedom at the wheel of the new Taycan Cross Turismo that holds its ground, even away from everyday life.'
                },
                col2:{
                    
                }
            }]
        })
            return{
        ...toRefs(data)
    }
    },

}

</script>