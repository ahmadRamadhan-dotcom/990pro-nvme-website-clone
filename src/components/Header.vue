<template>
  <div class="w-full bg-black flex justify-center">
    <div class="w-full grid">
      <div class="flex justify-center">
        <div
          class="w-10/12 sm:w-11/12 xl:w-[1300px] py-4 sm:py-4 xl:py-0 xl:pt-1.5 flex justify-between items-center sm:flex sm:justify-between sm:items-center"
        >
          <div class="xl:flex xl:items-center xl:gap-2">
            <img
              class="h-3 sm:h-3 lg:h-4"
              src="/global-samsung-logo.svg"
              alt="fancy samsung top logo   "
            />
            <LeftList :leftData="leftData" />
          </div>
          <FullList :fullData="fullData" />
          <RightList :rightData="rightData" />
        </div>
      </div>
      <span class="w-full sm:w-full">
        <hr
          style="
            height: 1px;
            border-width: 0;
            color: gray;
            background-color: gray;
          "
        />
      </span>
      <div class="flex justify-center xl:mt-1.5">
        <div
          class="w-10/12 sm:w-11/12 py-3 sm:py-3 xl:py-0 xl:w-[1300px] flex justify-between sm:flex sm:justify-between sm:items-center xl:flex xl:justify-between xl:items-center"
        >
          <div
            class="sm:flex sm:items-center sm:gap-2 xl:flex xl:items-center xl:gap-1"
          >
            <span
              class="font-['Samsung_Sharp_Sans'] text-[14px] sm:text-[14px] md:text-[13px] xl:text-[16px] font-bold text-[#aaaaaa]"
              >Internal S... /</span
            >
            <span
              class="font-['Samsung_Sharp_Sans'] text-[14px] sm:text-[14px] md:text-[13px] xl:text-[16px] font-bold"
              >990 PRO</span
            >
          </div>
          <CenterListBottom :centerData="centerData" />
          <div class="">
            <a
              href="#_"
              class="rounded-full xl:text-sm px-3 py-2 sm:px-3 sm:py-2 xl:px-5 xl:py-2 font-['SamsungOne'] font-bold nline-flex border items-center justify-center text-[12px] sm:text-[12px]"
            >
              Where to buy
            </a>
          </div>
        </div>
      </div>
      <span class="w-full sm:w-full md:hidden">
        <hr
          style="
            height: 1px;
            border-width: 0;
            color: gray;
            background-color: gray;
          "
        />
      </span>
      <CenterListBottomSmallDevices :centerData="centerData" />
    </div>
  </div>
</template>

<script setup>
import FullList from "./FullList.vue";
import RightList from "./RightList.vue";
import LeftList from "./LeftList.vue";
import CenterListBottom from "./CenterListBottom.vue";
import CenterListBottomSmallDevices from "./CenterListBottomSmallDevices.vue";
const centerData = [
  { id: 1, name: "Overview" },
  { id: 2, name: "Specifications" },
  { id: 3, name: "Download Files" },
];
const leftData = [
  { id: 1, name: "Products" },
  { id: 2, name: "Foundry" },
  { id: 3, name: "Insights" },
  { id: 4, name: "Support" },
];

const rightData = [
  { id: 1, name: "Sustainability" },
  { id: 2, name: "Newsroom" },
  { id: 3, name: "Careers" },
];

const fullData = [...leftData, ...rightData];
</script>
