<template>
    <div>
        <h1>Meu nome é: {{ nome }}</h1>
    </div>
</template>

<script>
export default {
    name: "LifeCycle",
    data: function () {
        return {
            nome: "Ainda não sei",
        };
    },
    created() {
        setTimeout(() => {
            this.nome = "Caio";
        }, 1000);
    },
    mounted() {
        setTimeout(() => {
            this.nome = "Caio Busarello Dutra";
        }, 2000);
    },
};
</script>
