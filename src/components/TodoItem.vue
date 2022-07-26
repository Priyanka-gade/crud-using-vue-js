<template>
<div>
    <div>
        <p>
        <input type="checkbox"/>
        {{items.title}}
        <button class="bg-red-500 rounded-md border-solid border-1 border-slate-50">delete</button>
        </p>
    </div>
</div>
</template>
<script>
    export default{
        name:"TodoItem component",
        props:['items']
    }
</script>
<style></style>