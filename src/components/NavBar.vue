<template>
    <v-app-bar app color="#111111" dark flat class="px-8 nvv">
        <v-btn icon>
        <v-img
          :src="require('../assets/png.png')"
          class=" my-8"
          contain
          height="24"
        />
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text @click="scroll('About')">About</v-btn>
        <v-btn text @click="scroll('FAQ')">FAQ</v-btn>
    </v-app-bar>
</template>

<script>
export default {
   methods: {
    scroll (refName) {
        const element = document.getElementById(refName);
        element.scrollIntoView({behavior: 'smooth'});
    }
   }

}
</script>

<style>
.nvv{
    width: 100%;
}
</style>