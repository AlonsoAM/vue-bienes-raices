<script setup></script>
<template>
  <v-card flat max-width="600" class="mx-auto my-10">
    <v-card-title primary-title class="text-center text-h4 font-weight-bold">
      Iniciar Sesión
    </v-card-title>
    <v-card-subtitle class="text-center text-h5 font-weight-bold">
      Iniciar sesión con tu cuenta
    </v-card-subtitle>
    <v-form class="mt-5">
      <v-text-field
        type="email"
        name="email"
        label="Email"
        bg-color="blue-grey-lighten-5"
      ></v-text-field>
      <v-text-field
        type="password"
        name="password"
        label="Password"
        bg-color="blue-grey-lighten-5"
      ></v-text-field>
      <v-btn color="pink-accent-3" block> Iniciar Sesión </v-btn>
    </v-form>
  </v-card>
</template>
