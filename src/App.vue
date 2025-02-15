<script setup lang="ts">
import { Popover } from 'radix-vue/namespaced';
</script>

<template>
  <div class="px-4">
    <Popover.Root>
      <Popover.Trigger class="cursor-pointer">
        Toggle popover
      </Popover.Trigger>
      
      <Popover.Portal>
        <Popover.Content class="px-4 py-2 bg-pink-400">
          I'm a popover!
        </Popover.Content>
      </Popover.Portal>
    </Popover.Root>
  </div>
</template>
