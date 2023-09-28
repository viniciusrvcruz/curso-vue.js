<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImagem @mudar-imagem="trocarImagem" />
    </div>
</template>
<script>
import MudarImagem from './MudarImagem.vue';

export default {
    name: 'Picture',
    components: {
        MudarImagem
    },
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: 'Vinicius Roberto'
        }
    },
    methods: {
        trocarImagem() {
            this.avatar = this.avatar == "/img/avatar.png" ? "/img/avatar2.png" : "/img/avatar.png"
        }
    }
}
</script>