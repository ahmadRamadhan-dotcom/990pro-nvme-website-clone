<template>
  <div
    class="bg-[#000000] h-[35vh] sm:h-[30vh] md:h-[30vh] lg:h-[45vh] flex justify-center items-center"
  >
    <div
      class="grid place-content-center place-items-center sm:place-content-center sm:place-items-center"
    >
      <h2
        class="text-2xl sm:text-2xl md:text-[34px] lg:text-5xl text-center font-['Samsung_Sharp_Sans'] font-bold"
      >
        The Ultimate SSD
      </h2>
      <span
        class="w-11/12 mt-8 text-center font-normal font-['SamsungOne'] text-sm sm:text-sm md:text-[15px] lg:text-lg xl:hidden"
      >
        Reach max performance of PCIe<sup>®</sup> 4.0. Experience
        longer-lasting, opponent-blasting speed The in-house controller's smart
        heat control delivers supreme power efficiency <br />
        while mantaining ferocious speed and perfomance, to always keep you at
        the top of your game.
      </span>
      <div class="text-center xl:mt-7 grid">
        <span
          v-for="(data, index) in overviewData"
          :key="index"
          class="hidden sm:hidden xl:block font-normal font-['SamsungOne'] text-lg"
          >{{ data.content }}
        </span>
        <span
          class="hidden sm:hidden md:block font-normal font-['SamsungOne'] text-[12px] md:mt-4 xl:mt-8 text-[#f8f8f8]"
        >
          * PCIe 4.0’s best theoretical sequential read is 8000 MB/s - 990 PRO
          reaches 7,450 MB/s as of Q3, 2022.
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const overviewData = [
  { id: 1, content: "Reach max performance of PCIe® 4.0." },
  { id: 2, content: "Experience longer-lasting, opponent-blasting speed" },
  {
    id: 3,
    content:
      "The in-house controller's smart heat control delivers supreme power efficiency",
  },
  { id: 4, content: "while mantaining ferocious speed and perfomance," },
  { id: 5, content: "to always keep you at the top of your game." },
];
</script>
