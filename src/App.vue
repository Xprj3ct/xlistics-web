<template>
  <v-app class="ovv" app dark flat :style="{ background: $vuetify.theme.themes.dark.background }">
    <v-main>
      <NavBar/>
      <v-container fluid>
          <v-row >
            <v-col cols="6">
              <v-img class="imp" src="phone.png" contain  max-height="300"></v-img>
            </v-col>
            <v-col cols="6">
                <h5 class="white--text font-weight-thin">Hello There,</h5>
                <h3 class="orange--text font-weight-black text-darken-4 top" max-width="100"> Easy Living with Logistics/Proxy services.</h3>
                <h6 class="white--text font-weight-regular text-center" >We make it easy for you to manage your shipments 
                  and logistics online, From finding a courier/proxy that is ready to be at your service anytime anywhere and on time.</h6>
                  <v-btn class="br " max-height="80" max-width="120" color="#111111"  ><v-img elevation="20" max-height="80" max-width="100" src="ga.png" /> </v-btn>
            </v-col>
            <WaitList class="top"/>
            
            
          </v-row >
      </v-container>  
             
              <AccorDion class="first"/>
             
    </v-main>
    <FooTer/>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import WaitList from "./components/WaitList.vue";
import FooTer from "./components/FooTer.vue";
import AccorDion from "./components/AccorDion.vue";



export default {
    name: "App",

    data: () => ({
     
    }),
    components: {
    NavBar,
    WaitList,
    FooTer,
    AccorDion
}
};
</script>

<style>
.top{
  margin-top: 10px ;
  width: 100%;
}
.imp{
  margin-top: 30px;
}
.br{
  margin-top: 10px; 
}
.first{
  width: 100%;
  
  padding: 2rem;
}

.ovv{
  width: 100%;
}

</style>