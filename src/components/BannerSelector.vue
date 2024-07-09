<script setup>

import { ref } from 'vue';
import Banner from '@/components/Banner.vue';

const vehicles = [
    {
        vehicleName: 'Honda Accord',
        vehicleTag: 'accord',
    },
    {
        vehicleName: 'Honda Civic',
        vehicleTag: 'civic',
    },
    {
        vehicleName: 'Honda CRV',
        vehicleTag: 'crv',
    },
]

const selectedVehicle = ref(vehicles[0].vehicleTag);

const selectVehicle = (e) => {
    selectedVehicle.value = e.target.value;
}

</script>

<template>

<div class="banner-selector">

    <Banner :vehicle="selectedVehicle" />

    <select v-on:change="selectVehicle">
        <option v-for="vehicle in vehicles" :key="vehicle.vehicleTag" :value="vehicle.vehicleTag">{{ vehicle.vehicleName }}</option>
    </select>

</div>


</template>

<style scoped>

.banner-selector{
    margin: 30px;
}

.banner-selector select{
    border-radius: 5px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    min-height: 30px;
    margin: 15px 0;
    padding: 15px 0 15px 5px;
    width: 932px;
}


</style>