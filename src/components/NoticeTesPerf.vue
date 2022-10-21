<template>
  <div
    class="leading-3 xl:grid text-center md:leading-5 mt-8 sm:pb-0 md:pb-10 grid place-content-center place-items-center sm:grid sm:place-content-center sm:place-items-center lg:mt-8"
  >
    <p
      class="sm:grid md:grid lg:grid font-['SamsungOne'] w-10/12 sm:w-11/12 md:w-1 lg:w-9/12 font-normal text-[#f8f8f8] text-[12px]"
    >
      * Sequential and random write performance was measured with Intelligent
      Turbo Write technology being activated. Intelligent Turbo Write operates
      only within a specific data transfer size. Performance may vary depending
      on SSD’s firmware, system hardware &amp; configuration and other factors.
      For detailed information, please contact your local service center
    </p>

    <div
      class="grid text-center place-content-center place-items-center mt-4 sm:mt-4 xl:mt-4"
    >
      <span
        v-for="(data, index) in noticeData"
        :key="index"
        class="w-10/12 sm:w-[95%] md:w-9/12 sm:grid font-['SamsungOne'] mb-4 font-normal text-[#f8f8f8] text-[12px]"
      >
        {{ data.content }}
      </span>
    </div>
    <span
      class="sm:mt-4 xl:mt-4 font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
    >
      *4TB to be released in 2023.
    </span>
  </div>
</template>

<script setup>
const noticeData = [
  {
    id: 1,
    content:
      "* Test system configuration: AMD Ryzen 7 5800X 8-Core Processor CPU@3.80GHz, DDR4 3600MHz 16GBx2 (PC4-25600 Overclock), OS - Windows 10 Pro 64bit, Chipset - ASRock-X570 Taichi",
  },
  {
    id: 2,
    content:
      "* To maximize the performance of the 990 PRO, please check whether your system supports PCIe® 4.0 at the Intel or AMD website.",
  },
];
</script>
