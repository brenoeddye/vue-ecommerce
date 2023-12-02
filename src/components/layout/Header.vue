<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    
})
</script>

<template>
    <header class="header">
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

        </div>
    </header>
</template>