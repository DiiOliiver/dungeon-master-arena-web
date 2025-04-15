<script setup lang="ts">
import {
  CCard,
  CCardBody,
  CCardHeader,
  CCardSubtitle,
  CCardTitle,
  CListGroup,
} from "@coreui/vue";
import DetailsAboutAlliedPlayersComponent from "./DetailsAboutAlliedPlayersComponent.vue";

const playerDetails = [
  {
    initiative: 1,
    player: 'Cras justo odio',
    life: 100
  },
  {
    initiative: 2,
    player: 'Dapibus ac facilisis',
    life: 50
  },
  {
    initiative: 3,
    player: 'Morbi leo risus',
    life: 75
  },
]
</script>

<template>
  <CCard class="h-100">
    <CCardHeader class="text-lg-start">
      <CCardTitle>Missão:</CCardTitle>
      <CCardSubtitle>Explore a caverna</CCardSubtitle>
    </CCardHeader>
    <CCardBody>
      <CListGroup
        v-for="(playerDetail, key) of playerDetails" :key="key"
      >
        <DetailsAboutAlliedPlayersComponent :playerDetail="playerDetail" />:
      </CListGroup>
    </CCardBody>
  </CCard>
</template>

<style scoped>
</style>