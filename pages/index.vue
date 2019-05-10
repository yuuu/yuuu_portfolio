<template>
  <v-layout row wrap justify-center align-center>
    <v-flex sm6 md6>
      <div class="text-xs-center display-3">
        Welcome to yuuu's Portfolio.
      </div>
      <v-layout justify-center>
        <v-btn color="secondary" large to="/profile">profile</v-btn>
      </v-layout>
    </v-flex>
    <v-flex sm6 md6>
      <v-img src="/logo.png" aspect-ratio="1" />
    </v-flex>
  </v-layout>
</template>
