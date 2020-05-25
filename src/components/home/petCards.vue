<template>
  <v-container fluid>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
        >
          <v-card color="#1e3c41" width="160px" >
            <v-img :src="card.src" class="white--text align-end" cover height="170px" width="160px">  
            </v-img>
            <v-card-actions class="actionsCard">
              <v-spacer></v-spacer>
              <v-card-title  class="white--text" v-text="card.title"></v-card-title>
              <v-spacer></v-spacer>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      </v-container>
</template>

<script>
export default {
    
    data: () => ({
      cards: [
        { title: 'Frida', src: 'https://cdn.discordapp.com/attachments/682040046072758387/714277798805635072/Frida.jpg', flex: 6 },
        { title: 'Jamgi', src: 'https://cdn.discordapp.com/attachments/682040046072758387/714278711368876083/pug-dog-isolated-white-background_127657-22419.jpg', flex: 6 },
        { title: 'Nala', src: 'https://media.discordapp.net/attachments/682040046072758387/714278674630967306/48-484516_dog-clipart-transparent-background-dog-cat-white-background.png', flex: 6 },
      ],
    }),
  
}
</script>

<style>
 .actionsCard{
     height: 45px;
 }
 .mascota{
   width: 200px;
   height: 72.64px;
   padding: 0px;
   background-size: contain;
   /* padding-top: 40px; */
   background-image: url('../assets/logoPetPatrol.png');
}
</style>