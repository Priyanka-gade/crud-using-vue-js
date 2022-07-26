<template>
    <div class="grid justify-items-left m-2 p-2 bg-slate-200">
        <div>
            <p>
                <input type="checkbox" v-bind:checked="items.completed " />
                {{ items.title }}
                <button @click="$emit('delete-todo', items.id)" class="del float-right bg-red-500 rounded-md text-white p-1 m-1">Delete</button>
                <button class="float-right bg-green-800 rounded-md text-white p-1 m-1">Edit</button>

            </p>
        </div>
    </div>
</template>
<script>
export default {
    name: "TodoItem component",
    props: ['items']
}
</script>
<style>
</style>