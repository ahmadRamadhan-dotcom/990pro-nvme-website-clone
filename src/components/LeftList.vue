<template>
  <div class="sm:hidden xl:flex">
    <span
      v-for="(data, index) in leftData"
      :key="index"
      class="cursor-pointer hover:border-b text-sm xl:p-[15px_12px] font-['SamsungOneBold']"
      >{{ data.name }}</span
    >
  </div>
</template>

<script setup>
const props = defineProps({
  leftData: Array,
});
</script>
