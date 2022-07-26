<template>
    <div class="grid justify-items-center">
        <br/>
        <h1 class="text-center">ToDos App </h1>
        <form class="grid justify-items-left bg-slate-200 p-7 w-64">
            <div>
                <input type="text" name="Title" placeholder="Title" required/> 
            </div>
            <br/>
            <div>
                <button class=" bg-blue-600 border-1 border-black text-white p-1 rounded-md font-serif font-semibold "> Add </button>
            </div>
        </form>
    </div>
</template>
<script>
    export default{
        name : "AddToDo component"
    }
</script>
<style scoped>
/* form{
    width: 220px;
}
button {
    color: whitesmoke;
    background-color: red;
    float: right;

} */
</style>