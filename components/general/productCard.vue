<template>
<v-card elevation="7" class="product-card">
    <img :src="image" alt="paris" class="product-card-image" >
    <v-card-title>  {{ title }}  </v-card-title>

    <v-card-subtitle>  {{ subtitle }}  </v-card-subtitle>

    <div class="product-card-more">
        
        <v-btn @click="navigateToPage">
            see more
        </v-btn>
        <span>
            {{ price }} $
        </span>
    </div>
    
    <div class="text-center" >
<v-rating
  
  bg-color="orange-lighten-1"
  color="red"
></v-rating>
</div>
<div class="product-card-more">
    <v-btn @click="navigatetoticket">
        Book a Ticket
    </v-btn>
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
},

methods:{
    navigateToPage(){
        this.$router.push(`/products-overview/${this.title}`)
    },
    navigatetoticket(){
        this.$router.push(`/ticket/`)
        
    }   

  }        }

</script>