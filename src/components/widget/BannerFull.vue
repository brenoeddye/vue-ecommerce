<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    
})
</script>

<template>
    <div class="widget-bannerFull">
        <ul class="widget-bannerFull__images">
            <li>
                <img src="https://via.placeholder.com/1920x680" alt="banner-home-1">
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
.widget-bannerFull {
    &__images {
        li {
            img {
                width: 100%;
            }
        }
    }
}
</style>