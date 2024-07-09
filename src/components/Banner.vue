<script setup>

import { computed } from 'vue';

const props = defineProps({
    vehicle: String
});

const bannerImgURL = computed(() => `/images/banners/${props.vehicle.toLowerCase()}.avif`);

</script>

<template>

    <div class="banner-img">
        <img :src="bannerImgURL" />
    </div>

</template>

<style scoped>

.banner-img{
    border: 1px solid #000;
    display: flex;
    margin: 0;
    padding: 0;
    width: 930px;
    position: relative;
}

.banner-img img{
    margin: 0;
    padding: 0;
}

</style>