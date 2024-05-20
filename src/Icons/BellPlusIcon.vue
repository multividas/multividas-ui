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
    class="icon icon-tabler icon-tabler-bell-plus"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M12.5 17h-8.5a4 4 0 0 0 2 -3v-3a7 7 0 0 1 4 -6a2 2 0 1 1 4 0a7 7 0 0 1 4 6v1" />
    <path d="M9 17v1a3 3 0 0 0 3.51 2.957" />
    <path d="M16 19h6" />
    <path d="M19 16v6" />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType.js'

export default defineComponent({
  name: 'BellPlusIcon',
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
