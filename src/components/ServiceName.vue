<template>
    <div>
        <b-card class="card" header="Service Name">
            <MyInput title="" placeholder="My Service" subtext="A friendly name, title, date, version or any other short description that helps you recognize the JSON file when opened."></MyInput>
        </b-card>
    </div>
</template>

<script>
    import Vue from "vue";
    import { CardPlugin } from "bootstrap-vue";
    import MyInput from "./MyInput.vue";
    Vue.use(CardPlugin);

    export default {
        name: "ServiceName",
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
        }
    .card > .card-text {
        text-align: left;
        margin: 0px;
        }
</style>
