<template>
  <div>
    <dropdown
      class="custom-select"
      :options="{ optionList }"
      :selected="{ selectedOption }"
      :placeholder="'Select airport'"
      :closeOnOutsideClick="true"
    />
  </div>
</template>
<script>
import dropdown from "vue-dropdowns";
export default {
  name: "EzyDropDown",
  components: { dropdown },
  props: {
    optionList: Array,
    selectedOption: {},
  },
};
</script>


<style scoped>
.custom-select {
  position: relative;
  font-family: Arial;
  border: 1px solid !important;
  border-radius: 5px !important;
}

.custom-select select {
  display: none;
}


.custom-select li {
  background-image: none !important;
}

.select-selected {
  background-color: DodgerBlue;
}

.select-selected:after {
  position: absolute;
  content: "";
  top: 14px;
  right: 10px;
  width: 0;
  height: 0;
  border: 6px solid transparent;
  border-color: #fff transparent transparent transparent;
}

.select-selected.select-arrow-active:after {
  border-color: transparent transparent #fff transparent;
  top: 7px;
}

.select-items div,
.select-selected {
  color: #ffffff;
  padding: 8px 16px;
  border: 1px solid transparent;
  border-color: transparent transparent rgba(0, 0, 0, 0.1) transparent;
  cursor: pointer;
}

.select-items {
  position: absolute;
  background-color: DodgerBlue;
  top: 100%;
  left: 0;
  right: 0;
  z-index: 99;
}

.select-hide {
  display: none;
}

.select-items div:hover,
.same-as-selected {
  background-color: rgba(0, 0, 0, 0.1);
}

.btn-group {
  margin: 0 !important;
  height: 37px !important;
}

.btn-group li {
  min-width: 145px !important;
  background-image: none !important;
  background: none !important;
}

.caret {
  top: 0px !important;
}
</style>
