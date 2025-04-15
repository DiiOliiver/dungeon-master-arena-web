<script setup lang="ts">
import { CCard, CCardBody, CCardHeader, CCardSubtitle, CCardTitle } from "@coreui/vue";
import GridMapComponent from "../gridmap/GridMapComponent.vue";
</script>

<template>
  <CCard>
    <CCardHeader class="text-lg-start">
      <CCardTitle>Mapa:</CCardTitle>
      <CCardSubtitle>Caverna (Nv. 1)</CCardSubtitle>
    </CCardHeader>
    <CCardBody class="position-relative h-100">
      <GridMapComponent />
    </CCardBody>
  </CCard>
</template>

<style scoped>
</style>