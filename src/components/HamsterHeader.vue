<template>
    <div class="header">
        <div class="header-container">
            <HamsterIcon name="close" class="header-container__button" />
            <HamsterIcon name="expand" class="header-container__button" />
            <HamsterIcon name="meatballs" class="header-container__button" />
        </div>
        <div class="header-profile">
            <div class="header-container__avatar">
            </div>
            <div class="header-container__counters">
            </div>
            <HamsterIcon name="settings" class="header-container__button" />
        </div>
    </div>

</template>

<script setup>
import HamsterIcon from './ui/HamsterIcon.vue';
</script>

<style lang="scss">
.header {
  &-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 0.75rem; 
    background: linear-gradient(180deg, #2B364D 0%, #131B2D 105.43%);
    border-top: 0.0625rem solid #5E6679;
    margin: 0;
  
    &__button {
      cursor: pointer;
    }

    &__counters {
        background: url("/src/assets/Counters.png");
        width: 75%;
        height: 75%;
    }

    &__avatar { 
        background: url("/src/assets/Avatar.png");
        width: 1.875rem;
        height: 2.5rem;
    }

    &__counters, &__avatar {
        cursor: pointer;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
    }
  }

  &-profile {
    background: linear-gradient(180deg, rgba(26, 54, 98, 0.8) 0%, rgba(23, 49, 92, 0.8) 100%);
    border-bottom: 0.025rem solid rgba(124, 208, 255, 0.4);
    border-radius: 0px 0px 1.125rem 1.125rem;
    display: flex;
    flex-direction: row;
    height: 2.5rem;
    justify-content: space-between;
    align-items: center;
    padding: 0.25rem 0.625rem 0.125rem 0.625rem;
    overflow: hidden;
  }
}

</style>