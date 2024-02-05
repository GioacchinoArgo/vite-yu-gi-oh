<script>
export default {
    name: 'PokemonCard',
    props: {
        name: String,
        imageUrl: String,
        type1: String,
        type2: String
    }
};
</script>

<template>
    <div class="pokemon-card text-center p-2">
        <img class="img-fluid shadow mb-3 rounded mix-blend-mode" :src="imageUrl" :alt="name">
        <div class="pokemon-details">
            <div class="pokemon-name">{{ name }}</div>
            <div class="pokemon-types">{{ type1 }}</div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
img {
    width: 100% auto;
}

.pokemon-card {
    cursor: pointer;
    background-color: #fff;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;

    &:hover {
        transform: scale(1.05);
    }

    .pokemon-name {
        font-size: 20px;
        font-weight: bold;
        margin-bottom: 5px;
        color: #333;
    }

    .pokemon-types {
        font-weight: 500;
        font-size: 14px;
        color: #555;
    }
}
</style>