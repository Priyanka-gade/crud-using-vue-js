<template>
<div class="grid justify-items-left m-2 p-2 bg-slate-200">
    <div>
        <p>
        <input type="checkbox"/>
        {{items.title}}
        
            <button class="float-right"><i id="delete" class="fa fa-trash" aria-hidden="true" ></i></button>
        <button class="float-right"><i id="edit" class='fas fa-edit'></i></button>
        
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