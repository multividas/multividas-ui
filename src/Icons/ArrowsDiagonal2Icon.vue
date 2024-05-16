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
    class="icon icon-tabler icons-tabler-outline icon-tabler-arrows-diagonal-2"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M16 20l4 0l0 -4" />
    <path d="M14 14l6 6" />
    <path d="M8 4l-4 0l0 4" />
    <path d="M4 4l6 6" />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType.js'

export default defineComponent({
  name: 'ArrowsDiagonal2Icon',
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
