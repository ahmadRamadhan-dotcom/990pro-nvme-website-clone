<template>
  <div class="hidden sm:hidden md:block xl:hidden">
    <div class="">
      <span
        v-for="(data, index) in fullData"
        :key="index"
        class="cursor-pointer hover:border-b text-[13px] md:text-[14px] md:p-[15px_5px] lg:p-[15px_15px] font-['SamsungOneBold']"
        >{{ data.name }}</span
      >
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  fullData: Array,
});
</script>
