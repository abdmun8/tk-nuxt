<template>
  <div
    class="
      h-20
      p-5
      bg-gray-200
      position-fixed
      top-0
      shadow-md
      flex
      items-center
    "
  >
    <span class="font-bold">{{ title }}</span>
  </div>
</template>

<script>
export default {
  name: "NavHeader",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
</style>
