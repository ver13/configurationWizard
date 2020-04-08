<template>
  <div style="width: 100%">
    <p class="title">{{title}}</p>
    <input type="string" v-model="message" :placeholder="placeholder" />
    <p class="subtext">{{subtext}}</p>
  </div>
</template>

<script>
export default {
  name: "MyInput",
  props: ["title", "placeholder", "subtext"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  text-align: left;
}
input {
  padding: 10px;
  width: 100%;
  box-sizing: border-box;
  color: gray;
  font-size: 12px;
}
.title {
  font-weight: bold;
  margin: 0px;
  font-size: 14px;
}
.subtext {
  margin: 0px;
  color: rgb(160, 160, 160);
  font-size: 12px;
}
</style>
