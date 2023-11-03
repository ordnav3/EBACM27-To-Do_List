<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTempo', 'trocarFiltro', 'editaTarefaTempo'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTempo" @change="props.editaTarefaTempo" required
                    type="text" placeholder="Digite aqui a descrição da tarefa" class="form-control">
            </div>
            <div class="col-md-2">
                <button class="btn btn-dark d-flex">
                    Cadastrar
                </button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-control text-center">
                    <option value="todas">Todas tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>