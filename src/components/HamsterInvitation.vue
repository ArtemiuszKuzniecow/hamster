<template>
    <div class="invitation">
        <div class="invitation__title">invite friends!</div>
        <div class="invitation__description">You and your friend will receive bonuses!</div>
    </div>
</template>

<script setup lang="ts">
</script>

<style lang="scss" scoped>
.invitation {
    &__title {
        @include yellowText(1.5rem, center);
    }

    &__description {
        @include whiteText(0.875rem, normal);
    }
}
</style>