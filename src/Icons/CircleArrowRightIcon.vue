<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="x"
    :height="y"
    :stroke-width="strokeWidth"
    viewBox="0 0 24 24"
    fill="none"
    stroke="currentColor"
    stroke-linecap="round"
    stroke-linejoin="round"
    class="icon icon-tabler icons-tabler-outline icon-tabler-circle-arrow-right"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M12 3a9 9 0 1 0 0 18a9 9 0 0 0 0 -18" />
    <path d="M16 12l-4 -4" />
    <path d="M16 12h-8" />
    <path d="M12 16l4 -4" />
  </svg>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType.js'

export default defineComponent({
  name: 'CircleArrowRightIcon',
  props: {
    x: {
      required: true,
      type: Number
    },
    y: {
      required: true,
      type: Number
    },
    strokeWidth: {
      required: true,
      type: Number
    },
    color: {
      required: true,
      type: String
    }
  },
  data() {
    return {
      styling: {
        color: this.color
      } as StylingType
    }
  }
})
</script>
