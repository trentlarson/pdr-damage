<template>
  <h1>Damage Report</h1>
  <p>
    Year: <input type="text" v-model="year">
    Make: <input type="text" v-model="make">
    Model: <input type="text" v-model="model">
    VIN: <input type="text" v-model="vin">
    Color: <input type="text" v-model="color">
  </p>

  <input type="submit" @click="print"/>

</template>

<script setup lang="ts">
/**
Vehicle info: Year, Make, Model, VIN (optional), Color
• Damage report for at least 3 panels from: Hood, Roof, Left/Right Front Door, Left/Right Rear Door, Trunk/Deck Lid, Left/Right Quarter Panel, Left/Right Fender
• For each panel: Number of dents (1–100), Average dent size (Small/Medium/Large/Oversized), Severity (Light/Moderate/Heavy)
• A submit button that shows a summary of the report
**/

import { Component, Vue } from "vue-facing-decorator";

class AccountViewView extends Vue {
  year: string = "2022";
  make: "Toyota";
  model: "Camry";
  color: "Silver";
  vin: "";

  print() {
    console.log("" + year + " " + make + " " + model + " " + color + " " + vin);
  }

  /**
  data() {
    return {
      "vehicle": {
        "year": "2022", "make": "Toyota", "model": "Camry", "color": "Silver"
      },
      "panels": [
        { "name": "Hood", "dentCount": 24, "dentSize": "Medium", "severity": "Moderate" }, { "name": "Roof", "dentCount": 41, "dentSize": "Small", "severity": "Heavy" }
      ]
    }
  }
  **/
}
</script>

<style scoped></style>
