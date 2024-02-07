<script>
  export default {
    data: () => ({
      items: [
        { title: 'Example 1' },
        { title: 'Example 2' },
        { title: 'Example 3' },
        { title: 'Example 4' },
      ],
    }),
  }
</script>

<template>
  <v-container fluid class="">
    <v-app-bar :elevation="0">
      <v-row>
        <v-col class="text-center">
          <h1 class="text-primary">bonsai</h1>
        </v-col>
        <v-col class="d-flex justify-space-around align-center">
          <!-- DROP DOWN MENUS -->
          <v-menu>
            <template v-slot:activator="{ props }">
              <v-btn append-icon="mdi-chevron-down" color="grey" v-bind="props" class="text-capitalize text-subtitle-1">Product</v-btn>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index" :value="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
          <v-menu>
            <template v-slot:activator="{ props }">
              <v-btn append-icon="mdi-chevron-down" color="grey" v-bind="props" class="text-capitalize text-subtitle-1">Templates</v-btn>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index" :value="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>

          <!-- BUTTONS -->
          <v-btn class="text-grey text-capitalize text-subtitle-1">Pricing</v-btn>
          <v-btn class="text-grey text-capitalize text-subtitle-1">Reviews</v-btn>
        </v-col>
        <v-col class="d-flex align-center justify-center">
          <v-btn class="text-primary mr-3 px-5 log-in-btn">LOG IN</v-btn>
          <v-btn class="bg-primary px-8 font-weight-bold">START FREE</v-btn>
        </v-col>
      </v-row>
    </v-app-bar>
  </v-container>
</template>

<style>
.log-in-btn{
  border: 3px solid #00b289;
}
</style>
