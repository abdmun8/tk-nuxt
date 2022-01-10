<template>
  <div>
    <NavHeader title="Tabungan Kurban" />
    <!-- {{ route?.params?.id }} -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      peserta: [
        {
          nama: "Abdul Munim",
          id: 1,
        },
        {
          nama: "Sayuti",
          id: 2,
        },
      ],
    };
  },
  mounted() {
    this.getPeserta();
  },
  methods: {
    getPeserta() {
      this.$axios.get("https://randomuser.me/api/").then((response) => {
        this.peserta = response.data.results;
      });
    },
  },
};
</script>

<style>
</style>
