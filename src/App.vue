<template>
  <v-app>
    <v-toolbar app>

    </v-toolbar>
    <v-content>
      <br>
      <NewMessages/>
      <br>
      <Messages/>
    </v-content>
  </v-app>
</template>

<script>
import Messages from './components/Messages'
import NewMessage from './components/NewMessages'

export default {
  name: 'App',
  components: {
    Messages, NewMessage
  }
}
</script>


