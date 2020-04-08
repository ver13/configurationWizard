<template>
  <div id="app">
    <div style="width: 50%">
      <ServiceName></ServiceName>
      <HTTPServerSettings></HTTPServerSettings>
      <TimeoutsAndTTL></TimeoutsAndTTL>
    </div>
  </div>
</template>

<script>
import ServiceName from "./components/ServiceName.vue";
import HTTPServerSettings from "./components/HTTPServerSettings.vue";
import TimeoutsAndTTL from "./components/TimeoutsAndTTL.vue";

export default {
  name: "App",
  components: {
    ServiceName,
    HTTPServerSettings,
    TimeoutsAndTTL
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>
