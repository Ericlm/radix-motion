<script setup lang="ts">
import { Popover } from 'radix-vue/namespaced';
import { AnimatePresence, Motion } from 'motion-v';
</script>

<template>
  <div class="px-4">
    <Popover.Root>
      <Popover.Trigger class="cursor-pointer">
        Toggle popover
      </Popover.Trigger>
      
      <Popover.Portal>
        <AnimatePresence>
          <Popover.Content as-child class="px-4 py-2 bg-pink-400">
              <Motion
              :initial="{ opacity: 0, scale: 0.95 }"
              :animate="{ opacity: 1, scale: 1 }"
              :exit="{ opacity: 0, scale: 0.95 }"
              :transition="{ duration: 0.3, ease: 'easeInOut' }"
            >
              I'm a popover!
            </Motion>
          </Popover.Content>
        </AnimatePresence>
      </Popover.Portal>
    </Popover.Root>
  </div>
</template>
