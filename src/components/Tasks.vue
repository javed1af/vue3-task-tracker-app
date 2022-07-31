<template>
    <div :key="task.id" v-for="task in tasks">
        <!-- listen to events from child component Task -->
        <!-- and emit events to parent(root) component App -->
        <Task @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task" />
    </div>
</template>

<script>
import Task from './Task'

export default {
    name: 'Tasks',
    props: {
        tasks: Array,
    },
    components: {
        Task
    },
    // emits: ['delete-task', 'toggle-reminder'],
}
</script>