<template>
    <header id="cabecalho">
        <img id="cabecalho--fundo" v-bind:src="require(`@/assets/${imagemAtual}`)" />

        <div id="cabecalho--top">
            <img id="cabecalho--logo" src="@/assets/logo_upminer.png" />

            <h1 id="cabecalho--titulo">
                Histórico Empresarial
            </h1>
        </div>

        <div id="cabecalho--descricao">
            O aplicativo histórico empresarial permite ao usuário ter acesso a todos<br>os fatos e acontecimentos relevantes de uma empresa desde seu ano<br>de fundação.
        </div>

        <div id="cabecalho--preco">
            <span id="cifrao">R$</span> 40,00
            <a id="cabecalho--saibaMais">
                Saiba mais
            </a>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: () => ({
        imagens: ['imagemBanner.jpg', 'imagemBanner_1.png'],
        imagemAtual: null,
        indice: 1,
    }),
    mounted() {
        // Inicialização...
        if (!this.imagemAtual && this.imagens) {
            this.imagemAtual = this.imagens[this.indice];
        }

        setInterval(() => {
            if (this.indice < this.imagens.length - 1) {
                this.indice += 1;
            } else {
                this.indice = 0;
            }

            this.imagemAtual = this.imagens[this.indice];
        }, 3000);
    }
}
</script>

<style lang="scss" scopes>
    @import "./Header.scss";
</style>