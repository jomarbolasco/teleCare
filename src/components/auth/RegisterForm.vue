<script setup>
import {
  requiredValidator,
  emailValidator,
  passwordValidator,
  confirmedValidator,
} from '../utils/validators'
import { ref } from 'vue'

const refVForm = ref()

const formDataDefault = {
  firstname: '',
  lastname: '',
  email: '',
  password: '',
  password_confirmation: '',
}

const formData = ref({
  ...formDataDefault,
})

const onSubmit = () => {
  alert(formData.value.email)
}

const onFormSubmit = () => {
  refVForm.value?.validate().then(({ valid }) => {
    if (valid) onSubmit()
  })
}
</script>

<template>
  <v-form ref="refVForm" @submit.prevent="onFormSubmit">
    <v-text-field
      v-model="formData.firstname"
      label="First name"
      variant="outlined"
      :rules="[requiredValidator]"
    ></v-text-field>

    <v-text-field
      v-model="formData.lastname"
      label="Last name"
      variant="outlined"
      :rules="[requiredValidator]"
    ></v-text-field>

    <v-text-field
      v-model="formData.email"
      label="Email"
      variant="outlined"
      :rules="[requiredValidator, emailValidator]"
    ></v-text-field>

    <v-text-field
      v-model="formData.password"
      label="Password"
      type="password"
      variant="outlined"
      :rules="[requiredValidator, passwordValidator]"
    ></v-text-field>

    <v-text-field
      v-model="formData.password_confirmation"
      label="Password Confirmation"
      type="password"
      variant="outlined"
      :rules="[requiredValidator, confirmedValidator]"
    ></v-text-field>

    <v-btn class="mt-2" type="submit" block prepend-icon="mdi-account-plus">Register</v-btn>
  </v-form>
</template>
