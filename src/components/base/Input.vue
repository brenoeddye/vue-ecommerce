<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    props: {
        type: String,
        placeholder: String,

        isSearch: Boolean,
    }
})
</script>

<template>
    <form v-if="isSearch">
        <input class="search" :type="type" :placeholder="placeholder">

        <button class="search__submit">Pesquisar</button>
    </form>
    <input class="search" v-else :type="type" :placeholder="placeholder">
</template>

<style lang="scss">
.search {
    border-radius: 60px;
    border: 1px solid transparent;

    &__submit {
        background: transparent;
        border: 0;
        font-size: 0;
    }
}
</style>