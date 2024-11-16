<template>
    <img :src="source" :alt="`${name}`">
</template>

<script lang="ts" setup>
import { defineProps } from 'vue';

const props = defineProps<{
    name: string;
}>();

const source = require(`@/assets/icons/${props.name}.svg`);
</script>
<style scoped></style>