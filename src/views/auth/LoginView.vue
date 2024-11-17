<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import LoginForm from '@/components/auth/LoginForm.vue'
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
                <p>Please Login</p>
              </v-card-title>

              <v-card-text class="bg-surface-light pt-4">
                <LoginForm></LoginForm>
                <v-divider class="my-5"></v-divider>
                <h5 class="text-center">
                  Don't have an account? <RouterLink to="/register"> register</RouterLink>
                </h5>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </template>
  </AppLayout>
</template>
