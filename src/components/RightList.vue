<template>
  <div class="md:flex md:items-center xl:flex xl:gap-3 xl:items-center">
    <div class="hidden sm:hidden xl:flex">
      <span
        v-for="(data, index) in rightData"
        :key="index"
        class="cursor-pointer hover:border-b text-sm xl:p-[15px_12px] font-['SamsungOneBold']"
        >{{ data.name }}</span
      >
    </div>
    <div
      class="flex items-center sm:flex sm:items-center xl:flex xl:items-center gap-5 sm:gap-5 xl:gap-5"
    >
      <button
        aria-label="search button"
        class="inline-flex items-cente w-4 sm:w-4 xl:w-5"
      >
        <img
          src="/icon-bold-action-search-wh.svg"
          alt="search icon with white color"
        />
      </button>
      <div class="flex items-center gap-2">
        <a href="#" class="w-4 sm:w-4 xl:w-5 flex items-center">
          <img src="/icon-language.svg" alt="white globel icon" />
        </a>
        <span
          class="font-['SamsungOne'] text-[10px] sm:text-[10px] xl:text-[12px]"
          >Global</span
        >
      </div>
      <a
        href="#_"
        class="md:hidden inline-flex items-center justify-center px-1 py-1"
      >
        <img
          src="../assets/navigation.svg"
          alt="hamburger menu only showing in small devices"
          class="h-5 sm:h-5"
        />
      </a>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  rightData: Array,
});
</script>
