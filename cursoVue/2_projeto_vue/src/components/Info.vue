<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades.</p>
        <p>Uilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Vue</li>
        </ul>
        <div>
            <button @click="showEmail">{{textoBotao}}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from "./Picture.vue"

export default {
    name: "Info",
    components: {
        Picture
    },

    data() {
        return {
            esta_trabalhando: true,
            mostrar_email: false,
            email: "caio.dutra@gmail.com",
            meu_link: "https://github.com/caiodutra08 ",
            textoBotao: "Mostrar email"
        }
    },
    methods : {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email) {
                this.textoBotao = "Mostrar email"
            } else {
                this.textoBotao = "Esconder email"
            }
        }
    }
};
</script>