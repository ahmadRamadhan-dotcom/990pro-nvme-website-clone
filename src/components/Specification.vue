<template>
  <div
    class="bg-[#1a1a1c] flex justify-center sm:pb-32 xl:pb-24 mt-20 sm:mt-20 xl:mt-36"
  >
    <div
      class="grid place-content-center sm:w-11/12 md:w-full xl:w-full place-items-center sm:mt-20 xl:mt-16"
    >
      <span
        class="font-['Samsung_Sharp_Sans'] font-bold sm:text-2xl md:text-[28px] lg:text-4xl"
        >Specifications
      </span>
      <div
        class="sm:mt-20 xl:mt-24 sm:grid sm:grid-cols-2 sm:gap-24 md:flex lg:gap-[100px] xl:flex xl:gap-[160px]"
      >
        <div
          v-for="(data, index) in quickSpecData"
          :key="index"
          class="grid place-content-start text-center place-items-start"
        >
          <img
            :src="'/src/assets/' + data.image"
            alt=""
            class="sm:h-10 md:h-12 xl:h-12"
          />
          <span
            class="sm:mt-5 xl:mt-6 font-['SamsungOne'] font-bold sm:text-[12px] md:text-[15px] lg:text-lg"
            >{{ data.name }}</span
          >
          <span
            class="sm:mt-1 xl:mt-1 font-['SamsungOne'] font-normal sm:text-[12px] xl:text-[12px]"
            >{{ data.content }}</span
          >
        </div>
      </div>
      <button
        aria-label="this button for show detail specification of this nvme"
        class="inline-flex sm:mt-10 xl:mt-12 items-center justify-center sm:py-1 sm:px-5 xl:px-5 xl:py-1.5 text-sm font-bold leading-6 font-['SamsungOne'] whitespace-no-wrap bg-white border border-gray-200 rounded-full text-[#000000] shadow-sm hover:bg-gray-50 focus:outline-none focus:shadow-none"
      >
        View more
      </button>
    </div>
  </div>
</template>

<script setup>
const quickSpecData = [
  { id: 1, name: "Form Factor", image: "spec-form-factor.png", content: "M.2" },
  { id: 2, name: "Capacity", image: "spec-capacity.png", content: "1TB, 2TB" },
  {
    id: 3,
    name: "Sequential Read Speed",
    image: "spec-sequential-read-speed.png",
    content: "Up to 7,450 MB/s",
  },
  {
    id: 4,
    name: "Sequential Write Speed",
    image: "spec-sequential-write-speed.png",
    content: "up to 6,900 MB/s",
  },
];
</script>
