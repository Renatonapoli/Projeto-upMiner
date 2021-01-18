<template>
    <div class="cartao">
        <header class="cartao--cabecalho">
            <!-- Cabeçalho do cartão-->
            <img :src="require(`@/assets/${icone}.png`)" alt="Sócio Ambiental">
            <h3>{{ titulo }}</h3>
        </header>
        <div class="cartao--corpo">
            <p>{{ corpo }}</p>
        </div>
        <footer class="cartao--rodape">
            <!-- Rodapé do Cartão -->
            <h3>{{ preco }}</h3>
            <a href="https://uplexis.com.br/">Saiba mais</a>          
        </footer>   
    </div>
</template>

<style lang="scss" scoped>
    @import './Card.scss';
</style>

<script>
export default {
    name: 'Card',
    props: {
        icone: String,
        titulo: String,
        corpo: String,
        preco: String,
        url: String,
    }
}
</script>