<template>
        <Homepage/>
</template>

<script>
import Homepage from '@/components/Homepage/Homepage';

export default{
    name:"Index",
    
    components:{
        Homepage
    },
    
    middleware({redirect}){
        redirect('/products-overview')
    }

}
</script>