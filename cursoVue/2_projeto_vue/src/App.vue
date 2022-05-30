<template>
    <div>
        <primeiro-componente></primeiro-componente>
        <p>O dado de app é: {{ testando }}</p>
    </div>
</template>

<script>
import PrimeiroComponente from "./components/PrimeiroComponente.vue";

export default {
    name: "App",
    components: {
        PrimeiroComponente,
    },
    data() {
        return {
            testando: "Testando",
        };
    },
};
</script>
