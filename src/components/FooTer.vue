<template>
  <v-footer class="vvv"
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
     <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon center
          href="https://twitter.com/Xlistics"
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. ontes, nascetur ridiculus mus.
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="py-2 caption font-weight-thin white--text text-center">
        {{ new Date().getFullYear() }} — <strong class="caption font-weight-thin">xlistics</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        
        'mdi-twitter',
        
      ],
    }),
  }
</script>
<style>
.vvv{
    width: 100%;
}
</style>