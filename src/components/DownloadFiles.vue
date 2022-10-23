<template>
  <div class="flex justify-center mt-20 sm:mt-20 sm:pb-20 xl:mt-10 xl:pb-20">
    <div class="xl:mt-16 grid w-11/12 sm:w-[95%] lg:w-4/5 xl:w-7/12">
      <span
        class="font-['Samsung_Sharp_Sans'] text-center font-bold text-[28px] sm:text-[28px] lg:text-4xl"
        >Related Resources</span
      >
      <div
        v-for="(data, index) in resourceData"
        id="resource-data"
        :key="index"
        :class="showMenu ? (data.show = true) : ''"
        v-show="data.show"
        class="xl:pb-5 flex items-end justify-between sm:flex sm:items-end md:items-center sm:justify-between xl:flex xl:items-center xl:justify-between mt-10 sm:mt-10 xl:mt-10"
      >
        <div
          class="flex items-center gap-5 sm:flex sm:items-center sm:gap-6 xl:flex xl:gap-5 xl:items-center"
        >
          <img
            class="h-24 sm:h-24 lg:h-32"
            :src="'/src/assets/' + data.image"
            alt="cool image of related resources of samsung 990 pro nvme m.2 SSD"
          />
          <div class="grid gap-1">
            <span
              id="name"
              class="font-bold font-['Samsung_Sharp_Sans'] text-sm sm:text-sm md:text-base lg:text-lg"
              >{{ data.name }}
            </span>
            <span
              id="type"
              class="font-bold font-['SamsungOne'] sm:text-[12px] sm:text-sm xl:text-sm"
              >{{ data.type }}
            </span>
            <span
              id="version"
              class="font-normal font-['SamsungOne'] text-[12px] text-[#aaaaaa]"
              >{{ data.version }}
            </span>
          </div>
        </div>
        <p
          class="font-bold font-['SamsungOne'] text-sm cursor-pointer flex gap-2 items-center"
        >
          <a :href="data.href">Download</a>
          <img
            src="../assets/icon-bold-action-download-w.svg"
            alt="icon download"
          />
        </p>
      </div>
      <button
        @click="showMenu = true"
        :class="showMenu ? 'hidden' : 'inline-flex'"
        aria-label="this button for show detail specification of resource-data"
        class="mt-12 sm:mt-10 xl:mt-12 items-center justify-center w-[106px] h-[42px] sm:w-[106px] sm:h-[42px] mx-auto sm:mx-auto text-sm font-bold leading-6 font-['SamsungOne'] whitespace-no-wrap bg-white border border-gray-200 rounded-full text-[#000000] shadow-sm hover:bg-gray-50 focus:outline-none focus:shadow-none"
      >
        View more
      </button>
    </div>
  </div>
</template>

<script>
const resourceData = [
  {
    id: 1,
    image: "990-pro-series_brochure.webp",
    name: "990 PRO Series Brochure",
    type: "Brochure",
    version: "Version 1.0",
    href: "https://download.semiconductor.samsung.com/resources/brochure/990_PRO_Series_Brouchure_Web_Version_1.0.pdf",
    show: true,
  },
  {
    id: 2,
    image: "990-pro_datasheet.webp",
    name: "Samsung NVME SSD 990 PRO Datasheet",
    type: "Datasheet",
    version: "Version 1.0",
    href: "https://download.semiconductor.samsung.com/resources/data-sheet/Samsung_NVMe_SSD_990_PRO_Datasheet_Rev.1.0.pdf",
    show: true,
  },
  {
    id: 3,
    image: "install_default_img.webp",
    name: "Magician Software",
    type: "Software Resource",
    version: "Version 7.2",
    href: "https://download.semiconductor.samsung.com/resources/software-resources/Samsung_Magician_installer_Official_7.2.0.930.zip",
    show: true,
  },
  {
    id: 4,
    image: "samsung_magician_7_0_1_installation_guide_v1.1_thumb.webp",
    name: "Magician Software Installation Guide",
    type: "Software Resource",
    version: "Version 7.2",
    href: "https://download.semiconductor.samsung.com/resources/software-resources/Samsung_Magician_7_2_0_Installation_Guide.pdf",
    show: false,
  },
  {
    id: 5,
    image: "open_source_announcement_7_0_0_v1.0_thumb.webp",
    name: "Magician Software Open Source Announcement",
    type: "Product Guide",
    version: "Version 1.0",
    href: "https://semiconductor.samsung.com/resources/product-guide/Open_Source_Announcement_7_0_0_v1.0.pdf",
    show: false,
  },
];

export default {
  name: "DownloadFiles",
  data() {
    return {
      resourceData,
      showMenu: false,
    };
  },
};
</script>

<style scoped>
#resource-data {
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}
</style>
