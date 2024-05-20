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
    class="icon icon-tabler icon-tabler-at"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path d="M12 12m-4 0a4 4 0 1 0 8 0a4 4 0 1 0 -8 0" />
    <path d="M16 12v1.5a2.5 2.5 0 0 0 5 0v-1.5a9 9 0 1 0 -5.5 8.28" />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType'

export default defineComponent({
  name: 'AtIcon',
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
