<template>
    <li>
        <img src="@/assets/globe-solid.png">
        <p>{{ titulo }}</p>
    </li>
</template>

<style lang="scss" scoped>
    @import './Categoria.scss';
</style>

<script>
export default {
    name: 'Categoria',
    props: {
        icone: String,
        titulo: String,
        chave: String,
    },
}
</script>