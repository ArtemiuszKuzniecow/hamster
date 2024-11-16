<template>
    <div class="gift">
        <HamsterIcon name="gift" />
        <div class="gift__container">
            <div class="gift__title">Invite friend</div>
            <div class="gift__description">
                <div class="gift__bonuses">
                    <img src="../assets/dollar.png" alt="bonus" width="16" height="16">
                    <span class="gift__bold">+500</span>
                </div>
                <div class="gift__normal">For you and your friends</div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import HamsterIcon from './ui/HamsterIcon.vue';
</script>

<style lang="scss" scoped>
.gift {
    display: flex;
    padding: 0.25rem 1.5rem;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    background: linear-gradient(90deg, rgba(48, 129, 180, 0.00) 0%, #215789 34.03%, #215789 78.06%, rgba(25, 72, 140, 0.00) 100%);

    &__container {
        display: flex;
        flex-direction: column;
        gap: 0.625rem;
    }

    &__bonuses {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
        flex-direction: row;
    }

    &__description {
        display: flex;
        flex-direction: row;
        gap: 0.5rem;
    }

    &__normal {
        @include whiteText(0.75rem, normal);
    }

    &__bold {
        @include whiteText(0.75rem, 900);
    }

    &__title {
        @include yellowText(0.875rem, start);
    }
}
</style>