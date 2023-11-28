<template>
  <a-tabs>
    <a-tab-pane v-for="item in tabData" :key="item.key" :tab="item.tab">
      <slot></slot>
    </a-tab-pane>
    <template #rightExtra>
        <slot name="icon-button"></slot>
    </template>
  </a-tabs>

</template>

<script setup>
import { ref } from "vue";

const tabData = [
  { key: "1", tab: "Tab 1" },
  { key: "2", tab: "Tab 2" },
  { key: "3", tab: "Tab 3" },
];

</script>
