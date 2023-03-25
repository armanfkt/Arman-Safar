<template>
    <v-container>
        <v-row>
            <v-col cols="12" sm="6">
                <img :src="city.image" alt="city.image">
            </v-col>
            
                                <v-col cols="12" sm="6">
                                    
                                    <h1> {{ city.title }} </h1>
                                    
                                    </v-col>
        
        </v-row>
        <v-row>
            <v-col cols="12" sm="4">
                <h3>
                            rate: {{ city.rate }}
                        </h3>
            </v-col>
            <v-col cols="12" sm="4">
                <h3>description: {{ city.description }}</h3>
            </v-col>
            <v-col>
                    <v-btn @click="navigatetoHomepage">
                        Hompage
                    </v-btn>
                </v-col>
        </v-row>
    </v-container>

</template>

<script>
    export default{
        name:"SingleProduct",

        data(){
            return{
                cityData:[
                    {
                        title: 'Paris',
                        image: '/cities/paris.jpg',
                        description: 'Paris Tour',
                        rate: 3.5
                    },
                    {
                        title: 'Rome',
                        image: '/cities/rome.jpg',
                        description: 'Best Rome tour ever',
                        rate: 4
                    },
                    {
                        title: 'Berlin',
                        image: '/cities/Berlin.jpg',
                        description: 'Wonderful Traveling to berlin',
                        rate: 4.6
                    },
                    {
                        title: 'Milan',
                        image: '/cities/milan.jpg',
                        description: 'Best Milan tour ever',
                        rate: 4.2
                    },
                    {
                        title: 'Barcelon',
                        image: '/cities/barcalon.jpg',
                        description: 'city of football',
                        rate: 5
                    },
                    {
                        title: 'London',
                        image: '/cities/london.jpg',
                        description: 'Enjoy Traveling to london with us ',
                        rate: '4'
                    },
                    {
                        title: 'Munich',
                        image: '/cities/munich.jpg',
                        description: 'Amazing Nights in munich   ',
                        rate: '3.9'
                    },
                    {
                        title: 'Denver',
                        image: '/cities/denver.jpg',
                        description: 'Exellent Weekend in denver',
                        rate: '2'
                    },
                ]
            }
        },
        methods:{
    navigatetoHomepage(){
     this.$router.push("/products-overview/")
    }
},

        computed:{
            city(){
               const cityNameFromURL = this.$route.params.city

               const singleTour = this.cityData.find((city) => (
                 cityNameFromURL.includes(city.title) 
               ))
               
               return singleTour
            }
        }
    }
</script>