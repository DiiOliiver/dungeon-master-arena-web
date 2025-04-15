<script setup lang="ts">
import '@coreui/coreui/dist/css/coreui.min.css'
import 'bootstrap/dist/css/bootstrap.min.css'
import {
  CContainer, CRow, CCol
} from "@coreui/vue";
import HeaderComponent from "./components/layout/HeaderComponent.vue";
import MapComponent from "./components/map/MapComponent.vue";
import SkillPlayerComponent from "./components/player/SkillPlayerComponent.vue";
import MissionDetailComponent from "./components/missiondetail/MissionDetailComponent.vue";
</script>

<template>
  <div class="min-vh-100 min-vw-100" style="background-color: #727d8d">
    <HeaderComponent />
    <CContainer>
      <CRow>
        <CCol sm="12" md="12" lg="8" class="mt-4">
          <MapComponent />
        </CCol>
        <CCol sm="12" md="12" lg="4" class="mt-4">
          <MissionDetailComponent />
        </CCol>
        <CCol sm="12" md="12" lg="12" class="mt-4">
          <SkillPlayerComponent />
        </CCol>
      </CRow>
    </CContainer>
  </div>
</template>

<style scoped>
</style>
