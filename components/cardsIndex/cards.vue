<template>
<v-row class="mt-4">
  <v-col cols="4" v-for="(item, i) in items" :key="i">
    <v-card class="mx-auto mb-4" max-width="344" outlined elevation="13">
        <v-list-item three-line>
          <v-list-item-content>
            <div class="overline mb-4">{{ item.category }}</div>
            <v-list-item-title class="headline mb-1">
              {{ item.name }}
            </v-list-item-title>
            <v-list-item-subtitle>{{ item.description }}</v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-avatar tile size="80" color="grey">
            <v-img
              :lazy-src="`https://${item.img}`"
              max-height="150"
              max-width="250"
              :src="`https://${item.img}`"
            ></v-img>
          </v-list-item-avatar>
        </v-list-item>
        <v-card-actions>
          <v-btn outlined rounded text :to="item.to">{{item.botton}}</v-btn>
        </v-card-actions>
    </v-card>
  </v-col>
</v-row>
</template>

<script>
import cardsIndex from '~/assets/json/cardsIndex.json'

export default {
  data() {
    return {
      items: cardsIndex,
    }
  },
}
</script>

<style scoped>
.theme--dark .v-card, .v-btn {
  border: 1px rgb(230, 180, 230) !important;
  border-style: dashed double !important;
}
</style>