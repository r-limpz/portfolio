<template>
    <button class="p-3 align-center text-center text-cyan-300 rounded-full border border-cyan-300 hover:bg-cyan-300 hover:text-black">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: "Button"
}
</script>