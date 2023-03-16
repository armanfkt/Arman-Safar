<template>
  <v-app>
    <v-app-bar color="primary" max-height="64px">
     <span>
      Arman Safar
     </span>
    </v-app-bar>
     
     <v-container>
      <nuxt />
     </v-container>
     
     <v-footer color="primary">
      <div >
       <p class="white--text"> Adress: Tehran, Shariati street, Diagon alley, house.NO. 85 </p>
       <p class="white--text"> Phone: +98 9123454345</p>
       <p class="white--text"> Fax: +98 21 65746553</p>
      </div>
     </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',

}
</script>
