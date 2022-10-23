<template>
  <div v-for="(data, index) in footerData" :key="index">
    <div @-click="handleActive(data.id)" class="md:hidden flex justify-between">
      <span
        class="sm:leading-[60px] font-bold font-['SamsungOne'] text-[#555555]"
        >{{ data.title }}</span
      >
      <button>
        <img
          :class="isActive ? 'rotate-180' : ''"
          src="../assets/icon-bold-navigation-open-down.svg"
          alt=""
        />
      </button>
    </div>
    <ul v-show="isActive === data.id" class="grid gap-1 xl:mt-3">
      <li
        v-for="(content, index) in data.content"
        :key="index"
        class="font-['SamsungOne'] font-normal p-4 text-[14px] text-[#555555]"
      >
        <a href="">
          {{ content }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FoterCollapse",
  data() {
    return {
      isActive: null,
    };
  },
  props: {
    footerData: Array,
  },
  methods: {
    handleActive(id) {
      if (this.isActive === id) {
        this.isActive = null;
      } else {
        this.isActive = id;
      }
    },
  },
};
</script>
