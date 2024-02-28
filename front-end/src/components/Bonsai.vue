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
  <v-container fluid class="ma-0 pa-0">

    <!-- NAVBAR MOBILE -->

    <v-row class="ma-0 pa-0 d-md-none">
      <v-col cols="4" class="d-flex pa-0 justify-center align-center">
        <v-btn class="elevation-0">
          <v-icon icon="mdi-menu" />
        </v-btn>
      </v-col>
      <v-col cols="4" class="pa-0 text-center">
        <h1 class="text-primary">bonsai</h1>
      </v-col>
      <v-col cols="3" class="pa-0"></v-col>
    </v-row>

    <!-- NAVBAR / HEADER -->

    <v-row class="d-none d-md-block ma-0 pa-0">
      <v-col class="text-center">
        <h1 class="text-primary ml-n16">bonsai</h1>
      </v-col>
      <v-col class="d-flex justify-space-around align-center">
        <!-- DROP DOWN MENUS -->
        <v-menu>
          <template v-slot:activator="{ props }">
            <v-btn append-icon="mdi-chevron-down" v-bind="props" class="text-grey elevation-0 text-capitalize text-subtitle-1">Product</v-btn>
          </template>
          <v-list>
            <v-list-item v-for="(item, index) in items" :key="index" :value="index">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
        <v-menu>
          <template v-slot:activator="{ props }">
            <v-btn append-icon="mdi-chevron-down" v-bind="props" class="text-grey elevation-0 text-capitalize text-subtitle-1">Templates</v-btn>
          </template>
          <v-list>
            <v-list-item v-for="(item, index) in items" :key="index" :value="index">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <!-- BUTTONS -->
        <v-btn class="elevation-0 text-grey text-capitalize text-subtitle-1">Pricing</v-btn>
        <v-btn class="elevation-0 text-grey text-capitalize text-subtitle-1">Reviews</v-btn>
      </v-col>
      <v-col class="d-flex align-center justify-center">
        <v-btn class="text-primary mr-3 px-5 log-in-btn">LOG IN</v-btn>
        <v-btn class="bg-primary px-8 font-weight-bold">START FREE</v-btn>
      </v-col>
    </v-row>

    <!-- PLANS AND PRICING -->

    <v-container class="mt-16 px-16">
      <v-row>
        <v-col>
          <h2 class="text-h4 my-font-serif text-center text-md-left">Plans & Pricing</h2>
        </v-col>
        <v-col>
          <h5 class="text-end mb-3 text-primary">2 MONTHS FREE!</h5>
          <div class="d-flex align-center justify-center justify-md-end">
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

  <!-- PLANS ANS PRICING CARDS -->

  <v-container class="mt-0 mt-md-16 px-10 px-md-16 mx-auto">
    <v-row>
      <v-col>
        <v-card class="pa-10 elevation-5 px-4 px-md-13 w-100">
          <v-card-title class="text-h5">Workflow</v-card-title>
          <div class="d-flex mx-4 my-3">
            <p class="text-h5">$</p>
            <p class="text-h3 d-flex align-end ml-2 font-weight-bold">19 <h6 class="text-subtitle-1 ml-2">/MONTH</h6></p>
          </div>
          <p class="bg-primary mx-4 mt-4 mb-10 divider-custom"></p>
          <ul class="mx-9">
            <li class="my-3">Unlimited Clients & Projects</li>
            <li class="my-3">Proposals</li>
            <li class="my-3">Contracts</li>
            <li class="my-3">Invoicing & Payments</li>
            <li class="my-3">Client CRM</li>
            <li class="my-3">Project Management</li>
            <li class="my-3">Task & Time Tracking</li>
            <li class="my-3">IOS, Android, Chrome & Mac Apps</li>
          </ul>
          <v-btn class="bg-primary w-100 py-8 d-flex align-center mt-12 mb-4">START FREE</v-btn>
        </v-card>
      </v-col>
      <v-col class="d-flex justify-end">
        <v-card class="pa-10 elevation-5 px-4 px-md-13 w-100">
          <v-card-title class="text-h5">Workflow Plus</v-card-title>
          <div class="d-flex mx-4 my-3">
            <p class="text-h5">$</p>
            <p class="text-h3 d-flex align-end ml-2 font-weight-bold">29 <h6 class="text-subtitle-1 ml-2">/MONTH</h6></p>
          </div>
          <p class="bg-primary mx-4 mt-4 mb-10 divider-custom"></p>
          <ul class="mx-9">
            <li class="my-3">Everything in Workflow, plus...</li>
            <li class="my-3">White-labelled client experience</li>
            <li class="my-3">Client forms and questionnaires</li>
            <li class="my-3">Workflow automations</li>
            <li class="my-3">Subcontracting (client-mode)</li>
            <li class="my-3">Calendly integration</li>
            <li class="my-3">Client portal</li>
            <li class="my-3">Priority support</li>
          </ul>
          <v-btn class="bg-primary w-100 py-8 d-flex align-center mt-12 mb-4">START FREE</v-btn>
        </v-card>
      </v-col>
    </v-row>
  </v-container>

  <!-- SUPER CHARGE TITLE -->

  <v-container class="mt-16 px-16">
    <h2 class="text-h4 my-font-serif text-center">Super charge your works with add-ons</h2>
  </v-container>

  <!-- SUPER CHARGE CARDS -->

  <v-container class="d-block d-md-flex mt-16 px-10 px-md-16">
    <v-card class="py-6 elevation-3">
      <v-row>
        <v-col cols="10">
          <v-card-title class="mb-n2">Colaborators</v-card-title>
          <v-card-subtitle>Invite other users to specific projects for limited access and funcionality.</v-card-subtitle>
        </v-col>
        <v-col cols="2" class="d-flex align-center">
          <h2 class="pl-14">Free</h2>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="py-6 elevation-3 my-4">
      <v-row>
        <v-col cols="10">
          <v-card-title class="mb-n2">Partners</v-card-title>
          <v-card-subtitle>Invite other users to specific projects for limited access and funcionality.</v-card-subtitle>
        </v-col>
        <v-col cols="2" class="d-flex flex-column align-center">
          <h2 class="text-h4 font-weight-bold">$9</h2>
          <h5>/MONTH</h5>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="py-6 elevation-3">
      <v-row>
        <v-col cols="10">
          <v-card-title class="mb-n2">Bonsai Tax</v-card-title>
          <v-card-subtitle>Invite other users to specific projects for limited access and funcionality.</v-card-subtitle>
          <button class="elevation-0 text-caption d-flex align-center text-primary ml-4 mt-1">LEARN MORE<v-icon icon="mdi-chevron-right"></v-icon> </button>
        </v-col>
        <v-col cols="2" class="d-flex flex-column align-center">
          <h2 class="text-h4 font-weight-bold">$10</h2>
          <h5>/MONTH</h5>
        </v-col>
      </v-row>
    </v-card>
  </v-container>

  <!-- SUPER CHARGE CARDS MOBILE -->

  <v-container class="d-block d-md-none mt-16 px-10 px-md-16">
    <v-card class="rounded-lg">
      <v-card-title class="text-center">Colaborators</v-card-title>
      <p class="text-center">Invite other users to specific projects for limited access and funcionality.</p>
      <h2 class="text-center">Free</h2>
    </v-card>
  </v-container>

  <!-- GREEN BG SECTION -->

  <v-container class="mt-16 px-16">
    <v-row style="background-color: #D4F1F4; height: 300px;" class="d-flex align-center rounded-lg">
      <v-col class="pl-0 pl-md-16" cols="12" md="9">
        <h2 class="d-flex text-h4 my-font-serif">It's <h2 class="text-h4 mx-2 text-primary my-font-serif">your</h2> business.</h2>
        <h2 class="text-h4 my-font-serif text-center">We're here to help it grow.</h2>
      </v-col>
      <v-col cols="12" md="3">
        <v-btn class="bg-primary px-12 py-8 font-weight-bold d-flex align-center">START FREE</v-btn>
      </v-col>
    </v-row>
  </v-container>

  <!-- FREQUENTLY ASKED QUESTIONS -->

  <v-container class="mt-16 px-16">
    <h2 class="text-h4 font-weight-thin text-primary text-center">Frequently Asked Questions</h2>
  </v-container>

  <v-container class="mt-16 px-16 d-flex flex-column align-center">
    <v-expansion-panels class="w-75 my-2 elevation-0">
      <v-expansion-panel title="How does the 14 days free trial work?" text="Lorem ipsum dolor "></v-expansion-panel>
    </v-expansion-panels>
    <v-expansion-panels class="w-75 my-2 elevation-0">
      <v-expansion-panel title="Can I change plans anytime?" text="Lorem ipsum dolor "></v-expansion-panel>
    </v-expansion-panels>
    <v-expansion-panels class="w-75 my-2 elevation-0">
      <v-expansion-panel title="How do I pause my Bonsai subscription?" text="Lorem ipsum dolor "></v-expansion-panel>
    </v-expansion-panels>
    <v-expansion-panels class="w-75 my-2 elevation-0">
      <v-expansion-panel title="What is your refund policy?" text="Lorem ipsum dolor "></v-expansion-panel>
    </v-expansion-panels>
  </v-container>

  <!-- END SECTION -->

  <v-container class="mt-16 px-16">
    <v-row>
      <v-col class="d-flex justify-center">
        <div>
          <h4 class="mb-6">PRODUCT</h4>
          <p class="my-1">Proposals</p>
          <p class="my-1">Contracts</p>
          <p class="my-1">Invoicing</p>
          <p class="my-1">Client CRM</p>
          <p class="my-1">Time Tracking</p>
          <p class="my-1">Task Tracking</p>
          <p class="my-1">Forms</p>
          <p class="my-1">Accounting</p>
          <p class="my-1">Bonsai Tax</p>
          <p class="my-1">Bonsai Cash</p>

          <p class="text-primary mt-5">Pricing</p>
          <p>Bonsai Reviews</p>
        </div>
      </v-col>
      <v-col class="d-flex justify-center">
        <div>
          <h4 class="mb-6">FREE RESOURCES</h4>
          <p class="my-1">Freelance Resources</p>
          <p class="my-1">Freelance Blog by Bonsai</p>
          <p class="my-1">How to Write a Contract</p>
          <p class="mb-7 mt-1">Online Signature Maker</p>

          <p class="my-1">Self-Employed Taxes Hub</p>
          <p class="my-1">Self-Employed Tax Calculator</p>
          <p class="my-1 mb-6">Self-Employed Tax Deductions</p>

          <h4 class="mb-3">Templates</h4>
          <button class="my-1">Invoice Templates</button><br>
          <button class="my-1">Proposal Templates</button><br>
          <button class="my-1">Contract Templates</button><br>
          <button class="my-1">Agreement Templates</button><br>
          <button class="my-1">Scope of Work Templates</button><br>
          <button class="my-1">Quote Templates</button><br>
          <button class="my-1">Credit Note Templates</button><br>
          <button class="my-1">Estimate Templates</button>
        </div>

      </v-col>
      <v-col class="d-flex justify-center">
        <div>
          <h4 class="mb-6">BONSAI</h4>
          <p>About</p>
          <p>Careers</p>
          <p>Support</p>
          <p>LinkedIn</p>
          <p>Twitter</p>
          <p>Privacy Policy</p>
          <p>Legal</p>

          <p class="mt-3">Affiliates</p>
          <p>Write for Us</p>

          <button class="mt-6">Comparisons</button>
        </div>

      </v-col>
    </v-row>
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

.divider-custom{
  height: 2px;
}
</style>
