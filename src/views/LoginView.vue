<script setup>
import { useForm, useField } from "vee-validate";
import { loginSchema as validationSchema } from "../validation/loginSchema";

const { handleSubmit } = useForm({ validationSchema });
const { value: email, errorMessage: errorEmail } = useField("email");
const { value: password, errorMessage: errorPass } = useField("password");

// console.log(errorEmail);

const submit = handleSubmit((values) => {
  console.log(values);
  if (values) {
    console.log("Iniciando sesion");
  } else {
    console.log("Por favor ingresar todos los campos");
  }
});
</script>
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
        v-model="email"
        :error-message="errorEmail"
      ></v-text-field>
      <v-text-field
        type="password"
        name="password"
        label="Password"
        bg-color="blue-grey-lighten-5"
        v-model="password"
      ></v-text-field>
      <v-btn @click="submit" color="pink-accent-3" block>
        Iniciar Sesión
      </v-btn>
    </v-form>
  </v-card>
</template>
