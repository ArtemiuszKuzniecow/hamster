<template>
    <div class="friend-list">
        <div class="friend-list-description">List of your friends</div>
        <HamsterIcon name="refresh" class="friend-list-refresh" />
    </div>
    <HamsterButton type="action" @click="openModal">
        <span class="friend-list__reward-button">
            Claim all rewards
        </span>
    </HamsterButton>
    <HamsterDropdown :items="players" />
    <Teleport to="body">
      <HamsterModal ref="modal">
        <HamsterBottomSheet :close="closeModal"/>
      </HamsterModal>
    </Teleport>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import HamsterBottomSheet from './HamsterBottomSheet.vue';
import HamsterModal from './HamsterModal.vue';
import HamsterButton from './ui/HamsterButton.vue';
import HamsterDropdown from './ui/HamsterDropdown.vue';
import HamsterIcon from './ui/HamsterIcon.vue';

const modal = ref<InstanceType<typeof HamsterModal> | null>(null);

const openModal = () => {
  modal.value?.showModal();
};

const closeModal = () => {
  modal.value?.handleClose();
};

const players = [
    {
        name: 'Anastasia V has joined the game',
        score: 1
    },
    {
        name: 'Dmitro',
        score: 2
    },
    {
        name: 'Diana',
        score: 33
    },
    {
        name: 'Nikita',
        score: 12
    },
    {
        name: 'Nikita',
        score: 2
    },
    {
        name: 'Nikita',
        score: 4
    },
    {
        name: 'Nikita',
        score: 124
    }
]
</script>

<style scoped lang="scss">
.friend-list {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 2.125rem;
    @include whiteTextOutlined(1.25rem);

    &-refresh {
        cursor: pointer;
    }

    &__reward-button {
        padding: 0px 0.5rem;
        color: #FFF;
        text-shadow: 0px 0.03125rem 0px #1F1F1F;
        -webkit-text-stroke-width: 0.03125rem;
        -webkit-text-stroke-color: var(--Button-stroke, #1F1F1F);
        font-family: "Movavi Grotesque";
        font-size: 1.5rem;
        text-transform: uppercase;
    }
}
</style>