<template>
  <div class="w-screen display-flex flex-direction-column">
    <NavHeader title="Tabungan Kurban" />
    <div>
      <div class="overflow-scroll flex-1">
        <ul class="p-2">
          <NuxtLink
            v-for="(item, index) in peserta"
            :key="index"
            :to="`/detail/${index}`"
          >
            <li
              class="
                px-5
                py-3
                bg-white-200
                rounded-md
                shadow-sm
                border-1
                flex flex-row
                justify-between
                mb-2
              "
            >
              <span>{{
                `${item.name.title} ${item.name.first} ${item.name.last}`
              }}</span>
              <span>500</span>
            </li>
          </NuxtLink>
        </ul>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "IndexPage",
  data() {
    return {
      peserta: [],
    };
  },
  mounted() {
    this.getPeserta();
  },
  methods: {
    getPeserta() {
      this.$axios
        .get("https://randomuser.me/api/?results=50")
        .then((response) => {
          this.peserta = response.data.results;
        });
    },
  },
};
</script>
