
<template>
    <v-container fluid class="wvv">
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
      <v-form
              ref="form"
              v-model="valid"
                lazy-validation >
        <v-card-text color=black >
            <h4 class="mt-4">Be the first to Know</h4   >
            <v-text-field label="Full name"></v-text-field>
            <v-text-field label="Email"></v-text-field>
            <v-text-field label="Phone No"></v-text-field>
            <v-select 
          :items="items" required
          :rules="[v => !!v || 'Item is required']"
          v-model="select"
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
        </v-form>
          </v-card>
        </v-dialog>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
        items: ['ANDROID', 'IOS'],
        dialog: false,
        
    }),
    methods: {
      validate () {
        this.$refs.form.validate()
      }
    }
}

// export default {
//     data: () => ({
//         items: ['ANDROID', 'IOS'],
//         dialog: false,
//         waitlist:{
//           fullname:"",
//           email:"",
//           device:"",
//           phone:""
//         }
        
//     }),
//     methods: {
//       handleWait(this.waitlist)
//     }

// }
</script>

<style>
.wvv{
    width: 100%;
}
</style>