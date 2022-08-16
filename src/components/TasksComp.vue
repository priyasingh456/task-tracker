<template>
    <div>
        <div :key="task.id" v-for="task in tasks">
            <TaskComp :task="task" />
        </div>
    </div>
</template>

<script>
import TaskComp from './TaskComp.vue';
export default {
    name: "TasksComp",
    props: {
        tasks: Array
    },
    components: { TaskComp }
}
</script>

<style scoped>


</style>