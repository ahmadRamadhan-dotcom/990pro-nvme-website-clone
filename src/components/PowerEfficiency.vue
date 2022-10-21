<template>
  <div class="flex xl:pt-10 xl:pb-12 justify-center">
    <div class="grid place-content-center place-items-center">
      <span class="font-['Samsung_Sharp_Sans'] font-bold xl:text-5xl"
        >Breakthrough power efficiency
      </span>
      <div class="xl:mt-10 grid text-center">
        <span
          v-for="(data, index) in powerEfficiencyData"
          :key="index"
          class="font-['SamsungOne'] font-normal text-lg"
        >
          {{ data.content }}
        </span>
        <span class="font-['SamsungOne'] font-normal text-lg">
          This low-power design makes max PCIe<sup>®</sup>4.0 performance
          possible with optimal power efficiency.
        </span>
      </div>
      <div class="xl:mt-10 grid text-center">
        <span class="text-[12px] font-normal font-['SamsungOne']"
          >* 980 PRO Sequential Read/Write - 1,129/877 MB/Watt,
        </span>
        <span class="text-[12px] font-normal font-['SamsungOne']"
          >990 PRO Sequential Read/Write - 1380/1319 MB/Watt based on internal
          test result of the 1TB capacity model.
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const powerEfficiencyData = [
  { id: 1, content: "More power-efficient performance." },
  { id: 2, content: "Higher perfomance usually consumes more power." },
  {
    id: 3,
    content:
      "But, 990 PRO uses less power with over 50% improved perfomance per Watt over 980 PRO.",
  },
];
</script>
