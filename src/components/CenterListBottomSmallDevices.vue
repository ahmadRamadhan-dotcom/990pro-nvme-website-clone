<template>
  <div class="md:hidden w-full">
    <div class="md:hidden">
      <div class="flex justify-center sm:flex sm:justify-start gap-7 sm:gap-8">
        <span
          v-for="(data, index) in centerData"
          :key="index"
          :class="
            data.id === 1
              ? ' font-bold border-b text-[#ffffff]'
              : ' font-normal text-[#dddddd]'
          "
          class="cursor-pointer hover:border-b hover:font-bold hover:text-[#ffffff] text-sm p-[13px_8px] sm:p-[13px_20px] xl:p-[13px_20px] font-['SamsungOne']"
          >{{ data.name }}</span
        >
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  centerData: Array,
});
</script>
