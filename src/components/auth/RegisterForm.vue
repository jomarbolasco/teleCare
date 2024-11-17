<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field label="First name" variant="outlined"></v-text-field>

    <v-text-field label="Last name" variant="outlined"></v-text-field>

    <v-text-field label="Email" variant="outlined"></v-text-field>

    <v-text-field label="Password" type="password" variant="outlined"></v-text-field>

    <v-text-field label="Password Confirmation" type="password" variant="outlined"></v-text-field>

    <v-btn class="mt-2" type="submit" block prepend-icon="mdi-account-plus">Register</v-btn>
  </v-form>
</template>
