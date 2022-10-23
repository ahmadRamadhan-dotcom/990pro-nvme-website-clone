<template>
  <footer
    class="bg-[#ffffff] sm:grid sm:place-content-center md:place-content-start justify-center w-full mt-10 pt-6 pb-8 sm:mt-0 sm:pb-8 sm:pt-8 xl:pt-8 xl:pb-4 2xl:place-content-center"
  >
    <div
      class="grid w-11/12 sm:w-full ml-[5%] sm:ml-0 md:ml-[4%] lg:ml-[2%] xl:ml-[7%]"
    >
      <span class="text-[12px] font-normal text-[#757575] font-['SamsungOne']"
        >* All product specifications reflect internal test results and are
        subject to variations by user’s system configuration.
      </span>
      <span class="text-[12px] font-normal text-[#757575] font-['SamsungOne']"
        >* All product images shown are for illustration purposes only and may
        not be an exact representation of the product.
      </span>
      <span class="text-[12px] font-normal text-[#757575] font-['SamsungOne']"
        >* Samsung reserves the right to change product images and
        specifications at any time without notice.
      </span>
    </div>
    <div
      role="breadcumb"
      class="ml-[5%] sm:ml-0 md:ml-[4%] lg:ml-[2%] xl:ml-[2%] mt-9 sm:mt-8 xl:mt-14 flex items-center sm:flex sm:items-center xl:flex xl:items-center md:gap-1 xl:gap-1"
    >
      <span class="text-[#555555] text-[12px] font-['SamsungOne'] font-normal"
        >Home</span
      >
      <img
        src="../assets/icon-bold-navigation-next.svg"
        alt="breadcumb navigation arrow svg"
        class="sm:h-3 xl:h-3"
      />
      <span class="text-[#555555] text-[12px] font-['SamsungOne'] font-normal"
        >Consumer Storage</span
      >
      <img
        src="../assets/icon-bold-navigation-next.svg"
        alt="breadcumb navigation arrow svg"
        class="sm:h-3 xl:h-3"
      />
      <span class="text-[#555555] text-[12px] font-['SamsungOne'] font-normal"
        >Internal SSD</span
      >
      <img
        src="../assets/icon-bold-navigation-next.svg"
        alt="breadcumb navigation arrow svg"
        class="sm:h-3 xl:h-3"
      />
      <span class="font-bold font-['SamsungOne'] text-[#555555] text-[12px]"
        >990 PRO</span
      >
    </div>
    <div>
      <FooterCollapse :footerData="footerData" />
      <div
        class="hidden sm:hidden md:ml-[4%] lg:ml-[2%] md:mt-7 md:grid md:grid-cols-3 md:gap-12 lg:flex lg:gap-10 xl:gap-20"
      >
        <div
          v-for="(data, index) in footerData"
          :key="index"
          class="md:w-32 xl:w-26"
        >
          <span
            class="font-bold xl:text-sm font-['SamsungOne'] text-[#555555]"
            >{{ data.title }}</span
          >
          <ul class="grid gap-2 md:gap-1 xl:gap-1 mt-4">
            <li
              v-for="(content, index) in data.content"
              :key="index"
              class="font-['SamsungOne'] font-normal text-[12px] text-[#555555]"
            >
              <a href="">
                {{ content }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import FooterCollapse from "./FooterCollapse.vue";
const footerData = [
  {
    id: 1,
    title: "Products",
    content: [
      "DRAM",
      "SSD",
      "eStorage",
      "MCP",
      "Consumer Storage",
      "Processor",
      "Image Sensor",
      "Display IC",
      "Security Solution",
      "Power IC",
      "LED",
    ],
  },
  {
    id: 2,
    title: "Foundry",
    content: [
      "Overview",
      "Process Technology",
      "Advanced Package",
      "SAFE TM",
      "Manufacturing",
      "Application Specific Service",
      "Foundry Event",
    ],
  },
  {
    id: 3,
    title: "Insights",
    content: [
      "5G",
      "AI",
      "Big Data",
      "Image Processing",
      "PIM",
      "EUV",
      "Smartphone",
      "Server & Network",
      "PC",
      "TV & Gaming",
      "Automotive",
    ],
  },
  {
    id: 4,
    title: "Support",
    content: [
      "Overview",
      "Product Finder",
      "Technical Resources",
      "Consumer Storage Support",
      "Fabrication Process",
      "Dictionary",
      "Global Network",
      "Contact Us",
      "B2B Workplace",
    ],
  },
  {
    id: 5,
    title: "Sustainability",
    content: [
      "Highlights",
      "Environment",
      "Labor & Human Rights",
      "Corporate Citizenship",
      "Sustainable Supply Chan",
    ],
  },
  {
    id: 6,
    title: "About Us",
    content: [
      "Business Area",
      "Executive",
      "Location",
      "History",
      "Careers",
      "News",
      "Event",
      "Tech Blog",
      "Investor Blog",
      "Investor Relations",
      "Ethics",
    ],
  },
];

const bottomFooterData = [
  { id: 1, name: "Privacy" },
  { id: 2, name: "Legal" },
  { id: 3, name: "Cookies" },
  { id: 4, name: "Accebility" },
  { id: 5, name: "Sitemap" },
];

export default {
  name: "Footer",
  data() {
    return {
      footerData,
      bottomFooterData,
    };
  },
  components: { FooterCollapse },
};
</script>
