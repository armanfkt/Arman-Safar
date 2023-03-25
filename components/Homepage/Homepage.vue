<template>
    <v-row>
        <v-col v-for ="tour in tours" :key="tour.title" cols="12" sm="6" md="3" xs="12">
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
                    image: "/cities/rome.jpg",
                    title: "Rome Tour",
                    subtitle:" Enjoy Your weekend in rome with our tour!",
                    price:850,
                },
                {
                    image: "/cities/Berlin.jpg",
                    title: "Berlin Tour",
                    subtitle:" Have a Good days in berlin with our tour!",
                    price:456,
                },
                {
                    image: "/cities/milan.jpg",
                    title: "Milan Tour",
                    subtitle:" The Best trip to themilan cradle of civilization and art!",
                    price:590,
                },
                {
                    image: "/cities/barcalon.jpg",
                    title: "Barcelon Tour",
                    subtitle:" Dream Times in Barcelona with our tour!",
                    price:900,
                },
                {
                    image: "/cities/london.jpg",
                    title: "London Tour",
                    subtitle:" Best Days ever in london with the best tour of Europe!",
                    price:1200,
                },
                {
                    image: "/cities/munich.jpg",
                    title: "munich Tour",
                    subtitle:" A wonderful excursion in the soccer city of germany with a tour!",
                    price:690,
                },
                {
                    image: "/cities/denver.jpg",
                    title: "denver Tour",
                    subtitle:" Best Days ever in denver with the best tour of Europe!",
                    price:1170,
                },
            ]
        }
    },
}
</script>