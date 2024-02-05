<script>
import { store } from '../../assets/data/store.js';
import PokemonCard from '../../components/pokemon/PokemonCard.vue';
export default {
    name: 'PokemonList',
    data: () => ({ store }),
    components: { PokemonCard },
};
</script>

<template>
    <section id="pokemon" class="my-5">
        <div class="row g-4 row-cols-2 row-cols-md-3 row-cols-lg-4 align-items-center">
            <div class="col" v-for="pokemon in store.pokemons" :key="pokemon.id">
                <PokemonCard :name="pokemon.name" :imageUrl="pokemon.imageUrl" :type1="pokemon.type1"
                    :type2="pokemon.type2" />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped></style>