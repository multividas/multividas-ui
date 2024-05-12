<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 24 24"
    :width="x"
    :height="y"
    :stroke-width="strokeWidth"
    stroke="currentColor"
    fill="none"
    stroke-linecap="round"
    stroke-linejoin="round"
    class="icon icon-tabler icon-tabler-gif"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M8 8h-2a2 2 0 0 0 -2 2v4a2 2 0 0 0 2 2h2v-4h-1" />
    <path d="M12 8v8" />
    <path d="M16 12h3" />
    <path d="M20 8h-4v8" />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType.js'

export default defineComponent({
  name: 'GIFIcon',
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
