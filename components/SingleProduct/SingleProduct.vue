<template>
    <v-container>
        <v-row>
            <v-col cols="12" sm="6">
                <img :src="city.image" alt="city.image">
            </v-col>

            <v-col  cols="12" sm="6">
                <v-row>
                    <v-col cols="12" sm="4">
                    
                    </v-col>

                    <v-col cols="12" sm="8">
                        <h1> {{ city.title }} </h1>
                    </v-col>
                </v-row>
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
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                    {
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                    {
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                    {
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                    {
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                    {
                        title: '',
                        image: '',
                        description: '',
                        rate: ''
                    },
                ]
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