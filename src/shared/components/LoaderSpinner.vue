<script setup lang="ts">
import { toRefs } from 'vue';

interface Props {
  color?: string;
  size?: string;
  thickness?: number;
  showText?: boolean;
}

const props = withDefaults(defineProps<Props>(), {
  color: 'primary',
  size: '3rem',
  thickness: 5,
  showText: true,
});

const { color, size, thickness, showText } = toRefs(props);
</script>

<template>
  <div class="column items-center">
    <q-spinner :color="color" :size="size" :thickness="thickness" />
    <span class="q-mt-sm" v-if="showText">Loading...</span>
  </div>
</template>

<style scoped></style>
