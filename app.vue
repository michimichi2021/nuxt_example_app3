<template>
   <v-row class="blue lighten-4 mt-6" justify="center" align-content="center">
    <v-card title="カウンターアプリ" class="mx-auto" justify="center" max-width="300">
      <v-card-item  justify="center" align-content="center">
        <v-list
          :lines="false"
          density="compact"
          nav
        >
          <v-list-item
            color="primary"
          >
          ボタンを押した回数<br/>{{ store.count }}
          </v-list-item>
          <v-list-item
            color="primary"
          >
          ボタンを押した回数×2<br> {{ store.doubleCount }}
          </v-list-item>
        </v-list>
        <v-btn color="primary" @click="store.increment">+</v-btn>
      </v-card-item>
    </v-card>
  </v-row>
</template>
<script setup lang="ts">
import { useCounterStore } from './store/counter'
const store = useCounterStore()
</script>
<style>
</style>