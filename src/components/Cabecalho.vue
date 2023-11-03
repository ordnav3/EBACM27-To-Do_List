<script setup>
const props = defineProps(['tarefasPendentes'])
</script>

<template>
    <header class="p-5 mt-5 mb-5 bg-dark rounded-3 text-white">
        <h1>Minhas tarefas</h1>
        <p>
            Você possui {{ props.tarefasPendentes }} tarefas pedentes
        </p>
    </header>
</template>