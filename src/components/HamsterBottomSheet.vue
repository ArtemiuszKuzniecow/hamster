<template>]
        <div class="bottom-sheet">
            <div class="bottom-sheet__close" @click="close">
                <HamsterIcon name="close-modal" />
            </div>
            <div class="bottom-sheet__title">Claim your rewars</div>
            <div class="bottom-sheet__content">
                <img src="../assets/hamsters.png" alt="hamsters">
                <div class="bottom-sheet__reward">
                    <div class="bottom-sheet__reward_content">
                        <div class="bottom-sheet__reward_description">reward for new friends</div>
                        <div class="bottom-sheet__reward_score">
                            <img src="../assets/dollar.png" alt="dollar" width="16px" height="16px">
                            <div class="bottom-sheet__reward_score-description">12,200</div>
                        </div>
                    </div>
                    <div class="bottom-sheet__reward_content">
                        <div class="bottom-sheet__reward_description">reward for friends level-up</div>
                        <div class="bottom-sheet__reward_score">
                            <img src="../assets/dollar.png" alt="dollar" width="16px" height="16px">
                            <div class="bottom-sheet__reward_score-description">12,200</div>
                        </div>
                    </div>
                </div>
                <div class="bottom-sheet__reward-button">
                    <HamsterButton type="action" @click="close">
                        <span class="bottom-sheet__reward-button_content">
                            Claim
                        </span>
                    </HamsterButton>
                </div>
            </div>
        </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';
import HamsterButton from './ui/HamsterButton.vue';
import HamsterIcon from './ui/HamsterIcon.vue';

type OpenCloseProps = {
    close: () => void;
};

defineProps<OpenCloseProps>(); 
</script>

<style lang="scss">
.bottom-sheet {
    display: flex;
    flex-direction: column;
    justify-content: end;
    border-radius: 1.3125rem 1.3125rem 0rem 0rem;
    background: var(--Pop-up-fill, linear-gradient(180deg, #124682 0%, #0F2C5B 100%));
    box-shadow: 0px -10px 30px 0px #113E76, 0px 30px 20.7px 0px rgba(0, 0, 0, 0.25) inset, 0px 3px 0px 0px #63ADED inset;
    width: 100vw;
    gap: 0.62rem;

    &__content {
        display: flex;
        padding-bottom: 1.5rem;
        flex-direction: column;
        gap: 1.6875rem;
    }

    &__title {
        @include yellowText(28px, center)
    }

    &__close {
        cursor: pointer;
        display: flex;
        height: 24px;
        justify-content: flex-end;
        align-items: flex-start;
        gap: 10px;
        align-self: stretch;
    }

    &__reward {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;

        &-button {
            display: flex;
            flex-direction: row;
            justify-content: center;

          &_content {
              padding: 0px 0.5rem;
              color: #FFF;
              text-shadow: 0px 0.03125rem 0px #1F1F1F;
              -webkit-text-stroke-width: 0.03125rem;
              -webkit-text-stroke-color: var(--Button-stroke, #1F1F1F);
              font-family: "Movavi Grotesque";
              font-size: 1.5rem;
              text-transform: uppercase;
              width: 100%;
          } 
        }

        &_content {
            display: flex;
            flex-direction: row;
            justify-content: center;
            gap: 0.62rem;
        }

        &_description {
            @include whiteText(0.75rem, normal);
            width: 60%;
            text-align: start;
            text-transform: uppercase;
        }

        &_score {
            display: flex;

            &-description {
                @include whiteText(0.75rem, 900);
                width: 20%;
                text-align: start;
                text-transform: uppercase;
            }
        }
    }

    animation: 0.3s ease bottom-sheet-show;

    @keyframes bottom-sheet-show {
        from {
            transform: translateY(100%);     
        }
    }
}
</style>