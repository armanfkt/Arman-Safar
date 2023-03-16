<template>
    <v-row>
        <v-col v-for ="tour in tours" :key="tour.title" cols="12" sm="3">
            <product-card :image="tour.image" :title="tour.title"  :subtitle="tour.subtitle" :price="tour.price" />

        </v-col>
    </v-row>
</template>

<script>
import ProductCard from "@/components/general/productCard.vue"

export default{
    name:'Homepage',
    components:{
        ProductCard
    },
    data(){
        return{
            tours:[
                {
                    image: "/cities/paris.jpg",
                    title: "Paris Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:900,
                },
                {
                    image: "/cities/paris.jpg",
                    title: "Rome Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:850,
                },
                {
                    image: "/cities/paris.jpg",
                    title: "Berlin Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:456,
                },
                {
                    image: "/cities/paris.jpg",
                    title: "Milan Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:590,
                },
                {
                    image: "/cities/paris.jpg",
                    title: "Barcelon Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:900,
                },
                {
                    image: "/cities/paris.jpg",
                    title: "London Tour",
                    subtitle:" Best Days ever in Paris with the best tour of Europe!",
                    price:1200,
                },
            ]
        }
    },
}
</script>