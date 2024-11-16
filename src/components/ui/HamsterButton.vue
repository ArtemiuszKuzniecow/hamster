<template>
    <button
        :class="['button', type === 'link' ? 'button--link' : 'button--action']"
        @click="onClick"
    >
        <slot></slot>
    </button>
</template>

<script lang="ts" setup>
import { defineProps } from 'vue';

defineProps<{
    type?: 'action' | 'link';
    onClick?: () => void;
}>();
</script>

<style lang="scss" scoped>
.button {
    cursor: pointer;
    display: flex;
    height: 2.5rem;
    min-height: 1.875rem;
    padding: 0 1.5rem;
    justify-content: center;
    align-items: center;
    gap: 0.6875rem;
    border-radius: 1.125rem;

    &--action {
        background: linear-gradient(180deg, #FACF45 0%, #D5A512 100%);
        box-shadow: 
            0px 0.0625rem 0.0625rem 0px rgba(0, 0, 0, 0.25), 
            0px 0.125rem 0px 0px #FFEEBA inset, 
            0px -0.125rem 0px 0px #7A5D00 inset;
    }

    &--link {
        border: 0.125rem solid #7DD0FF;
        background: linear-gradient(90deg, #134381 0%, #1E5EA3 48.5%, #134381 100%);
        box-shadow: 0px 0.0625rem 0.625rem 0px rgba(125, 208, 255, 0.50);
        color: #fff;
        font-size: 0.875rem;
        font-weight: 900;
        text-align: center;
        padding: 0.125rem 1rem;
    }
}
</style>
