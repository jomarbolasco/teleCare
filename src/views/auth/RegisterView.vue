<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import RegisterForm from '@/components/auth/RegisterForm.vue'

import { useDisplay } from 'vuetify'

const { mobile } = useDisplay()
</script>

<template>
  <AppLayout>
    <template #content>
      <v-container fluid>
        <v-row>
          <v-col cols="12" md="6" class="mx-auto">
            <v-card class="mx-auto" elevation="24">
              <v-card-title>
                <v-img
                  class="mx-auto"
                  src="/public/images/telecare logo.png"
                  :width="mobile ? '75%' : '25%'"
                ></v-img>
                <h2>teleCARE</h2>
                <p>Please Sign-up</p>
              </v-card-title>

              <v-card-text class="bg-surface-light pt-4">
                <RegisterForm></RegisterForm>
                <v-divider class="my-5"></v-divider>
                <h5 class="text-center">
                  Already have an account? <RouterLink to="/login"> Login</RouterLink>
                </h5></v-card-text
              >
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </template>
  </AppLayout>
</template>
