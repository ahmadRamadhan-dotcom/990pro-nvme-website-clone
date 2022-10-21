<template>
  <div class="sm:pb-12 xl:h-[85vh] flex justify-center">
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
          class="sm:text-2xl md:text-[34px] sm:w-[200px] md:w-full text-center lg:text-5xl sm:mt-10 md:mb-10 xl:mb-10 font-bold font-['Samsung_Sharp_Sans']"
          >PCIe 4.0 speed maximized
        </span>
        <div
          class="md:hidden grid text-sm font-normal font-['SamsungOne'] text-center mt-10"
        >
          <span v-for="(data, index) in pcie4PerfDataSmallDevices" :key="index">
            {{ data.content }}
          </span>
        </div>
        <span
          v-for="(data, index) in pcie4PerfData"
          :key="index"
          class="sm:hidden md:block font-['SamsungOne'] font-normal md:text-[15px] lg:text-lg"
          >{{ data.content }}
        </span>
        <div class="sm:hidden md:block lg:mt-8 grid text-center">
          <span
            class="font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
          >
            * Sequential and random write performance was measured with
            Intelligent Turbo Write technology being <br class="lg:hidden" />
            activated. Intelligent Turbo Write operates only
            <br class="md:hidden lg:block xl:hidden" />
            within a specific data transfer size.
            <br class="md:hidden lg:block" />
          </span>
          <span
            class="font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
          >
            Performance may vary <br class="lg:hidden" />
            depending on SSD’s firmware, system hardware & configuration and
            other factors. For detailed information, please
            <br class="lg:hidden" />
            contact your local <br class="md:hidden lg:block xl:hidden" />
            service center <br class="lg:hidden xl:block" />
          </span>
          <br class="sm:hidden xl:block" />
          <span
            class="xl:mt-6 font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
          >
            * Test system configuration: AMD Ryzen 7 5800X 8-Core Processor
            CPU@3.80GHz, DDR4 3600MHz 16GBx2 (PC4 <br class="lg:hidden" />
            -25600 Overclock), <br class="md:hidden lg:block xl:block" />
          </span>
          <span
            class="font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
          >
            OS - Windows 10 Pro 64bit, Chipset - ASRock-X570 Taich
          </span>
          <div class="sm:mt-5 xl:mt-5 grid">
            <span
              class="font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
            >
              * To maximize the performance of the 990 PRO, please check whether
              your system supports PCIe®4.0 at the Intel
              <br class="lg:hidden" />
              or AMD website.
            </span>
            <span
              class="md:mt-6 xl:mt-5 font-['SamsungOne'] font-normal text-[#f8f8f8] text-[12px]"
            >
              *4TB to be released in 2023.
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
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
      "Fly high in gaming, video and 3D editing, data analysis, and more.",
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
</script>
