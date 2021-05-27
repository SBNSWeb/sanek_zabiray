<template>

  <v-app :class="{ 'pa-3': $vuetify.breakpoint.smAndUp }" :dark="darkTheme" id="inspire">
    <v-container>
      <v-layout wrap>
        <v-flex sm12 md6 offset-md3>
          <v-card elevation="4" light tag="section">
            <v-card-title>
              <v-layout align-center justify-space-between>
                <h3 class="headline">
                  {{ platformName }}
                </h3>
                <v-flex>
                  <!--картинку нвхуй-->
                   
                  <v-img :alt="platformName" class="ml-3" contain height="48px" position="center right" src="logo-delta.png"></v-img>
                  
                </v-flex>
              </v-layout>
            </v-card-title>
            <v-divider></v-divider>
            <v-card-text>
              <!--войди туда сюда-->
              <p>Введите данные вашей команды:</p>
              <v-form>

                <v-text-field
                              outline
                              label="Имя команды"
                              type="text"
                              v-model="comname"></v-text-field>
                <v-text-field
                              outline
                              hide-details
                              label="Дивизион"
                              type="value"
                              v-model="comdiv"></v-text-field>
                
                <v-text-field
                              outline
                              hide-details
                              label="Описание"
                              type="text"
                              v-model="comdesc"></v-text-field>

              </v-form>
              
            </v-card-text>

            <v-card-actions :class="{ 'pa-3': $vuetify.breakpoint.smAndUp }">
              
              <v-spacer></v-spacer>
              <v-btn color="info" :large="$vuetify.breakpoint.smAndUp">
                <v-icon left>Go</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex sm12 md6 offset-md3>


        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
 export default{}

</script>
  
<style>

</style>
