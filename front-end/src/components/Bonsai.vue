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

    <!-- NAVBAR / HEADER -->

    <v-app-bar :elevation="0">
      <v-row>
        <v-col class="text-center">
          <h1 class="text-primary ml-n16">bonsai</h1>
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

    <!-- PLANS AND PRICING -->

    <v-container class="mt-16 px-16">
      <v-row>
        <v-col>
          <h2 class="text-h4 my-font-serif">Plans & Pricing</h2>
        </v-col>
        <v-col>
          <h5 class="text-end mb-3 text-primary">2 MONTHS FREE!</h5>
          <div class="d-flex align-center justify-end">
            <h3 class="font-weight-regular">MONTHLY</h3>
            <label class="switch mx-5">
              <input type="checkbox">
              <span class="slider round"></span>
            </label>
            <h3 class="text-grey font-weight-regular">YEARLY</h3>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<style>
.log-in-btn{
  border: 3px solid #00b289;
}

.my-font-serif{
  font-family: serif;
}


/* The switch - the box around the slider */
.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #00b289;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #00b289;
}

input:focus + .slider {
  box-shadow: 0 0 1px #00b289;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
