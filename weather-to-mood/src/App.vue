<template>
    <component :is="componentId">
        <div class="container">
            <button class="btn" @click="goToWeatherCards">
                Weather By Conditions
            </button>
        </div>
    </component>
</template>

<script>
import WeatherCards from "./components/WeatherCards.vue";

export default {
    components: {
        WeatherCards,
    },
    data() {
        return {
            componentId: "App.vue",
        };
    },
    methods: {
        goToWeatherCards() {
            this.componentId = "WeatherCards";
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
body{
  background-color: cornsilk;
}
.btn{
  background-color: #90bce9;
  color: aliceblue;
  border-radius: 10px;
}
</style>
