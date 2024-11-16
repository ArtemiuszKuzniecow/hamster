<template>
  <transition name="modal-fade" @after-leave="handleClose">
  <div v-if="visible" class="modal-overlay" @click="handleClose">
      <div class="modal" @click.stop>
        <slot></slot>
      </div>
    </div>
  </transition>
</template>

<script lang="ts" setup>
import { ref, defineExpose } from 'vue';

const visible = ref(false);

const showModal = () => {
  visible.value = true;
};

const handleClose = () => {
  visible.value = false;
};

defineExpose({
  showModal,
  handleClose
});
</script>

<style lang="scss">
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.50);;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  z-index: 1000;
}

.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.3s linear;
}

.modal-fade-enter-from {
  opacity: 0;
}

.modal-fade-enter-to {
  opacity: 1;
}

.modal-fade-leave-from {
  opacity: 1;
}

.modal-fade-leave-to {
  opacity: 0;
}
</style>