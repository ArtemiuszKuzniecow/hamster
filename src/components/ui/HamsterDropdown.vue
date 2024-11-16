<template>
  <div class="dropdown">
    <div class="dropdown-item__container" v-for="(item) in items" :key="item.name" :name="item.name"
      :score="item.score">
      <img src="../../assets/questionMark.png" alt="questionMark">
      <span class="dropdown-item__name">{{ item.name }}</span>
      <div class="dropdown-item__score">
        <HamsterIcon name="union"/>
        <span class="dropdown-item__score_description">{{ item.score }} lvl</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';
import HamsterIcon from './HamsterIcon.vue';
defineProps<{
  items: { name: string; score: number }[];
}>();
</script>

<style lang="scss" scoped>
.dropdown {
  display: flex;
  max-height: 27.5rem;
  padding: 1.25rem 0.25rem 0.375rem 0.25rem;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.75rem;
  border-right: 0.0625rem solid #3579B5;
  border-bottom: 0.0625rem solid #3579B5;
  border-left: 0.0625rem solid #3579B5;
  background: radial-gradient(51.09% 70.69% at 50% 52.89%, #3081B4 0%, #19488C 100%);
  box-shadow: 0px 0.25rem 0.28125rem 0px rgba(0, 3, 6, 0.50) inset;

  &-item {
    &__container {
      display: flex;
      max-height: 27.5rem;
      padding: 0.375rem 0.25rem;
      justify-content: stretch;
      align-items: center;
      gap: 0.5rem;
      align-self: stretch;
      border-bottom: 0.0625rem solid rgba(167, 222, 253, 0.00);
      background: radial-gradient(51.09% 70.69% at 50% 52.89%, #3081B4 0%, #19488C 100%);
      @include whiteTextOutlined(0.875rem);
    }

    &__score {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 0.25rem;

      &_description {
        min-width: 3rem;
      }
    }

    &__name {
      width: 100%;
    }
  }
}

</style>