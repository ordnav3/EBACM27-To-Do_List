<script setup>
const props = defineProps(['tarefas']);
</script>

<template>
    <p v-if="props.tarefas <= 0" class="mt-5 btn btn-light w-100">Não existe tarefas</p>
    <ul v-else class="list-group mt-5">
        <li class="list-group-item" v-for="tarefa in props.tarefas">
            <input @change="evento => tarefa.finalizada = evento.target.checked" :checked="tarefa.finalizada"
                :id="tarefa.titulo" type="checkbox">
            <label :class="{ done: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">
                {{ tarefa.titulo }}
            </label>
        </li>
    </ul>
</template>

<style scoped>
.done {
    text-decoration: line-through;
}
</style>