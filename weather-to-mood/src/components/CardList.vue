<template>
    <div class="row mb-5 mt-5">
        <div class="cards col">
            <img :src="card.image" alt="" />
        </div>
    </div>
</template>

<script>
export default {
    props: ["card"],
};
</script>

<style scoped>
.cards {
    border-radius: 10px;
    transition: all 0.5s ease;
    margin: 30px;
}
.cards:hover {
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    transition: all 0.5s ease;
}
</style>
