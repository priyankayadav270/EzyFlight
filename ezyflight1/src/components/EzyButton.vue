<template>
  <div class="left">
    <button @click="searchData">{{ title }}</button>
  </div>
</template>
<script>
export default {
  name: "EzyButton",
  props: {
    title: String,
  },
  methods: {
    searchData: function () {
    },
  },
};
</script>

<style scoped>
.left{
  text-align: right;
}
</style>
