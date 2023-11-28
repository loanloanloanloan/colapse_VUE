<template>
  <Tabs>
    <Tabs>
      <Colapse :activeKey="keyColapse" @change="handleChangeColapse" />
    </Tabs>
    <template #icon-button>
      <a-button :disabled="keyColapse.length === 2"><caret-down-outlined /></a-button>
      <a-button :disabled="keyColapse.length === 0"><caret-up-outlined /></a-button>
    </template>
  </Tabs>
</template>

<script setup>
import {ref} from 'vue'
import { CaretUpOutlined, CaretDownOutlined } from "@ant-design/icons-vue";
import Tabs from "./components/Tabs.vue";
import Colapse from "./components/Colapse.vue";
const keyColapse = ref(['1', '2'])
const disableButton1 = ref(true);
const disableButton2 = ref(false);


const handleChangeColapse = (key)=>{  
  keyColapse.value = key
  if(keyColapse.value === 2) {
    disableButton2.value = true;
  } 
  else{
    disableButton1.value = false;
    disableButton2.value = false;
  }
}

</script>

