<template>
    <div>
        <div v-for="items in Todata" :key="items">
            <!-- {{items.title}} -->
            <TodoItem v-bind:Todata="Todata" v-bind:items="items" v-on:delete-todo="$emit('delete-todo', items.id)">
            </TodoItem>
        </div>
    </div>
</template>
<script>
import TodoItem from './TodoItem.vue';

export default {
    name: "ToDos componemt",
    props: ["Todata"],
    components: { TodoItem }
}
</script>
<style scoped>
</style>