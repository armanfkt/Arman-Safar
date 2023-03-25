<template>
    <v-container id="container" >
        <div class="col3">

            <v-row>
                
                <v-col cols="12" sm="6">
                    
                    <h2 >FirstName :</h2>
                    <input class="input"> {{ text }}
                </v-col>
                <v-col cols="12" sm="6">
                    
                    <h2 >Last Name :</h2>
                    <input class="input"> {{ text }}
                </v-col>
            </v-row>
        </div>
        <div class="col3">

            <v-row>
                
                <v-col cols="12" sm="6">
                    
                    <h2 >NationalCode :</h2>
                    <input class="input" type="number" :maxlength="10" value="0022040099"> {{ text }}
                </v-col>
                <v-col cols="12" sm="6">
                    
                    <h2 >BirthDay :</h2>
                    <input class="input" type="date" > {{ text }}
                </v-col>
            </v-row>
        </div>
        <div>

            <v-row>
                
                <v-col id="col3" cols="12" sm="12">
                    <div>
                        <v-autocomplete 
      clearable
      label="Select your city"
      :items="['Berlin', 'Rome', 'Barcelon', 'Paris', 'London', 'Milan', 'Munich', 'Denver']"
    ></v-autocomplete>
                    </div>
                    <div id="div5">

                        
                        <div id="div4" >
                            <label id="lable" for="select">flightType :</label>
                            <select  id="select" value="select"  v-model="flightType">
                                
                            <option value="One-way Flight" >One-way Flight</option>
                            <option >Return Flight</option>
                        </select>
                    </div> 
                    
                    <div    >
                        <input class="date" type="date" v-model="departureDate">
                        <input class="date" type="date" v-model="returnDate" >
                        <v-btn id="btn">reservation</v-btn>  
                            
                            
                            
                    </div>
                    
                </div>
                </v-col>
                <v-col>
                    <v-btn @click="navigatetoHomepage">
                        Hompage
                    </v-btn>
                </v-col>
            </v-row>
        </div>
        
</v-container>
</template>

<script>
export default{
    name:"Ticket",
    
    data() {
        return{
            ticket:[
                {text: 'Edit me',
                checked: true,
                checkedNames: ['Jack'],
                picked: 'One',
                selected: 'A',
            multiSelected: ['A']}

        ]
    }
},

methods:{
    navigatetoHomepage(){
     this.$router.push("/products-overview/")
    }
},
}






</script>