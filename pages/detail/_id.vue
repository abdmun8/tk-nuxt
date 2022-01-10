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
    console.log(this.$route.params.id);
  },
};
</script>

<style>
</style>
