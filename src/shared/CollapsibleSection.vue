<template>
    <div>
        <div class="header">
            <span v-if="open" @click="open = !open">Collapse</span>
            <span v-if="!open" @click="open = !open">Expand</span>
            </div>
            <slot v-if="open">
                <div>Default Content</div>
            </slot>
    </div>
</template>

<script>
export default {
  name: 'CollapsibleSection',
  data() {
    return { open: true };
  },
};
</script>
<style>
 .header {
     background-color: #bbb;
     padding: 3px;
     cursor: pointer;
 }
</style>
