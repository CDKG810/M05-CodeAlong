<template>
      <v-flex sm8 offset-sm2>
         <v-card>
            <v-toolbar dark>
               <v-toolbar-title>Messages               </v-toolbar-title>
            </v-toolbar>
         
            <v-list>
               <v-list-item v-for="(message, index) in messages" :key="index">
                  <v-list-item-content>
                     <v-list-item-title>{{ message }}</v-list-item-title>
                  </v-list-item-content>
               </v-list-item>
            </v-list>
         </v-card>
      </v-flex>
 </template>
 <script>
  
import axios from "axios";
import store from "../store.js";
    
   

    export default {
       data() {
          return {
             messages: store.state.messages
          };
       },
       async created() {
            this.messages = (await axios.get("http://localhost:3000/messages")).data;
       }
    };
 </script>
