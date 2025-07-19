<script setup>
    const props = defineProps(['tarefasPendentes', 'tarefasFinalizadas'])
</script>

<template>
    <header class="p-5 mb-4 mt-4 bg-light rounded-3">
        <h1>Minhas tarefas</h1>
        <p>
            Você possui {{ props.tarefasPendentes }} tarefas pendentes
        </p>
        <p>
            Você possui {{ props.tarefasFinalizadas }} tarefas finalizadas
        </p>
    </header>
</template>