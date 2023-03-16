<template>
<v-card elevation="7" class="product-card">
    <img :src="image" alt="paris" class="product-card-image">
    <v-card-title>  {{ title }}  </v-card-title>

    <v-card-subtitle>  {{ subtitle }}  </v-card-subtitle>

    <div class="product-card-more">
        <v-btn @click="navigattopage">
            see more
        </v-btn>
        <span>
            {{ price }} $
        </span>
    </div>
    
</v-card>
        
    
</template>
<script>


export default{
name:'ProductCard',
props:{
    image:{
        type: String,
        default:''
    },
    title:{
        type: String,
        default:''
    },
    subtitle:{
        type: String,
        default:''
    },
    price:{
        type: Number,
        default:0
    },
    methods:{
                navigateToPage(){
                    navigateToPage
                },
},
        }
}
</script>