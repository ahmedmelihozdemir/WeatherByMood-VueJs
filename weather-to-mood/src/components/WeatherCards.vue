<template>
    <div class="weather-area">
        <h1 class="mb-2 text-center">Weather By Condition</h1>
        <h4 class="mb-2">Chose a condition.</h4>
        <div class="container">
            <SelectMood></SelectMood>
        </div>
        <div class="container">
            <CardList
                :class="{ shadow: selectedCard == card.id }"
                @click="selectedCard = card.id"
                v-for="card in cards"
                :key="card"
                :card="card"
                :selectedId="selectedId"
            ></CardList>
        </div>
        <p>{{ selectedCard }}</p>
    </div>
</template>

<script>
import CardList from "./CardList.vue";
import SelectMood from "./SelectMood.vue";

export default {
    components: {
        CardList,
        SelectMood,
    },
    data() {
        return {
            selectedCard: null,
            cards: [
                {
                    id: 1,
                    component: "app-card",
                    image: "https://picsum.photos/id/29/200/300",
                },
                {
                    id: 2,
                    component: "app-card",
                    image: "https://picsum.photos/id/555/200/300",
                },
                {
                    id: 3,
                    component: "app-card",
                    image: "https://picsum.photos/id/235/200/300",
                },
                {
                    id: 4,
                    component: "app-card",
                    image: "https://picsum.photos/id/85/200/300",
                },
            ],
        };
    },
    props:["selectedId"],
};
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
h1 {
    font-size: 2.5rem;
    color: rosybrown;
}
.shadow {
    border-radius: 10px;
    background-color: rosybrown;
    box-shadow: 0 0 10px rgba(85, 13, 167, 0.5);
    transition: 0.5s ease;
}
</style>
