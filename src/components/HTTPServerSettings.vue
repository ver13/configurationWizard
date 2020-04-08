<template>
  <div>
    <b-card class="card" header="HTTP Server settings">
      <MyInput title="Port" placeholder="8080" subtext="Port where AVA Framework Server listens to connections, defaults to 8080. The port can also be specified at startup time with the flag -p"></MyInput>

      <b-card class="secondCard" header="Enable HTTPS">
        <input type="checkbox" id="checkbox" v-model="checked" />
        <p>Mark this option to enable TLS in the listening port</p>
      </b-card>

      <div class="doubleColumn">
        <div class="firstColumn">
          <MyInput title="HTTP Read Timeout" placeholder="0s" subtext="Maximum duration for reading the entire HTTP request, including the body"></MyInput>
        </div>
        <div class="secondColumn">
          <MyInput title="HTTP Write Timeout" placeholder="0s" subtext="Maximum duration before timing-out writes of the response"></MyInput>
        </div>
      </div>
      <div class="doubleColumn">
        <div class="firstColumn">
          <MyInput title="HTTP Idle Timeout" placeholder="0s" subtext="Maximum amount of time to wait for the next request when keepalives are enabled"></MyInput>
        </div>
        <div class="secondColumn">
          <MyInput title="HTTP Read Header Timeout" placeholder="0s" subtext="Maximum time spent to read headers"></MyInput>
        </div>
      </div>
    </b-card>
  </div>
</template>

<script>
import Vue from "vue";
import { CardPlugin } from "bootstrap-vue";
import MyInput from "./MyInput.vue";
Vue.use(CardPlugin);

export default {
  name: "HTTPServerSettings",
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
  padding: 10px;
}

.card > .card-text {
  margin: 0px;
}

.secondCard {
  margin-top: 20px;
  border: 1px solid #20a1fd;
}

.secondCard > .card-header {
  color: white;
  background-color: #20a1fd;
}

.secondCard > .card-body {
  display: flex;
  padding: 5px;
  text-align: left;
}
.secondCard > .card-body > input {
  margin-top: auto;
  margin-bottom: auto;
  margin-right: 10px;
  margin-left: 10px;
}

.doubleColumn {
  display: flex;
  margin-top: 20px;
}

.doubleColumn > .firstColumn {
  width: 48%;
  padding-right: 2%;
}

.doubleColumn > .secondColumn {
  width: 48%;
  padding-left: 2%;
}
</style>
