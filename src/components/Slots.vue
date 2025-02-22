<script setup>

</script>
<template>
    <div class="component">
        <h2>Component with slots</h2>
        <button>
            <slot name="icon"/> 
            <slot name="text"> Button </slot> 
    </button>
    </div>
</template>