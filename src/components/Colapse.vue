<template>
  <a-collapse v-model:activeKey="activeKey" expand-icon-position="end">
    <a-collapse-panel key="1" header="This is panel header 1">
      <p>{{ text }}</p>
    </a-collapse-panel>
    <a-collapse-panel key="2" header="This is panel header 2">
      <p>{{ text }}</p>
    </a-collapse-panel>
  </a-collapse>
</template>

<script setup>
import { ref, watch} from "vue";
const text = `A dog is a type of domesticated animal.Known for its loyalty and faithfulness,it can be found as a welcome guest in many households across the world.`;
const activeKey = ref(['1', '2']);
const props = defineProps(['activeKey'])

watch(activeKey.value,()=>{
    activeKey.value = props.activeKey 
})
</script>
