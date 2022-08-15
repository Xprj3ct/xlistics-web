<template>
<div >
    <v-img src="about.png" class="mx-5" contain max-height="100"  max-width="300"/>
    <v-parallax
    height="1500"
    src="bgg.png"
  >
        <v-row elevation="16">
            <v-col col="6">
                <v-img src="1.png" transition="slide-x-transition" contain  max-height="300"/>
            </v-col>
             <v-col col="6">
                <v-img  src="2.png" transition="slide-x-reverse-transition" contain  max-height="250"/>
            </v-col>
        </v-row>
        <v-row elevation="16">
             <v-col col="6">
                <v-img transition="slide-x-transition" src="3.png" contain  max-height="300"/>
            </v-col>
             <v-col col="6">
                <v-img src="4.png" contain  max-height="250"/>
            </v-col>
             <v-col col="6">
                <v-img src="5.png" contain  max-height="300"/>
            </v-col>
        </v-row>
    </v-parallax>
</div>
</template>

<script>

</script>

<style>

</style>