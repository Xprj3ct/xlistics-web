<template>
  <div class="avv">
    <v-img src="faq.png" contain max-height="100"  max-width="300"/>

    <v-expansion-panels>
      <v-expansion-panel class="mt-2">
        <v-expansion-panel-header color=black class="caption font-weight-regular white--text">
          What is xlistics ?
          <template v-slot:actions>
            <v-icon color="error">
              mdi-plus
            </v-icon>
          </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content color=black class="caption font-weight-regular white--text">
            xlistics is a game changing logistics and proxy app
            That will be building the bridge between users to proxy/courier
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel class="mt-2">
        <v-expansion-panel-header color=black class="caption font-weight-regular white--text">
          Who is a courier/proxy?
          <template v-slot:actions>
            <v-icon color="error">
              mdi-plus
            </v-icon>
          </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content color=black class="caption font-weight-regular white--text">
            a courier is a person that  transports commercial packages and documents.
            Proxy : a person authorized to act on behalf of another. example : I sent a proxy to help me purchase a bag in dubai.
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel class="mt-2">
        <v-expansion-panel-header color=black class="caption font-weight-regular white--text">
          How can I trust couriers/proxy on the Xlistics app ?
          <template v-slot:actions>
            <v-icon color="error">
              mdi-plus
            </v-icon>
          </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content color=black class="caption font-weight-regular white--text">
          All couriers/proxy are verified legally by the government and the company.
            If you are to come into issue please do well to contact our help system 
            For more details check Terms and condition
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel class="mt-2">
        <v-expansion-panel-header color=black class="caption font-weight-regular white--text">
          How will I pay for the services ?
          <template v-slot:actions>
            <v-icon color="error">
              mdi-plus
            </v-icon>
          </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content color=black class="caption font-weight-regular white--text">
          Payments for services can be made on the xlistics App and also in hand with courier/proxy
        </v-expansion-panel-content>
      </v-expansion-panel>

      <v-expansion-panel class="mt-2">
        <v-expansion-panel-header color=black class="caption font-weight-regular white--text">
          Xlistics reach?
          <template v-slot:actions>
            <v-icon color="error">
              mdi-plus
            </v-icon>
          </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content color=black class="caption font-weight-regular white--text">
            We are not restricted to a pacticular zone or city, base on database and availability of courier/proxy
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<style>
.avv{
    width: 100%;
}
</style>