<script setup>
    const props = defineProps({
        alerta:{
            type:Object,
            require: true
        }
    })
</script>

<template>
    <div
    class="text-white text-center p-3 uppercase font-bold mb-3 rounded-md bg-green-500"
    >
        {{ alerta.mensaje }}
    </div>
</template>


