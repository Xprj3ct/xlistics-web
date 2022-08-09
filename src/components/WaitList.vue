<template>
    <v-container fluid >
    <v-row >
        <v-btn 
        color="#111111"
        elevation="10"
        fab block @click="dialog = !dialog"
        ><v-img src="waitlist.png" max-height="200" max-width="200"/>
        </v-btn>
    <v-dialog
        v-model="dialog"
          max-width="500px"
        >
    <v-card>
        <v-card-text color=black >
            <h4 class="mt-4">Be the first to Know</h4   >
            <v-text-field label="Full name"></v-text-field>
            <v-text-field label="Email"></v-text-field>
            <v-text-field label="Phone No"></v-text-field>
            <v-select 
          :items="items"
          label="Preferred Device"
        ></v-select>
            <!-- <small class="white--text">* This doesn't actually save.</small> -->
            </v-card-text>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn
                text
                color="primary"
                @click="dialog = false"
              >
                Submit
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        items: ['ANDROID', 'IOS'],
        
        dialog: false,
        
    })
}
</script>

<style>

</style>