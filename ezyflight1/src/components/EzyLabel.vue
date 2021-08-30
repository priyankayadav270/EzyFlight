<template>
  <div>
    <label class="bd ma">{{ title }} </label>
  </div>
</template>
<script>
export default {
  name: "EzySwitch",
  props: {
    title: String,
  },
};
</script>
<style scoped>
.ma{
    margin-right: 1rem;
    margin-left:1rem;
}
.bd{
  font-weight: bold !important;
  text-decoration-color:chartreuse !important;
}
</style>
