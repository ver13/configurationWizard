<template>
  <div>
    <b-card class="card" header="Timeouts and TTL">
      <p>All settings below are used across all backends unless overridden explicitly in each endpoint.</p>

      <MyInput title="Backend Timeout" placeholder="3000ms" subtext="Default timeout for all connections against your backends, including the time spent in the whole pipe. This value can be overridden later on specific endpoints."></MyInput>

      <MyInput title="Default Cache TTL" placeholder="300s" subtext="Value must be an integer expressing the number of seconds."></MyInput>

      <p>The time the service considers the origin is still valid. Applies to GET requests only. The service does not cache anything but expedites the headers for proxies to do the caching (e.g., a Varnish server).</p>
    </b-card>
  </div>
</template>

<script>
import Vue from "vue";
import { CardPlugin } from "bootstrap-vue";
import MyInput from "./MyInput.vue";
Vue.use(CardPlugin);

export default {
  name: "TimeoutsAndTTL",
  components: {
    MyInput
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  box-shadow: 0px 0px 4px 1px #80808078;
  border-radius: 5px;
  border-top: 3px solid #20a1fd;
}
.card > .card-header {
  border-bottom: 1px solid #00000014;
  text-align: left;
  font-weight: bold;
  padding: 10px;
  }
.card > .card-body {
  text-align: left;
  padding: 10px;
  font-size: 13px;
  }
.card > .card-text {
  text-align: left;
  margin: 0px;
  }
</style>
