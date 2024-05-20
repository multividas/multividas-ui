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
    class="icon icon-tabler icon-tabler-apps-filled"
    :style="styling"
  >
    <path stroke="none" d="M0 0h24v24H0z" fill="none" />
    <path
      d="M9 3h-4a2 2 0 0 0 -2 2v4a2 2 0 0 0 2 2h4a2 2 0 0 0 2 -2v-4a2 2 0 0 0 -2 -2z"
      stroke-width="0"
      fill="currentColor"
    />
    <path
      d="M9 13h-4a2 2 0 0 0 -2 2v4a2 2 0 0 0 2 2h4a2 2 0 0 0 2 -2v-4a2 2 0 0 0 -2 -2z"
      stroke-width="0"
      fill="currentColor"
    />
    <path
      d="M19 13h-4a2 2 0 0 0 -2 2v4a2 2 0 0 0 2 2h4a2 2 0 0 0 2 -2v-4a2 2 0 0 0 -2 -2z"
      stroke-width="0"
      fill="currentColor"
    />
    <path
      d="M17 3a1 1 0 0 1 .993 .883l.007 .117v2h2a1 1 0 0 1 .117 1.993l-.117 .007h-2v2a1 1 0 0 1 -1.993 .117l-.007 -.117v-2h-2a1 1 0 0 1 -.117 -1.993l.117 -.007h2v-2a1 1 0 0 1 1 -1z"
      stroke-width="0"
      fill="currentColor"
    />
  </svg>
</template>

<script lang="ts">
// Vue
import { defineComponent } from 'vue'
// Types
import StylingType from '../Types/StylingType'

export default defineComponent({
  name: 'AppsFilledIcon',
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
