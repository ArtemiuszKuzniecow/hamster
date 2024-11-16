<template>
    <div class="referals">
        <HamsterInvitation />
        <HamsterGift />
        <HamsterButton type="link">
            <span class="referals__more-bonuses">
                MORE BONUSES!
            </span>
        </HamsterButton>
        <HamsterButton type="link">
            <span class="referals__referal-link">
                YOUR REFERAL LINK <HamsterIcon name="copy"/>
            </span>
        </HamsterButton>
        <HamsterFriendsList />
    </div>
</template>

<script setup lang="ts">
import HamsterFriendsList from './HamsterFriendsList.vue';
import HamsterGift from './HamsterGift.vue';
import HamsterInvitation from './HamsterInvitation.vue';
import HamsterButton from './ui/HamsterButton.vue';
import HamsterIcon from './ui/HamsterIcon.vue';
</script>

<style lang="scss" scoped>
.referals {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    margin: 0.875rem 0.4375rem;

    &__more-bonuses {
        color: #81F128;
        text-align: center;
        font-size: 1.25rem;
    }

    &__referal-link {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 1.5rem;
        color: white;
        text-align: center;
        font-size: 1.25rem;
        vertical-align: middle;
    }
}
</style>