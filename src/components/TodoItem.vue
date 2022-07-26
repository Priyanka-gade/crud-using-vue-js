<template>
    <div class="grid justify-items-left m-2 p-2 bg-slate-200">
        <div>
            <!-- class="line-through" v-bind:class="{'is-complete':items.completed}" -->
            <p>
                <input type="checkbox" />
                <!-- v-on:change="markcompleted" v-bind:checked="items.completed" -->
                {{ items.title }}
                <button @click="$emit('delete-todo', items.id)"
                    class="del font-serif font-semibold float-right bg-red-500 rounded-md text-white p-1 m-1">Delete</button>
                <button @click="update"
                    class="font-serif font-semibold float-right bg-green-800 rounded-md text-white p-1 m-1">Edit</button>
            </p>
        </div>
        <div v-if="this.flag">
            <form @submit="updatetodo">
                <div>
                    <input type="text" v-model="updateTitle" placeholder="Title" required />
                </div>
                <div>
                    <button class="float-left font-serif font-semibold bg-blue-700 rounded-md text-white p-1 m-1">
                        Update
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: "TodoItem component",
    props: ['items', 'Todata'],
    methods: {
        update() {
            this.flag = !this.flag;
        },
        updatetodo(e) {
            e.preventDefault()
            this.Todata.filter((items) => {
                if (items.id == this.items.id) {
                    //update the title
                    items.title = this.updateTitle
                }
            })
            //reset the flag
            this.flag = false
        }

    },
    data() {
        return {
            flag: false,
            updateTitle: ""
        }
    }
}
</script>
<style>
</style>