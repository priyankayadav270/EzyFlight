<template>
  <div class="w150">
    <label id={idStr} class="bd ma">{{ title }} </label>
  </div>
</template>
<script>
export default {
  name: "EzySwitch",
  props: {
    title: String,
    idStr: String,
  },
};
</script>
<style scoped>
.ma {
  margin-right: 1rem;
  margin-left: 1rem;
}
.bd {
  font-weight: bold !important;
  text-decoration-color: chartreuse !important;
}
.w150{
  width: 170px;
}
</style>
