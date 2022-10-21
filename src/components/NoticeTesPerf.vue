<template>
  <div
    class="leading-3 xl:grid text-center md:leading-5 mt-8 sm:pb-0 md:pb-10 grid place-content-center place-items-center sm:grid sm:place-content-center sm:place-items-center lg:mt-8"
  >
    <span
      v-for="(data, index) in noticeDataTopLargeDevices"
      :key="index"
      class="hidden sm:hidden lg:block font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
    >
      {{ data.content }}
    </span>

    <span
      class="hidden sm:grid md:hidden font-['SamsungOne'] w-11/12 font-normal text-[#f8f8f8] text-[12px]"
    >
      * Sequential and random write performance was measured with Intelligent
      Turbo Write technology being activated. Intelligent Turbo Write operates
      only within a specific data transfer size. Performance may vary depending
      on SSD’s firmware, system hardware &amp; configuration and other factors.
      For detailed information, please contact your local service center
    </span>

    <p
      class="w-11/12 sm:hidden font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
    >
      * Sequential and random write performance was measured with Intelligent
      Turbo Write technology being activated. Intelligent Turbo Write operates
      only within a specific data transfer size. Performance may vary depending
      on SSD’s firmware, system hardware &amp; configuration and other factors.
      For detailed information, please contact your local service center
    </p>

    <span
      class="hidden sm:hidden md:grid lg:hidden font-['SamsungOne'] w-10/12 font-normal text-[#f8f8f8] text-[12px]"
    >
      * Sequential and random write performance was measured with Intelligent
      Turbo Write technology being activated. Intelligent Turbo Write operates
      only within a specific data transfer size. Performance may vary depending
      on SSD’s firmware, system hardware &amp; configuration and other factors.
      For detailed information, please contact your local service center
    </span>

    <div
      class="grid text-center place-content-center place-items-center mt-4 sm:mt-4 xl:mt-4"
    >
      <span
        v-for="(data, index) in noticeDataBottomLargeDevices"
        :class="data.id === 3 ? 'xl:mt-5' : ''"
        :key="index"
        class="hidden sm:hidden font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
      >
        {{ data.content }}
      </span>

      <span
        v-for="(data, index) in noticeDataBottomSmallDevices"
        :key="index"
        :class="data.id === 3 ? 'mt-4' : ''"
        class="hidden sm:grid font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
      >
        {{ data.content }}
      </span>

      <span
        v-for="(data, index) in noticeDataBottomMobileDevices"
        :key="index"
        class="w-10/12 sm:hidden font-['SamsungOne'] mb-4 font-normal text-[#f8f8f8] text-[12px]"
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
const noticeDataTopLargeDevices = [
  {
    id: 1,
    content:
      " * Sequential and random write performance was measured Intelligent Turbo Write technology being activated. Intelligent Turbo Write operates only within a specific data transfer size.",
  },
  {
    id: 2,
    content:
      "Performance may vary depending on SSD’s firmware, system hardware & configuration and other factors. For detailed information, please contact your local service center",
  },
];

const noticeDataBottomSmallDevices = [
  {
    id: 1,
    content:
      "* Test system configuration: AMD Ryzen 7 5800X 8-Core Processor CPU@3.80GHz, DDR4 3600MHz 16GBx2 (PC4- ",
  },
  {
    id: 2,
    content:
      "25600 Overclock), OS - Windows 10 Pro 64bit, Chipset - ASRock-X570 Taichi",
  },
  {
    id: 3,
    content:
      "* To maximize the performance of the 990 PRO, please check whether your system supports PCIe ® 4.0 at the ",
  },
  {
    id: 4,
    content: "Intel or AMD website.",
  },
];

const noticeDataBottomMobileDevices = [
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

const noticeDataBottomLargeDevices = [
  {
    id: 1,
    content:
      "* Test system configuration: AMD Ryzen 7 5800X 8-Core Processor CPU@3.80GHz, DDR4 3600MHz 16GBx2 (PC4-25600 Overclock),",
  },
  { id: 2, content: "OS - Windows 10 Pro 64bit, Chipset - ASRock-X570 Taich" },
  {
    id: 3,
    content:
      "* To maximize the performance of the 990 PRO, please check whether your system supports PCIe®4.0 at the Intel or AMD website.",
  },
];
</script>
