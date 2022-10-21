<template>
  <div class="py-12 sm:py-10 md:py-0xl:h-[85vh] flex justify-center">
    <div class="grid place-content-center place-items-center">
      <div class="grid place-items-center">
        <div class="grid md:hidden text-center">
          <span class="text-[12px] text-[#f8f8f8] font-normal">
            * PCie 4.0's best theoretical sequential read is 8000 MB/s
          </span>
          <span class="text-[12px] text-[#f8f8f8] font-normal">
            - 990 PRO reaches 7.4580 MB/s as of Q3, 2022
          </span>
        </div>
        <span
          class="text-2xl sm:text-2xl md:text-[34px] w-10/12 sm:w-[200px] md:w-full text-center lg:text-5xl mt-12 sm:mt-10 md:mb-10 xl:mb-10 font-bold font-['Samsung_Sharp_Sans']"
          >PCIe 4.0 speed maximized
        </span>
        <div
          class="sm:hidden pb-12 mt-6 grid text-sm font-normal font-['SamsungOne'] text-center"
        >
          <span
            v-for="(data, index) in pcie4PerfDataMobileDevices"
            :key="index"
          >
            {{ data.content }}
          </span>
          <span>
            performance of PCIe<sup>®</sup> 4.0 Fly high in gaming, video
          </span>
          <span> and 3D editing, data analysis, and more. </span>
        </div>
        <div
          class="hidden sm:pb-16 sm:grid md:hidden text-sm font-normal font-['SamsungOne'] text-center mt-10"
        >
          <span v-for="(data, index) in pcie4PerfDataSmallDevices" :key="index">
            {{ data.content }}
          </span>
        </div>
        <Samsung999ProNvmeSpeed class="md:hidden" />
        <span
          v-for="(data, index) in pcie4PerfData"
          :key="index"
          class="hidden sm:hidden md:block font-['SamsungOne'] font-normal md:text-[15px] lg:text-lg"
          >{{ data.content }}
        </span>
        <NoticeTesPerf />
        <Samsung999ProNvmeSpeed class="hidden sm:hidden md:block" />
      </div>
    </div>
  </div>
</template>

<script setup>
import Samsung999ProNvmeSpeed from "./990ProSpeedImage.vue";
import NoticeTesPerf from "./NoticeTesPerf.vue";
const pcie4PerfData = [
  { id: 1, content: "Huge speed boost." },
  {
    id: 2,
    content:
      "40% and 55% faster random read/write speeds than 980 PRO - up to 1400K/1650K IOPS,",
  },
  {
    id: 3,
    content:
      "while sequential read/write speeds up to 7450/6900 MB/s reach near max performance of PCIe® 4.0.",
  },
  {
    id: 4,
    content:
      " Fly high in gaming, video and 3D editing, data analysis, and more.",
  },
];

const pcie4PerfDataSmallDevices = [
  {
    id: 1,
    content:
      "Huge speed boost 40% and 55% faster random read/write speeds than 980 PRO - up to",
  },
  {
    id: 2,
    content:
      "1400K/1650K IOPS while sequential read/write speeds up to 7450/6900 MB/s reach near max",
  },
  {
    id: 3,
    content:
      "performance of PCIe® 4.0. Fly high in gaming, video and 3D editing, data analysis, and more.",
  },
];

const pcie4PerfDataMobileDevices = [
  { id: 1, content: "Huge speed boost. 40% and 55% faster random" },
  { id: 2, content: "read/write speeds than 980 PRO - up to" },
  { id: 3, content: "1400K/1650K, while sequential read/write" },
  { id: 4, content: "speeds up to 7450/6900 MB/s react near max" },
];
</script>
