<script setup lang="ts">
const props = defineProps(['playerDetail'])
import { CBadge, CListGroupItem, CProgress, CProgressStacked } from "@coreui/vue";
</script>

<template>
  <CListGroupItem class="d-flex justify-content-between align-items-center">
    <CBadge color="primary" shape="rounded-pill">
      {{ props.playerDetail.initiative }}
    </CBadge>
    {{ props.playerDetail.player }}
    <CProgressStacked style="width: 50px">
      <CProgress color="success" :value="props.playerDetail.life" />
      <CProgress color="danger" :value="(100 - props.playerDetail.life)" />
    </CProgressStacked>
  </CListGroupItem>
</template>

<style scoped>

</style>