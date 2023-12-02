<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    props: {
        changeTheme: String
    },
    methods: {
        returnTheme() {
            this.$emit('changeTheme');
        }
    }
})
</script>

<template>
    <header class="header">
        <div class="header__content">
            <div class="header__logo">
                <h1 class="header__logo--image">Brein Store</h1>
            </div>
            <div class="header__search">
                <baseInput 
                    type="text"
                    placeholder="Estou procurando..." 
                    isSearch />
            </div>
            <div class="header__user">
                <button @click="returnTheme">changeTheme</button>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
.header {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: var(--tertiary);
    transition: all .3s linear;

    &__content {
        @include container;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
</style>