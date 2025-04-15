<script setup lang="ts">
  import { GridLayout, GridItem } from 'grid-layout-plus'
  import { reactive } from 'vue'
  const layout = reactive([
    { x: 0, y: 0, w: 1, h: 4, i: '0', static: false },
    { x: 2, y: 0, w: 1, h: 4, i: '1', static: false },
  ])
</script>

<template>
  <GridLayout
      v-model:layout="layout"
      :row-height="12"
      :col-num="12"
      max-rows="34"
      class="grid--layout"
      :style="`background-image: url(${'/imgs/maps/cave_01.png'})`"
      :use-style-cursor="false"
      :vertical-compact="false"
      prevent-collision
  >
    <GridItem
        v-for="item in layout"
        :key="item.i"
        :x="item.x"
        :y="item.y"
        :w="item.w"
        :h="item.h"
        :i="item.i"
        @resize="() => {}"
        :is-resizable="false"
    >
      {{ item.i }}
    </GridItem>
  </GridLayout>
</template>

<style scoped>
  @import "custom.css";
</style>