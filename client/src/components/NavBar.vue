<script lang="ts">
import { ref } from "vue";
import { generateTabNavigation } from '../core/navigation';

export default {
  setup() {
    const items = ref(generateTabNavigation());
    return { items };
  },
};
</script>

<template>
  <div>
    <MenuBar :model="items">
      <template #start>
        <img
          alt="logo"
          src="/sh.png"
          height="40"
          class="mr-2"
        />
      </template>
    </MenuBar>
  </div>
</template>

<style lang="css">

</style>
