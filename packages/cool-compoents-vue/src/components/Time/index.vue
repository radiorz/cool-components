<!--
* @FileDescription: 该文件的描述信息
* @Date: 2022年06月11日 09:10:43
* TODO:
* [] 
-->

<script>
export default {
  name: "TheTime",
};
</script>
<script setup>
import { ref, onMounted } from "vue";
let time = ref(new Date());
onMounted(() => {
  setInterval(() => {
    time.value = new Date();
  }, 1000);
});
</script>

<template>
  <div class="the-time bg-slate-500">
    {{ time }}
  </div>
</template>

<style lang="scss" scoped></style>
