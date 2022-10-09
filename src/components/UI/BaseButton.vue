<template>
    <button :class="mode" :type="type">
        <slot></slot>
    </button>
</template>

<script>
    export default {
        props: ['mode' , 'type']
    }
</script>

<style>
    .deleteButton{
        border: none;
        background: yellow;
    }
</style>