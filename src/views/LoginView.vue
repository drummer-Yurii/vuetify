<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  email: '',
  password: '',
  remember: false
})

const submit = () => {
  alert(JSON.stringify(form.value))
}
</script>

<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="4">
        <v-card class="pa-4">
          <v-card-title class="text-center">Login Here</v-card-title>
          <v-card-item>
            <v-form @submit.prevent="submit">
              <v-text-field
                type="email"
                variant="solo"
                prepend-inner-icon="mdi-email"
                v-model="form.email"
                label="Email"
              ></v-text-field>
              <v-text-field
                type="password"
                variant="solo"
                prepend-inner-icon="mdi-key"
                v-model="form.password"
                label="Password"
              ></v-text-field>
              <v-checkbox
                v-model="form.remember"
                color="red"
                label="Remember Me"
                hide-details
              ></v-checkbox>
              <v-btn color="red-darken-1" class="mt-2" type="submit" block>Submit</v-btn>
            </v-form>
          </v-card-item>
          <v-card-action>
            <div class="mx-4">
              <v-btn block to="/register"> Register </v-btn>
            </div>
          </v-card-action>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
