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
      <v-card-title >
        <strong class="caption font-weight-thin">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-2"
          dark
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

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
        'mdi-instagram',
      ],
    }),
  }
</script>
<style>
.vvv{
    width: 100%;
}
</style>