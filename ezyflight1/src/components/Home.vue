<template>
  <div class="bgimage">
    <div class="ui_container mb">
      <div class="mb">
        <EzyLabel title="Welcome To EzyFlight ... Book your ticket here" />
      </div>
      <table class="table">
        <tr class="flex mb">
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Origin" />
              <EzyDropDown />
            </div>
          </td>
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Destination " />
              <EzyDropDown />
            </div>
          </td>
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Round Trip ?" /><EzySwitch />
            </div>
          </td>
          <td><EzyButton title="Search" /></td>
        </tr>
        <tr class="flex mb">
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Number of adults" /><EzyCounter />
              <EzyLabel title="Number of kids ?" /><EzyCounter />
            </div>
          </td>
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Departure Date" /><EzyDate
                placeholder="Departure Date"
              />
            </div>
          </td>
          <td class="col">
            <div class="flex mb">
              <EzyLabel title="Return Date" /><EzyDate
                placeholder="Rerurn Date"
              />
            </div>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
import EzyButton from "./EzyButton.vue";
import EzyCounter from "./EzyCounter.vue";
import EzyDate from "./EzyDate.vue";
import EzyDropDown from "./EzyDropDown.vue";
import EzySwitch from "./EzySwitch.vue";
import EzyLabel from "./EzyLabel.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    EzyButton,
    EzyCounter,
    EzyDate,
    EzyDropDown,
    EzySwitch,
    EzyLabel,
  },
  setup() {
    axios
      .get(
        "https://api-uat-ezycommerce.ezyflight.se/api/v1/Airport/OriginsWithConnections/en-us",
        {
          headers: {
            Authorization: `token ${"Tenant-Identifier:9d7d6eeb25cd6083e0df323a0fff258e59398a702fac09131275b6b1911e202d"}`,
          },
        }
      )
      .then((res) => {
        console.log(res.data);
      })
      .catch((error) => {
        console.error(error);
      });
  },
};
</script>


<style scoped>
.bgimage {
  background-color:turquoise;
}
.table {
  table-layout: fixed;
  width: 100%;
}
.ui_container {
  position: relative;
  padding: 0 24px;
  box-sizing: border-box;
  max-width: 1280px;
  min-height: 2000px;
}
.flex {
  display: flex;
}
.mb {
  margin-bottom: 1rem;
}
.col {
  width: 400px;
  padding-left: 50px;
}
</style>
