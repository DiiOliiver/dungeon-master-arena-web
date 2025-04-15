<script setup lang="ts">
import '@coreui/coreui/dist/css/coreui.min.css'
import 'bootstrap/dist/css/bootstrap.min.css'
import {
  CContainer, CRow, CCol, CCard, CCardBody,
  CCardHeader, CCardSubtitle, CCardTitle, CImage,
  CListGroup, CListGroupItem, CBadge, CProgress, CProgressStacked
} from "@coreui/vue";
import HeaderComponent from "./components/layout/HeaderComponent.vue";
</script>

<template>
  <div class="min-vh-100 min-vw-100" style="background-color: #727d8d">
    <HeaderComponent />
    <CContainer>
      <CRow>
        <CCol sm="12" md="12" lg="8" class="mt-4">
          <CCard style="height: 50rem">
            <CCardHeader class="text-lg-start">
              <CCardTitle>Mapa:</CCardTitle>
              <CCardSubtitle>Caverna (Nv. 1)</CCardSubtitle>
            </CCardHeader>
            <CCardBody class="overflow-y-scroll">
              <CImage
                fluid
                src="/imgs/maps/cave_02.png"
                class="card--image--map"
              />
            </CCardBody>
          </CCard>
        </CCol>
        <CCol sm="12" md="12" lg="4" class="mt-4">
          <CCard class="h-100">
            <CCardHeader class="text-lg-start">
              <CCardTitle>Missão:</CCardTitle>
              <CCardSubtitle>Explore a caverna</CCardSubtitle>
            </CCardHeader>
            <CCardBody>
              <CListGroup>
                <CListGroupItem class="d-flex justify-content-between align-items-center">
                  <CBadge color="primary" shape="rounded-pill">1</CBadge> Cras justo odio
                  <CProgressStacked style="width: 50px">
                    <CProgress color="success" :value="100" />
                    <CProgress color="danger" :value="0" />
                  </CProgressStacked>
                </CListGroupItem>
                <CListGroupItem class="d-flex justify-content-between align-items-center">
                  <CBadge color="primary" shape="rounded-pill">2</CBadge> Dapibus ac facilisis
                  <CProgressStacked style="width: 50px">
                    <CProgress color="success" :value="70" />
                    <CProgress color="danger" :value="30" />
                  </CProgressStacked>
                </CListGroupItem>
                <CListGroupItem class="d-flex justify-content-between align-items-center">
                  <CBadge color="primary" shape="rounded-pill">3</CBadge> Morbi leo risus
                  <CProgressStacked style="width: 50px">
                    <CProgress color="success" :value="49" />
                    <CProgress color="danger" :value="51" />
                  </CProgressStacked>
                </CListGroupItem>
              </CListGroup>
            </CCardBody>
          </CCard>
        </CCol>
        <CCol sm="12" md="12" lg="12" class="mt-4">
          <CCard style="height: 20rem">
            <CCardBody>
              <div>
                Outra coisa
              </div>
            </CCardBody>
          </CCard>
        </CCol>
      </CRow>
    </CContainer>
  </div>
</template>

<style scoped>
.card--image--map {
  opacity: 95%;
  z-index: -100;
}
</style>
