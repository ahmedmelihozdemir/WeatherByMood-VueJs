<template>
    <div class="row mood-list">
        <label class="">Select a mood</label>
        <select v-model="selectedMood" class="form-control">
            <option
                :selected="mood == selectedMood"
                v-for="mood in moods"
                :key="mood"
            >
                {{ mood.name }}
            </option>
        </select>

        <p>Selected Mood: {{ selectedMood }}</p>
        <div v-if="selectedMood == 'sad'">
            <img src="https://picsum.photos/id/171/200/300" alt="" />
        </div>
        <div v-if="selectedMood == 'cheerful'">
            <img src="https://picsum.photos/id/124/200/300" alt="" />
        </div>
        <div v-if="selectedMood == 'romantic'">
            <img src="https://picsum.photos/id/22/200/300" alt="" />
        </div>
        <div v-if="selectedMood == 'gloomy'">
            <img src="https://picsum.photos/id/1019/200/300" alt="" />
        </div>
        <div v-if="selectedMood == 'angry'">
            <img src="https://picsum.photos/id/1025/200/300" alt="" />
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selectedId: null,
            selectedMood: "",
            /* moods: ["sad", "cheerful", "romantic", "gloomy", "angry"], */
            moods: [
                { id: 1, name: "sad" },
                { id: 2, name: "cheerful" },
                { id: 3, name: "romantic" },
                { id: 4, name: "gloomy" },
                { id: 5, name: "angry" },
            ],
        };
    },
};
</script>

<style scoped>
.cards {
    transition: all 0.5s ease;
    margin: 20px;
}
.cards:hover {
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    transition: all 0.5s ease;
}
</style>
