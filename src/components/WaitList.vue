
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
            <v-text-field v-model="waitlist.fullname" label="Full name"></v-text-field>
            <v-text-field v-model="waitlist.email" label="Email"></v-text-field>
            <v-text-field v-model="waitlist.phone" label="Phone No"></v-text-field>
            <v-select 
          :items="items"
          label="Preferred Device"
          v-model="waitlist.device"
        ></v-select>
            <!-- <small class="white--text">* This doesn't actually save.</small> -->
            </v-card-text>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn
                text
                color="primary"
                v-on:click="handleWait"
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

import { addDoc, collection, doc } from 'firebase/firestore'
import db from '../firebase'

 const handleWait = async (waitList) => {
    console.log(waitList)

        try {

            await addDoc(collection(db, `waitList`), {
                name: waitList.fullname,
                email: waitList.email,
                phone: waitList.phone,
                os: waitList.device

            })

            setName("")
            setEmail("")
            setPhone("")
            setOs("")


        } catch (err) {
            console.log(err)
        }
    }

export default {
    data: () => ({
        items: ['ANDROID', 'IOS'],
        dialog: false,
        waitlist:{
          fullname:"",
          email:"",
          device:""
          phone:""
        }
        
    }),
    methods: {
      handleWait(this.waitlist)
    }

}
</script>

<style>

</style>