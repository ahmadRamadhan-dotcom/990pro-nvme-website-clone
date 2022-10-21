<template>
  <div class="sm:hidden md:block xl:mx-auto text-center">
    <div class="xl:flex xl:gap-8">
      <span
        v-for="(data, index) in centerData"
        :key="index"
        :class="
          data.id === 1
            ? ' font-bold border-b text-[#ffffff]'
            : ' font-normal text-[#dddddd]'
        "
        class="cursor-pointer hover:border-b hover:font-bold hover:text-[#ffffff] text-sm md:p-[13px_28px] lg:p-[13px_30px] xl:p-[13px_20px] font-['SamsungOne']"
        >{{ data.name }}</span
      >
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  centerData: Array,
});
</script>
