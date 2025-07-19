<script setup>
    const props = defineProps(['tarefas'])

    function possuiTarefas() {
        return props.tarefas.length > 0;
    }
</script>

<template>
    <ul v-if="tarefas.length > 0" class="list-group mt-4">
        <li class="list-group-item" v-for="tarefa in props.tarefas">
            <input @change="evento => tarefa.finalizada = evento.target.checked" :checked="tarefa.finalizada"
                :id="tarefa.titulo" type="checkbox">
            <label :class="{ done: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">
                {{ tarefa.titulo }}
            </label>
        </li>
    </ul>
    <p v-else class="text-center mt-4">Nenhuma tarefa cadastrada</p>
</template>

<style scoped>
.done {
    text-decoration: line-through;
}
</style>