<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro()">Ativar múltiplos eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data() {
        return {
            multiplos_eventos: 'teste',
            txt1: 'Primeiro evento',
            txt2: 'Segundo evento'
        }
    },
    methods: {
        primeiro(txt) {
            this.multiplos_eventos = txt
        },
        segundo(txt) {
            setTimeout(() => this.multiplos_eventos = txt, 500)
        },
        terceiro() {
            setTimeout(() => this.multiplos_eventos = '', 1500)
        }
    }
}
</script>

<style scoped>
    div  {
        margin: 100px;
    }
</style>