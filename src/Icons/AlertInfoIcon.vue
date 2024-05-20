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
    class="icon icon-tabler icon-tabler-info-circle"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M3 12a9 9 0 1 0 18 0a9 9 0 0 0 -18 0" />
    <path d="M12 9h.01" />
    <path d="M11 12h1v4h1" />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType'

export default defineComponent({
  name: 'AlertInfoIcon',
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
