<script setup>

import CarTrim from '@/components/CarTrim.vue';
import Header from '@/components/Header.vue';
import BannerSelector from '@/components/BannerSelector.vue';

const accord = {
  modelName: 'Accord',
  trimName: 'EX',
  thumbnail: '/images/2025-honda-accord-ex/Trim_Jellybeans_294x165_2023_Accord_EX_MGM.avif',
  defaultTrim: 'silverTrim',
  silverTrim: '/images/2025-honda-accord-ex/NEWTrim_BAP_Carousel_718x402_2023_Accord_EX_MGM_1.avif',
  blackTrim: '/images/2025-honda-accord-ex/Trim_BAP_Carousel_718x402_2023_Accord_EX_CBP_1.avif',
  redTrim: '/images/2025-honda-accord-ex/Trim_BAP_Carousel_718x402_2023_Accord_EX_RRM_1.avif',
  whiteTrim: '/images/2025-honda-accord-ex/Trim_BAP_Carousel_718x402_2023_Accord_EX_PWP_1.avif',
  sellingPrice: '$29,506',
  includes: 'Includes freights & PDI $2,000.00 and fees $131.50. Excludes taxes.',
};

const civic = {
  modelName: 'Civic',
  trimName: 'LX',
  thumbnail: '/images/2025-honda-civic-lx/MY25_Civic_Sedan_LX_SRSM_1036x520_Desktop_TrimSelector_Front.avif',
  defaultTrim: 'silverTrim',
  silverTrim: '/images/2025-honda-civic-lx/MY25_Civic_Sedan_LX_SRSM_718x402_Desktop_TrimsCarousel_Front_01.avif',
  blackTrim: '/images/2025-honda-civic-lx/MY25_Civic_Sedan_LX_CBP_718x402_Desktop_TrimsCarousel_Front_01.avif',
  redTrim: '/images/2025-honda-civic-lx/MY25_Civic_Sedan_LX_RR_718x402_Desktop_TrimsCarousel_Front_01.avif',
  whiteTrim: '/images/2025-honda-civic-lx/MY25_Civic_Sedan_LX_PWP_718x402_Desktop_TrimsCarousel_Front_01.avif',
  sellingPrice: '$37,596',
  includes: 'Includes freights & PDI $2,000.00 and fees $131.50. Excludes taxes.',
};

const crv = {
  modelName: 'CRV',
  trimName: 'LX 2WD',
  thumbnail: '/images/2025-honda-crv-lx-2wd/MY25_CR-V_LX-2WD_SRSM_294x165_Desktop_TrimsSelector_Front.avif',
  defaultTrim: 'silverTrim',
  silverTrim: '/images/2025-honda-crv-lx-2wd/MY25_CR-V_LX_2WD_SRSM_718x402_Desktop_TrimsCarousel_Front_01.avif',
  blackTrim: '/images/2025-honda-crv-lx-2wd/MY25_CR-V_LX_2WD_CBP_718x402_Desktop_TrimsCarousel_Front_01.avif',
  redTrim: '/images/2025-honda-crv-lx-2wd/MY25_CR-V_LX_2WD_RRM_718x402_Desktop_TrimsCarousel_Front_01.avif',
  whiteTrim: '/images/2025-honda-crv-lx-2wd/MY25_CR-V_LX_2WD_PWP_718x402_Desktop_TrimsCarousel_Front_01.avif',
  sellingPrice: '$37,861',
  includes: 'Includes freights & PDI $2,000.00 and fees $131.50. Excludes taxes.',
};


</script>

<template>

<main>

  <Header />
  <div class="trim-list">

    <CarTrim 
    inList
    :vehicle="accord"
    :modelName="accord.modelName"
    :trimName="accord.trimName" 
    :thumbnail="accord.thumbnail"
    :sellingPrice="accord.sellingPrice"
    :includes="accord.includes"
    :defaultTrim="accord.defaultTrim"
    />

    <CarTrim 
    inList
    :vehicle="civic"
    :modelName="civic.modelName"
    :trimName="civic.trimName"   
    :thumbnail="civic.thumbnail"
    :sellingPrice="civic.sellingPrice"
    :includes="civic.includes"
    :defaultTrim="civic.defaultTrim"
    />

    <CarTrim 
    inList
    :vehicle="crv" 
    :modelName="crv.modelName"
    :trimName="crv.trimName"  
    :thumbnail="crv.thumbnail"
    :sellingPrice="crv.sellingPrice"
    :includes="crv.includes"
    :defaultTrim="crv.defaultTrim"
    />

  </div>
  <BannerSelector />

</main>

</template>

<style>

body{
  font-family: Helvetica, sans-serif;
  margin: 0;
  padding: 0;
}

.text-hidden{
  position: absolute !important;
  clip: rect(1px 1px 1px 1px);
  height: 1px;
  width: 1px;
  overflow: hidden;
  clip: rect(1px, 1px, 1px, 1px);
}

.trim-list {
  display: flex;
  gap: 40px;
}

</style>
