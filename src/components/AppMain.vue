<script>
import PokemonList from './pokemon/PokemonList.vue'
export default {
    name: 'AppMain',
    components: { PokemonList },
}
</script>

<template>
    <main class="container pb-3">
        <PokemonList />
    </main>
</template>

<style lang="scss" scoped></style>