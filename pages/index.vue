<template>
  <v-layout row wrap justify-center align-center>
    <v-flex sm6 md6>
      <div class="display-3">
        Welcome to yuuu&#39;s Portfolio.
      </div>
      <v-divider class="my-3"></v-divider>
      <div class="title mb-3">Check out my profile!</div>
      <v-layout justify-center>
        <v-btn color="secondary" large to="/profile">profile</v-btn>
      </v-layout>
    </v-flex>
    <v-flex sm6 md6>
      <v-img src="/icon.png" aspect-ratio="1" />
    </v-flex>
  </v-layout>
</template>
