<template>
  <div>
    <Datepicker class="h40"></Datepicker>
  </div>
</template>
<script>
import Datepicker from "vuejs-datepicker";
export default {
  name: "EzyDate",
  components: { Datepicker },
};
</script>
<style scoped>
.h40 input[type="text"] {
  height: 40px;
}
</style>
